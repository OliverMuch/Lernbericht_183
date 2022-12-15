# Lern-Bericht

Oliver Much; Cross Site Scripting

## Einleitung

Mit dem Cross Site Scripting kann der Inhalt einer Seite mittels Einschleusen von eigenem JavaScript-Code auf der seite verändert werden.

## Was habe ich gelernt?

Ich habe gelernt, dass bei einer Webapplikation das Escaping eine sehr wichtige Rolle spielt, um solche Manipulationen mit z.B. XSS zu vermeiden. 

## Beschreibung

✍️ Verwenden Sie drei verschiedene Medien, um zu zeigen, was Sie gelernt haben. Zum Beispiel:

Das Escaping schützt unsere Applikation von Manipulationen wie von XSS. Durch das Escaping verhindern wir, dass das Programm Problematische Benutzereingaben nicht "falsch" interpretiert. Wir wollen z.B. verhindern, dass durch die EIngabe von `<script/>` JavaScript-Code ausgeführt werden kann. Dazu müssen wir die Eingabe escapen. 

In `JSF` wird automatisch escaping betrieben. Es kann jedoch explizit ab- oder eingestellt werden. Dazu reicht dieser Code in den betroffenen `.xhtml` Dateien:
`<h:outputText value="#{newsitem.detail}" escaping="true"/>`

- Ein gut dokumentierter Code-Fetzen


![xss](https://user-images.githubusercontent.com/69577485/207817594-7e82a3e7-8a80-42fb-9e76-ab8617061062.gif)

## Verifikation

Das GIF zeigt, wie mittels Eingabe von JavaScript-Code der Inhalt verändert werden kann. Durch das Eingeben von dem  `<script></script>` Tag, wird die Eingabe als JavaScript-Code angesehen und das Programm führt den Code innerhalb der Tags aus. 

# Reflektion zum Arbeitsprozess

👍 Überlegen Sie sich jeweils etwas, was gut an Ihrer Arbeit lief;

👎 und etwas, was nicht gut lief.

**VBV**: ✍️ Formulieren Sie davon ausgehend einen _handelbaren_ Verbesserungsvorschlag.
