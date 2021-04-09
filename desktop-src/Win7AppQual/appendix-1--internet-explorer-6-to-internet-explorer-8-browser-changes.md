---
description: In der folgenden Tabelle werden die Änderungen zwischen Microsoft Internet Explorer 6 und Windows Internet Explorer 8 beschrieben.
ms.assetid: 5A7DDFC4-69A4-4B5A-9C0A-6172E2142494
title: IE 8-Browser Änderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7abf978d2211a03b59a78847a66efc21f3213c41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865356"
---
# <a name="appendix-1-internet-explorer-6-to-internet-explorer-8-browser-changes"></a>Anhang 1: Browser Änderungen von Internet Explorer 6 zu Internet Explorer 8

In der folgenden Tabelle werden die Änderungen zwischen Microsoft Internet Explorer 6 und Windows Internet Explorer 8 beschrieben.



Entwurfs Änderungen von Internet Explorer 6 zu Internet Explorer 7

Entwerfen von Änderungen von Internet Explorer 7 auf Internet Explorer 8

$ {ROWSPAN2} $Internet Explorer-Versionsverwaltung $ {Remove} $  

Überprüfen Sie den Code, der für Internet Explorer 6, Windows Internet Explorer 7 oder Internet Explorer 8 nicht ordnungsgemäß für bestimmte Fälle in Bezug auf die Ermittlung von [Benutzer-Agent-Zeichen folgen, Versions Vektoren oder bedingte Kommentare](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))angezeigt wird.

-   Wenn eine lange Benutzer-Agent-Zeichenfolge auf einen Server trifft, der nur kürzere UA-Zeichen folgen akzeptiert, wird Benutzern [eine Fehlerseite](https://www.enhanceie.com/ua.aspx)angezeigt.

<!-- -->

-   Die Kompatibilitäts Ansicht in Internet Explorer 8, die für Intranetsites standardmäßig aktiviert ist, sendet eine Benutzer-Agent-Zeichenfolge von Internet Explorer 7. Um zwischen Internet Explorer 7 und der Kompatibilitäts Ansicht zu unterscheiden, suchen Sie nach dem neuen Eincheck [Token](/archive/blogs/ie/).

$ {ROWSPAN3} $-Kompatibilitäts Updates für Standards

-   Gilt für [angegebene Dokument Modi](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)).
-   Der [Internet Explorer 8-Kompatibilitäts Ansichtsmodus](/archive/blogs/ie/), der für Intranetsites standardmäßig aktiviert ist, setzt normalerweise [Standard Updates von Internet Explorer 7 auf Internet Explorer 8 zurück](/archive/blogs/ie/site-compatibility-and-ie8).
-   Verwenden Sie den ["EmulateIE7" X-UA-kompatiblen http-](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx) Header oder das **Meta** -Element, um die Kompatibilitäts Ansicht für Websites oder bestimmte Webseiten zu aktivieren.

$ {Remove} $  

Quiranmodusausnahme: Sie müssen keine Kompatibilitäts Änderungen an den Webseiten vornehmen, die den "Quiri Mode DOCTYPE" angeben (durch Festlegen des "Standards-Compliance" DOCTYPE-Schalters auf "Off").

Gilt für Internet Explorer 7-Standards oder den Modus "Strict" und höher:

-   [XML-Prologe](/previous-versions/windows/internet-explorer/ie-developer/) in der ersten Zeile des Quellcodes bewirken nicht mehr, dass DOCTYPE-Deklarationen fehlschlagen.
-   Box [Model](/previous-versions/windows/internet-explorer/ie-developer/) Overflow-Inhalt überschneidet das Feld, und das Feld "div" wird nicht mehr automatisch so vergrößert, dass es dem Inhalt entspricht.
-   [Bestimmte CSS-Filter](/previous-versions/windows/internet-explorer/ie-developer/) (z \* . b. html, unter \_ Striche und/ \* \* /Kommentare) werden nicht unterstützt.
-   [Nur das äußerste Objekt Element in den in der Tabelle eingefügten Objekten](/previous-versions/windows/internet-explorer/ie-developer/) wird instanziiert.
-   [Anwendungen, die das SELECT-Element](/previous-versions/windows/internet-explorer/ie-developer/) verwenden, um ein HWND für die Verwendung mit Microsoft Win32-APIs zu erhalten, können unterbrechen, da das [SELECT-Element](/archive/blogs/ie/) jetzt ein fensterloses Steuerelement ist.
-   [CDF (Channel Definition Format)](/previous-versions/aa740486(v=msdn.10)) wird zugunsten von RSS-Feeds nicht unterstützt.
-   [XBM](/previous-versions/aa740486(v=msdn.10)), ein Abbild Erstellungs Format, das für X-basierte Systeme konzipiert ist, wird nicht unterstützt.
-   [Basis Tags](/previous-versions/aa740486(v=msdn.10)) außerhalb des Haupt Dokuments sind nicht zulässig.

Gilt für Internet Explorer 8-Standards-Modus und höher:

-   [Nicht geschlossene P-Elemente](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx) werden automatisch geschlossen, wenn Sie von den Elementen [**Table**](https://msdn.microsoft.com/library/ms535901(v=VS.85).aspx), [**Form**](https://msdn.microsoft.com/library/ms535249(v=VS.85).aspx), [**NOFRAMES**](https://msdn.microsoft.com/library/ms535857(v=VS.85).aspx)oder [**NoScript**](https://msdn.microsoft.com/library/ms535858(v=VS.85).aspx) gefolgt werden.
-   [Falsch](/archive/blogs/ie/site-compatibility-and-ie8) formatierter HTML-Code wird nicht unterstützt. Dies gilt für wohl geformtes, gültiges Markup.
-   Die ["ClassName"-Attribut](/archive/blogs/ie/site-compatibility-and-ie8) Syntax wird nicht unterstützt, sondern anstelle der "Class"-Syntax.
-   [Die Attribute](/archive/blogs/ie/site-compatibility-and-ie8) -Auflistung enthält nicht alle möglichen Attribute, die von Windows Internet Explorer erkannt werden.
-   Die [Attribut Reihenfolge wurde geändert](/archive/blogs/ie/site-compatibility-and-ie8), was sich auf die Attribute-Auflistung, innerHTML und outerHTML auswirkt.
-   Bei [getElementById](/archive/blogs/ie/site-compatibility-and-ie8) wird die Groß-/Kleinschreibung beachtet, und die namens Attribute werden nicht gesucht.
-   [Generische CSS-Präfix Selektoren](/archive/blogs/ie/site-compatibility-and-ie8) (d. \\ h \* . v: Syntax) werden nicht unterstützt, sondern anstelle von expliziten Tagnamen.
-   [CSS-Ausdrücke](/archive/blogs/ie/site-compatibility-and-ie8) werden nicht unterstützt, zugunsten der verbesserten CSS-Unterstützung oder der DHTML-Logik.
-   Code, der für benutzerdefinierte JSON-Objektmethoden gedacht ist, kann mit dem neuen systemeigenen [JSON-Objekt](/archive/blogs/ie/site-compatibility-and-ie8) in Internet Explorer 8 in Konflikt stehen.
-   Das [Festlegen der anfänglichen Eigenschaften](/archive/blogs/ie/site-compatibility-and-ie8) für das currentStyle-Objekt gibt den ursprünglichen Wert zurück.
-   [Nicht angegebene Eigenschaftswerte](/archive/blogs/ie/site-compatibility-and-ie8) für das Objekt Stil Objekt currentStyle geben eine leere Zeichenfolge zurück (z. b. im Blogbeitrag [ASP.net und IE8 Rendering White Issue](/archive/blogs/giorgio/) ).

<!-- -->

-   Für Websites und Anwendungen, bei denen Barrierefreiheit von Bedeutung ist, aktualisieren Sie die [Aria-Syntax in allen Internet Explorer-Renderingmodi](/archive/blogs/ie/).
-   Überprüfen Sie die [komplette Liste der CSS-Updates von Internet Explorer 6 zu Internet Explorer 8](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx).

Verbesserungen der Sicherheit

-   Anwenden unabhängig vom Dokument Modus.
-   Mithilfe [Gruppenrichtlinie](https://www.microsoft.com/p/group-policy/9wzdncrfjtm4?activetab=pivot:overviewtab)können Sie die Sicherheitsfunktionen deaktivieren.

<!-- -->

-   Das [Fenster "Fenster. Opener](/previous-versions/aa740486(v=msdn.10)) " wird mit der Fenster-und schließende Eingabeaufforderung nicht zugelassen.
-   Der [Schutz von Objekt Zwischenspeichern](/previous-versions/windows/internet-explorer/ie-developer/) ist standardmäßig aktiviert, wodurch der Zugriff auf Verweise von Objekten blockiert wird, wenn Benutzer eine neue Domäne suchen (gilt für Internet Explorer 6 und höhere Versionen unter Windows XP mit Service Pack 2 (SP2) und höhere Versionen).
-   [DHTML-Skriptlets](/previous-versions/windows/internet-explorer/ie-developer/) sind standardmäßig deaktiviert.
-   [Skripts, die in die Statusleiste schreiben,](/previous-versions/windows/internet-explorer/ie-developer/) werden blockiert.
-   Die [URL-Erstellung schlägt möglicherweise fehl](/previous-versions/windows/internet-explorer/ie-developer/) , wenn URLs keine RFC-Richtlinien erfüllen.
-   Auf [HTTPS-Seiten wird eine Fehlerseite angezeigt](/previous-versions/windows/internet-explorer/ie-developer/) , wenn der Standort nur für SSLv2 konfiguriert ist, oder wenn das Standort Sicherheitszertifikat veraltet oder ungültig ist, Fehler aufweist oder schwache Chiffren aufweist.
-   Nur ["Punycode" codierte internationalisierte Domänen Namen](/previous-versions/windows/internet-explorer/ie-developer/) werden unterstützt. Andere Formate wie ANSI und UTF-8 werden blockiert.
-   [Domänen übergreifende Skript-URLs](/previous-versions/windows/internet-explorer/ie-developer/), umgeleitete Navigation in DOM-Objekten und Frame Navigationen werden blockiert.
-   [Modale oder nicht modale Dialogfelder](/previous-versions/aa740486(v=msdn.10)) , die aus Skripts erstellt werden, scheinen [etwas größer](/archive/blogs/ie/)zu sein.
-   [Unsichere Protokolle](/previous-versions/aa740486(v=msdn.10)) Ansichts Quelle, Gopher (auf WinInet-Ebene) und Telnet sind nicht funktionsfähig.

<!-- -->

-   Der [XSS-Filter](/archive/blogs/ie/) ist standardmäßig aktiviert, wodurch Skript Muster blockiert werden, die am häufigsten Typ-1 XSS-Angriffen ähneln, es sei denn, Sie deaktivieren Sie über einen X-XSS-Protection-HTTP-Header.
-   Domänen übergreifende, Dokument übergreifende Kommunikations-und XDR-Funktionen wie [Skript](/archive/blogs/jscript/) Erstellung werden nicht unterstützt. Dies ist eine sicherere [xdm-und XDR-AJAX-](/archive/blogs/ie/)Funktion.
-   AJAX-aktivierte Websites, die [den Hash der URL manuell bearbeiten](/previous-versions//cc891506(v=vs.85)) , werden möglicherweise durch die neue Window. Location. Hash-Navigations Eigenschaft beschädigt.
-   [Neue AJAX-Funktionen](https://msdn.microsoft.com/library/Gg598940(v=VS.85).aspx) wie [xdm](/archive/blogs/ie/) haben systemeigene [**Eigenschaften**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc288548(v=vs.85)) , die möglicherweise mit vorhandenen benutzerdefinierten Eigenschaften in Konflikt stehen.
-   Beim [Dateiuploadsteuerelement](/archive/blogs/ie/) wird nur der Dateipfad und nicht der vollständige Pfad an den Server gesendet.
-   Der HTML-Code oder das Skript, das mit dem [ \* MIME-Typ "Image/"](/archive/blogs/ie/) übermittelt wird, kann nicht ausgeführt werden.
-   Wenn Sie [einen Frame auf oberster Ebene](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565638(v=vs.85)) zu einer Website in einem anderen Sicherheitskontext navigieren, wird ein neues Fenster oder eine neue Registerkarte geöffnet, anstatt innerhalb des vorhandenen Frames zu navigieren.
-   Das [UTF-7-codierte Skript](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565635(v=vs.85)) wird in Windows-1252-Codierung erzwungen, was zu einem reinen Text Rendering führen kann.
-   Auf [HTTP/HTTPS-Seiten im gemischten Modus](/archive/blogs/askie/mixed-content-and-internet-explorer-8-0) wird ein Dialogfeld angezeigt, in dem standardmäßig nur sichere Elemente angezeigt werden (im Gegensatz zum vorherigen nicht sicheren Standard). Benutzer können versehentlich [http-Elemente blockieren](/archive/blogs/askie/mixed-content-and-internet-explorer-8-0), wie z. b. Schlüsselbilder.
-   [DEP/NX ist standardmäßig aktiviert. dadurch](https://www.microsoft.com/windows/internet-explorer/readiness/developers-existing.aspx#depnx)werden bestimmte Add-ons (d. h. ActiveX-Steuerelemente und COM-Objekte), die mit älteren Versionen von ATL erstellt werden, in der Ausführung von Code, der im Arbeitsspeicher als "nicht ausführbare Datei" gekennzeichnet ist, blockiert.
-   [Inhalt, der von einem WebProxy zurückgegeben wird,](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565641(v=vs.85)) wird blockiert, wenn ein SSL-Tunnel nicht als Reaktion auf eine Verbindungsanforderung an den ursprünglichen Server eingerichtet wird.

Änderungen an der Architektur

-   Anwenden unabhängig vom Dokument-oder Kompatibilitätsmodus.

<!-- -->

-   Der [geschützte Modus](/previous-versions/windows/internet-explorer/ie-developer/) ist für [Internet-, Intranet-und eingeschränkte Sites-Zonen](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537187(v=vs.85))standardmäßig aktiviert. Dieser Modus [blockiert Browser Erweiterungen, die ein Sicherheitsrisiko darstellen können](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565645(v=vs.85)) , wenn Anwendungen ausgeführt werden und [Anwendungen mit niedrigerer Berechtigung auf höhere Berechtigungs Prozesse zugreifen](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565646(v=vs.85)), wie z. b. das Startmenü, die Systemsteuerung und die Microsoft Windows-Registrierung (gilt für Internet Explorer 7 und höhere Versionen unter Windows Vista und höheren Versionen).

<!-- -->

-   [Update für den geschützten Modus](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565648(v=vs.85)): das Intranet wird standardmäßig in mittlerer (anstatt niedriger) Integritäts Stufe ausgeführt.
-   [Lose gekoppelte Internet Explorer](https://www.microsoft.com/windows/internet-explorer/readiness/developers-existing.aspx#lcie) blockiert möglicherweise Add-ons (d. h. ActiveX-Steuerelemente und COM-Objekte), die eine der folgenden Aktionen ausführen:
    -   Verwenden Sie Windows Hierarchy-Techniken, um UI-Frame-und Registerkarten Fenster zu suchen (die nun in separaten Prozessen auf verschiedenen Integritäts Ebenen ausgeführt werden).
    -   Erstellen Sie eine Unterklasse des Benutzeroberflächen Rahmens (jetzt mit mittlerer Integritäts Ebene) aus einem Registerkarten Prozess mit niedriger Integrität.
    -   Verwenden Sie nicht unterstützte Messaging Techniken zwischen dem Benutzeroberflächen Rahmen und Registerkarten.



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Adressierung der Anwendungskompatibilität beim Migrieren zu Internet Explorer 8](addressing-application-compatibility-when-migrating-to-internet-explorer-8.md)
</dt> </dl>

 

 
