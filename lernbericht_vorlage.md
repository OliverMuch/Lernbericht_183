# Lern-Bericht

Oliver Much; Cross Site Scripting

## Einleitung

Mit dem Cross Site Scripting kann der Inhalt einer Seite mittels Einschleusen von eigenem JavaScript-Code auf der seite verändert werden.

## Was habe ich gelernt?

Ich habe gelernt, dass bei einer Webapplikation das Escaping eine sehr wichtige Rolle spielt, um solche Manipulationen mit z.B. XSS zu vermeiden. 

## Beschreibung

Das Escaping schützt unsere Applikation von Manipulationen wie von XSS. Durch das Escaping verhindern wir, dass das Programm Problematische Benutzereingaben nicht "falsch" interpretiert. Wir wollen z.B. verhindern, dass durch die EIngabe von `<script/>` JavaScript-Code ausgeführt werden kann. Dazu müssen wir die Eingabe escapen. 

In `JSF` wird automatisch escaping betrieben. Es kann jedoch explizit ab- oder eingestellt werden. Dazu reicht dieser Code in den betroffenen `.xhtml` Dateien:
`<h:outputText value="#{newsitem.detail}" escaping="true"/>`
Durch dieses Codestück werden die Eingaben aus dem TextField automatisch escaped. 


![xss](https://user-images.githubusercontent.com/69577485/207817594-7e82a3e7-8a80-42fb-9e76-ab8617061062.gif)

## Verifikation

Das GIF zeigt, wie mittels Eingabe von JavaScript-Code der Inhalt verändert werden kann. Durch das Eingeben von dem  `<script></script>` Tag, wird die Eingabe als JavaScript-Code angesehen und das Programm führt den Code innerhalb der Tags aus. 

# Reflektion zum Arbeitsprozess

👍 Ich habe schnell die Funktionsweise von XSS verstanden und konnte es bei meinem Projekt ausprobieren. 

👎 Zu Beginn des Auftrags war mir noch unklar, wie man das XSS escapen konnte und ich habe Zeit beim Überlegen verloren. 

**VBV**: ✍️ Formulieren Sie davon ausgehend einen _handelbaren_ Verbesserungsvorschlag.
