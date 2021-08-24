---
description: In der folgenden Tabelle werden die Änderungen zwischen Microsoft Internet Explorer 6 und Windows Internet Explorer 8 beschrieben.
ms.assetid: 5A7DDFC4-69A4-4B5A-9C0A-6172E2142494
title: Änderungen am IE 8-Browser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c775448d8eca55097b0121592c28ece0b2c347f4492e7a48b2d51d9ab688fa89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680290"
---
# <a name="appendix-1-internet-explorer-6-to-internet-explorer-8-browser-changes"></a>Anhang 1: Browseränderungen Internet Explorer 6 bis Internet Explorer 8

In der folgenden Tabelle werden die Änderungen zwischen Microsoft Internet Explorer 6 und Windows Internet Explorer 8 beschrieben.



Entwurfsänderungen von Internet Explorer 6 in Internet Explorer 7

Entwurfsänderungen von Internet Explorer 7 in Internet Explorer 8

${ROWSPAN2}$Internet Explorer Versionierung${REMOVE}$  

Suchen Sie nach Code, der fälschlicherweise Sonderfälle um Internet Explorer 6, Windows Internet Explorer 7 oder Internet Explorer 8 durch [Zeichenfolgensniffing des Benutzer-Agents, Versionsvektoren oder bedingte Kommentare](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))enthält.

-   Wenn eine lange Benutzer-Agent-Zeichenfolge (UA) auf einen Server trifft, der nur kürzere UA-Zeichenfolgen akzeptiert, wird Benutzern [eine Fehlerseite angezeigt.](https://www.enhanceie.com/ua.aspx)

<!-- -->

-   Die Kompatibilitätsansicht in Internet Explorer 8, die standardmäßig für Intranetsites aktiviert ist, sendet eine Internet Explorer 7-Benutzer-Agent-Zeichenfolge. Um zwischen Internet Explorer 7 und Kompatibilitätsansicht zu unterscheiden, suchen Sie nach dem neuen [Trident-Token.](/archive/blogs/ie/)

${ROWSPAN3}$ Updates der Standardskonformität

-   Gilt für [angegebene Dokumentmodi.](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85))
-   [Internet Explorer 8 Kompatibilitätsansicht Modus](/archive/blogs/ie/), der für Intranetsites standardmäßig aktiviert ist, werden Standardupdates in der Regel [von Internet Explorer 7 auf Internet Explorer 8 zurückgesetzt.](/archive/blogs/ie/site-compatibility-and-ie8)
-   Verwenden Sie den [EmullateIE7 X-UA-kompatiblen HTTP-Header](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx) oder das **Metaelement,** um Kompatibilitätsansicht auf Websites oder bestimmten Webseiten zu aktivieren.

${REMOVE}$  

Ausnahme im Quirksmodus: Sie müssen keine Änderungen an der Standardskonformität für Webseiten vornehmen, die den quirks-Modus DOCTYPE angeben (indem Sie den DOCTYPE-Schalter "standards-compliance" auf "off" festlegen).

Gilt für Internet Explorer 7-Standards oder den Modus "Strict" und höher:

-   [XML-Prologs](/previous-versions/windows/internet-explorer/ie-developer/) in der ersten Zeile des Quellcodes führen nicht mehr dazu, dass DOCTYPE-Deklarationen fehlschlagen.
-   [Der](/previous-versions/windows/internet-explorer/ie-developer/) Inhalt des Boxmodellüberlaufs überschneidet das Feld und passt nicht mehr automatisch die Box div an den Inhalt an.
-   [Bestimmte CSS-Filter](/previous-versions/windows/internet-explorer/ie-developer/) (z. B. \* \_ HTML, Unterstrich und \* \* //comment) werden nicht unterstützt.
-   [Nur das äußerste OBJECT-Element in geschachtelten Objekten](/previous-versions/windows/internet-explorer/ie-developer/) wird instanziiert.
-   [Anwendungen, die auf dem SELECT-Element basieren,](/previous-versions/windows/internet-explorer/ie-developer/) um ein HWND für die Verwendung mit Microsoft Win32-APIs abzurufen, können möglicherweise ausfallen, da das [SELECT-Element](/archive/blogs/ie/) jetzt ein fensterloses Steuerelement ist.
-   [Das Kanaldefinitionsformat (Channel Definition Format, CDF)](/previous-versions/aa740486(v=msdn.10)) wird zugunsten von RSS-Feeds nicht unterstützt.
-   [XBM](/previous-versions/aa740486(v=msdn.10)), ein Bildverarbeitungsformat, das für X-basierte Systeme entwickelt wurde, wird nicht unterstützt.
-   [BASIStags](/previous-versions/aa740486(v=msdn.10)) außerhalb des HEAD-Dokuments sind nicht zulässig.

Gilt für Internet Explorer 8-Standards-Modus und höher:

-   [Nicht geschlossene P-Elemente](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx) werden automatisch geschlossen, wenn auf sie [**TABLE-,**](https://msdn.microsoft.com/library/ms535901(v=VS.85).aspx) [**FORM-,**](https://msdn.microsoft.com/library/ms535249(v=VS.85).aspx) [**NOFRAMES-**](https://msdn.microsoft.com/library/ms535857(v=VS.85).aspx)oder [**NOSCRIPT-Elemente**](https://msdn.microsoft.com/library/ms535858(v=VS.85).aspx) folgen.
-   [Falsch formatiertes HTML](/archive/blogs/ie/site-compatibility-and-ie8) wird zugunsten von wohlgeformten, gültigen Markups nicht unterstützt.
-   Die [Attributsyntax "className"](/archive/blogs/ie/site-compatibility-and-ie8) wird zugunsten der Syntax "class" nicht unterstützt.
-   [Die Attributauflistung](/archive/blogs/ie/site-compatibility-and-ie8) enthält nicht alle möglichen Attribute, die Windows Internet Explorer erkennt.
-   [Die Attributreihenfolge hat sich geändert](/archive/blogs/ie/site-compatibility-and-ie8)und wirkt sich auf die Attributauflistung, innerHTML und outerHTML aus.
-   [Bei GetElementById](/archive/blogs/ie/site-compatibility-and-ie8) wird die Groß-/Kleinschreibung beachtet, und namensattribute werden nicht durchsucht.
-   [Generische CSS-Präfixselektoren](/archive/blogs/ie/site-compatibility-and-ie8) (d.h. v \\ : \* Syntax) werden zugunsten expliziter Tagnamen nicht unterstützt.
-   [CSS-Ausdrücke](/archive/blogs/ie/site-compatibility-and-ie8) werden nicht unterstützt, zugunsten der verbesserten CSS-Unterstützung oder DHTML-Logik.
-   Code, der für benutzerdefinierte JSON-Objektmethoden vorgesehen ist, kann mit dem [neuen nativen JSON-Objekt](/archive/blogs/ie/site-compatibility-and-ie8) in Internet Explorer 8 in Konflikt geraten.
-   [Die anfänglichen Eigenschaften](/archive/blogs/ie/site-compatibility-and-ie8) für das currentStyle-Objekt werden nicht mehr abgeschaltet und geben ihren Anfangswert zurück.
-   [Nicht angegebene Eigenschaftswerte](/archive/blogs/ie/site-compatibility-and-ie8) für das currentStyle-Objektstilobjekt geben eine leere Zeichenfolge zurück (siehe z. B. den Blogbeitrag ASP.NET Menu and IE8 rendering white issue (ASP.NET [Menu und IE8 Rendering White Issue).](/archive/blogs/giorgio/)

<!-- -->

-   Aktualisieren Sie für Standorte und Anwendungen, bei denen die Barrierefreiheit ein Problem darstellt, [die ARIA-Syntax für alle Internet Explorer Renderingmodi.](/archive/blogs/ie/)
-   Überprüfen Sie die [vollständige Liste der CSS-Updates von Internet Explorer 6 bis Internet Explorer 8.](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx)

Verbesserungen der Sicherheit

-   Gilt unabhängig vom Dokumentmodus.
-   Sie können Sicherheitsfeatures deaktivieren, indem Sie [Gruppenrichtlinie](https://www.microsoft.com/p/group-policy/9wzdncrfjtm4?activetab=pivot:overviewtab)verwenden.

<!-- -->

-   Die [Window.opener-Umgehung](/previous-versions/aa740486(v=msdn.10)) der Window.close-Eingabeaufforderung ist nicht zulässig.
-   Der [Objektzwischenspeicherungsschutz](/previous-versions/windows/internet-explorer/ie-developer/) ist standardmäßig aktiviert, wodurch der Zugriff auf Verweise auf Objekte blockiert wird, wenn Benutzer zu einer neuen Domäne navigieren (gilt für Internet Explorer 6 und höhere Versionen auf Windows XP mit Service Pack 2 (SP2) und höher).
-   [DHTML-Skriptlets](/previous-versions/windows/internet-explorer/ie-developer/) sind standardmäßig deaktiviert.
-   [Skripts, die in die Statusleiste schreiben,](/previous-versions/windows/internet-explorer/ie-developer/) werden blockiert.
-   [Die URL-Erstellung schlägt möglicherweise fehl,](/previous-versions/windows/internet-explorer/ie-developer/) wenn DIE URLs nicht den RFC-Richtlinien entsprechen.
-   [HTTPS-Seiten zeigen eine Fehlerseite](/previous-versions/windows/internet-explorer/ie-developer/) an, wenn die Website nur für SSLv2 konfiguriert ist oder wenn das Websitesicherheitszertifikat veraltet oder ungültig ist, Fehler aufweist oder schwache Verschlüsselungen aufweist.
-   Nur ["Punycode"-codierte internationalisierte Domänennamen](/previous-versions/windows/internet-explorer/ie-developer/) werden unterstützt. Andere Formate wie ANSI und UTF-8 werden blockiert.
-   [Domänenübergreifende Skript-URLs,](/previous-versions/windows/internet-explorer/ie-developer/)umgeleitete Navigation in DOM-Objekten und Framenavigationen werden blockiert.
-   [Modale oder moduslose Dialogfelder,](/previous-versions/aa740486(v=msdn.10)) die aus dem Skript erstellt werden, erscheinen möglicherweise [etwas größer.](/archive/blogs/ie/)
-   [Unsichere Protokolle](/previous-versions/aa740486(v=msdn.10)) view-source, Gopher (auf WinINET-Ebene) und Telnet funktionieren nicht.

<!-- -->

-   [Der XSS-Filter](/archive/blogs/ie/) ist standardmäßig aktiviert, wodurch Skriptmuster blockiert werden, die XSS-Angriffen vom Typ 1 am häufigsten ähneln, es sei denn, Sie deaktivieren sie über einen X-XSS-Protection-HTTP-Header.
-   Domänenübergreifende, dokumentübergreifende Kommunikations-Hacks wie [SCRIPT SRC](/archive/blogs/jscript/) werden zugunsten [sichererer XDM- und XDR AJAX-Features](/archive/blogs/ie/)nicht unterstützt.
-   AJAX-fähige Websites, [die den Hash der URL manuell bearbeiten,](/previous-versions//cc891506(v=vs.85)) werden möglicherweise durch die neue navigationseigenschaft window.location.hash beschädigt.
-   [Neue AJAX-Features](https://msdn.microsoft.com/library/Gg598940(v=VS.85).aspx) wie [XDM](/archive/blogs/ie/) verfügen über [**native Eigenschaften,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc288548(v=vs.85)) die mit vorhandenen benutzerdefinierten Eigenschaften in Konflikt stehen können.
-   [Das Dateiuploadsteuerelement](/archive/blogs/ie/) sendet nur den Dateipfad und nicht den vollständigen Pfad an den Server.
-   HTML-Code oder -Skript, der bzw. das mit dem [ \* MIME-Typ "image/"](/archive/blogs/ie/) bereitgestellt wird, wird an der Ausführung gehindert.
-   [Wenn Sie einen Rahmen der obersten Ebene](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565638(v=vs.85)) zu einer Website in einem anderen Sicherheitskontext navigieren, wird ein neues Fenster oder eine neue Registerkarte geöffnet, anstatt innerhalb des vorhandenen Frames zu navigieren.
-   [UTF-7-codiertes Skript](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565635(v=vs.85)) wird in Windows-1252-Codierung erzwungen, was zu Nur-Text-Rendering führen kann.
-   [Http/HTTPS-Seiten im "gemischten Modus"](/archive/blogs/askie/mixed-content-and-internet-explorer-8-0) zeigen ein Dialogfeld an, in dem standardmäßig nur sichere Elemente angezeigt werden (im Gegensatz zum vorherigen unsicheren Standard). Benutzer entscheiden sich möglicherweise versehentlich [dafür, HTTP-Elemente wie](/archive/blogs/askie/mixed-content-and-internet-explorer-8-0)Schlüsselbilder zu blockieren.
-   [DEP/NX ist standardmäßig aktiviert,](https://www.microsoft.com/windows/internet-explorer/readiness/developers-existing.aspx#depnx)wodurch bestimmte Add-Ons (d. h. ActiveX-Steuerelemente und COM-Objekte) blockiert werden, die mit älteren Versionen von ATL erstellt wurden, um Code auszuführen, der als "nicht ausführbare Datei" im Arbeitsspeicher markiert ist.
-   [Inhalte, die von einem Webproxy zurückgegeben werden,](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565641(v=vs.85)) werden blockiert, wenn kein SSL-Tunnel als Antwort auf eine CONNECT-Anforderung an den ursprünglichen Server eingerichtet wird.

Änderungen der Architektur

-   Gilt unabhängig vom Dokument- oder Kompatibilitätsmodus.

<!-- -->

-   [Der geschützte Modus](/previous-versions/windows/internet-explorer/ie-developer/) ist standardmäßig für [Internet-, Intranet- und Eingeschränkte Sites-Zonen](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537187(v=vs.85))aktiviert. Dieser Modus [blockiert Browsererweiterungen, die ein Sicherheitsrisiko darstellen könnten,](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565645(v=vs.85)) wenn Anwendungen mit und [niedrigeren Berechtigungen auf Prozesse](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565646(v=vs.85))mit höheren Berechtigungen zugreifen, z. B. die Startmenü, Systemsteuerung und die Microsoft Windows-Registrierung (gilt für Internet Explorer 7 und höhere Versionen auf Windows Vista und höheren Versionen).

<!-- -->

-   [Update im geschützten Modus:](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565648(v=vs.85))Intranet wird standardmäßig auf mittlerer (statt niedriger) Integritätsebene ausgeführt.
-   [Lose gekoppelte Internet Explorer](https://www.microsoft.com/windows/internet-explorer/readiness/developers-existing.aspx#lcie) können Add-Ons (d. b. ActiveX-Steuerelemente und COM-Objekte) blockieren, die eines der folgenden Aufgaben ausführen:
    -   Verwenden Sie Windows-Hierarchietechniken, um Benutzeroberflächenrahmen und Registerkartenfenster zu suchen (die jetzt in separaten Prozessen auf unterschiedlichen Integritätsebenen ausgeführt werden).
    -   Erstellen Sie eine Unterklasse des Benutzeroberflächenframes (jetzt auf mittlerer Integritätsebene) aus einem Registerkartenprozess mit niedriger Integrität.
    -   Verwenden Sie nicht unterstützte Messagingtechniken zwischen Benutzeroberflächenrahmen und Registerkarten.



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Adressierung der Anwendungskompatibilität beim Migrieren zu Internet Explorer 8](addressing-application-compatibility-when-migrating-to-internet-explorer-8.md)
</dt> </dl>

 

 
