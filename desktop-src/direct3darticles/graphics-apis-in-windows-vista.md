---
title: Grafik-APIs in Windows
description: In diesem Artikel werden Windows Grafikfeatures und APIs erläutert.
ms.assetid: 54cd5027-cdcf-fc4a-40a9-beacfaa08681
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 848f24c42aa98c6d27a0873ab07c389dea24826d880188837536d83bd87549b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987158"
---
# <a name="graphics-apis-in-windows"></a>Grafik-APIs in Windows

Windows Vista bietet Unterstützung für ein völlig neues Anzeigetreibermodell, das seit der Einführung des Windows Driver Model (WDM) für Windows 98 eine wichtige Überarbeitung des Entwurfs von Videotreibern darstellt. Dieses neu gestaltete Modell spiegelt die Weiterentwicklung der Videohardware von der Welt der 2D-Rastervorgänge und GDI-Anwendungen zur Entwicklung von 3D-Spielen mit Grafikhardware mit fester Funktion und schließlich zur Entwicklung der modernen programmierbaren Grafikverarbeitungseinheit (GPU) wider, die eine Vielzahl von Hochleistungsgrafikanwendungen unterstützt. Windows 7 und Windows 8 auf der Windows Vista-Grafikinfrastruktur aufbauen, indem sie zusätzliche Grafikfeatures und APIs bereitstellen. In diesem Artikel werden Windows Grafikfeatures und APIs erläutert.

-   [Hintergrund](#background)
-   [Direct3D 9](#direct3d-9)
-   [Direct3D 9Ex](#direct3d-9ex)
-   [Direct3D 10](#direct3d-10)
-   [Direct3D 10.1](#direct3d-101)
-   [Direct3D 11](#direct3d-11)
-   [Direct3D 11.1](#direct3d-111)
-   [Opengl](#opengl)
-   [Anwendungskompatibilität, GDI und ältere Versionen von Direct3D](#application-compatibility-gdi-and-older-versions-of-direct3d)
-   [Empfehlungen](#recommendations)

## <a name="background"></a>Hintergrund

Die primäre API für die Programmierung von Grafiken seit den frühen Tagen Windows ist die grafische Geräteschnittstelle (GDI). Diese API wurde für die Verarbeitung zahlreicher 2D-Ausgabegeräte entwickelt und bildete die Grundlage für die Windows Benutzeroberfläche. DirectDraw und Direct3D wurden als alternative APIs eingeführt, um Vollbildspiele und 3D-Rendering als Erweiterungen der vorhandenen Hardware zu unterstützen. Interaktionen mit GDI waren kompliziert. Die effektive Mischung herkömmlicher GDI-Elemente mit Direct3D-Elementen wurde durch diesen Entwurf eingeschränkt. Die Windows XP-Version von WDM, die als XPDM bezeichnet wird, spiegelt die nebeneinandere Natur von GDI und Direct3D wider (siehe Abbildung 1).

**Abbildung 1: Grafik-APIs in Windows XP**

![Xpdm](images/graphics-apis-in-windows-xp.gif)

Im Laufe der Jahre hat sich die Leistungsfähigkeit von 3D-Grafikkarten erheblich erhöht, bis der Großteil der Hardware für diese Funktion bestimmt ist. Ein neues Treibermodell, Windows Display Driver Model (WDDM), bringt GPU und Direct3D in den Vordergrund und ermöglicht die Erstellung einer völlig neuen Benutzeroberfläche, des 3D-Desktops, der die 2D-Welt von GDI nahtlos mit der Leistung moderner programmierbarer GPUs kombiniert. Mit WDDM wird die Videohardware vollständig von Direct3D gesteuert, und alle anderen Grafikschnittstellen kommunizieren mit der Videohardware über das neue Direct3D-zentrierte Treibermodell (siehe Abbildung 2).

**Abbildung 2. Grafik-APIs in Windows Vista**

![Wddm](images/graphics-apis-in-windows-vista.gif)

Weitere Informationen zum WDDM finden Sie im [Entwurfshandbuch für Windows Vista Display Driver Model (WDDM)](/windows-hardware/drivers/display/windows-vista-display-driver-model-design-guide) auf MSDN.

## <a name="direct3d-9"></a>Direct3D 9

Version 9 von DirectX wurde erstmals 2002 für Windows veröffentlicht, mit nachfolgenden Updates in den Jahren 2003 und 2004. Diese API stellt ein Zehntausendfache der Weiterentwicklung der DirectX-Technologien, die Einführung leistungsfähigerer Shaderprogrammiermodelle für Direct3D und eine Reife dar, die von Tausenden von Versandtiteln unterstützt wird. Direct3D 9 ist die primäre Grafikschnittstelle auf Windows Vista. Es bleibt die ideale API zum Schreiben von 3D-Spielen und -Anwendungen, die auf der breiten Palette vorhandener Hardware und Windows Releases ausgeführt werden müssen. Die Details des neuen Treibermodells werden für Anwendungen mithilfe der Direct3D 9-Schnittstellen ausgeblendet, aber im Hintergrund nutzt das Betriebssystem die neuen Funktionen vollständig, um echtes Multitasking der GPU, eine effizientere Ressourcenverwaltung und eine stabile Leistung bereitzustellen.

Um vollständige Kompatibilität mit älteren Versionen von Windows sicherzustellen, müssen einige Eigenheiten des alten Treibermodells auch mit dem neuen Windows Vista-Anzeigetreibermodell emuliert werden. Wenn beispielsweise eine Vollbildanwendung den Fokus verliert, muss sie davon ausgehen, dass sie alle Ressourcen im Videospeicher (VRAM) verloren hat, und diese, die sie als nicht verwaltete Ressourcen erstellt hat, erneut laden, obwohl das neue Treibermodell die Ressourcen transparent verarbeitet, ohne sie aus dem Gerätekontext zu entfernen. Auch das Konzept eines verwalteten im Vergleich zum Standardressourcentyp ist spezifisch für das alte Treibermodell. Ein weiteres Beispiel ist die Erwartung eines Fehlers beim Zuordnen von nicht verwalteten Ressourcen (Standardpool) über die verfügbare VRAM-Menge, obwohl das neue Treibermodell eine nahezu unbegrenzte Menge an virtuellem Videospeicher bereitstellen kann. Aufgrund dieser Anforderungen erhalten Direct3D-Anwendungen, die auf Windows Vista ausgeführt werden, weiterhin diese Fehlerbedingungen. Daher sind sie in ihrer Fähigkeit eingeschränkt, die grundlegenden Direct3D 9-Schnittstellen zu verwenden, um einige Features des neuen Treibermodells vollständig zu nutzen.

Während neue Systeme, die mit Windows Vista ausgeliefert werden, Grafikkarten mit WDDM-Treibern enthalten, und neue Treiber für eine Reihe beliebter Grafikkarten im Feld enthalten sind, unterstützt Windows Vista weiterhin die Möglichkeit, ältere XPDM-Treiber für Upgrades und Unternehmenseditionen zu verwenden. Auf Systemen, die das alte Treibermodell verwenden, müssen Direct3D 9 und ältere Schnittstellen verwendet werden, und der Betrieb des Grafiksystems ähnelt dem von Windows XP (Abbildung 1). WDDM ist erforderlich, damit Anwendungen Direct3D 9Ex, Direct3D 10 und höhere Versionen verwenden können.

## <a name="direct3d-9ex"></a>Direct3D 9Ex

Die Direct3D 9Ex-Schnittstelle bietet Zugriff auf eine geringfügige Erweiterung der Direct3D 9-Standard-API, die die virtualisierte Ressourcenzuordnung, neue semantische Daten verloren gegangener Geräte und einige andere neue Features verfügbar macht, die während der Ausführung auf Windows Vista verfügbar sind. Durch das Erstellen dieses erweiterten Objekts verwendet die Direct3D 9-API die neue Semantik und erfordert daher, dass die Anwendung unterschiedliche Logik (und somit unterschiedliche Codepfade) für die Erstellung, Verwaltung und Fehlerbehandlung von Ressourcen für neue Arten von Bedingungen verwendet. Diese API ist nur auf Windows Vista verfügbar und erfordert WDDM-Treiber. Da Direct3D 9Ex einen separaten API- und Treibercodepfad als Direct3D 9 verwendet, erfordert die Unterstützung dieser API zusätzliche Testfälle für Ihre Anwendung.

Der Hauptgrund für die Erstellung der neuen Direct3D 9Ex-API bestand darin, vollzugriff auf die neuen Funktionen von WDDM zu ermöglichen und gleichzeitig die Kompatibilität für vorhandene Direct3D-Anwendungen aufrechtzuerhalten. Der neue 3D-Desktop und viele Windows Vista-spezifischen Anwendungen nutzen diese Version von Direct3D 9, sind aber nicht funktionsfähig, wenn sie auf älteren XPDM-Treibern ausgeführt werden. Da die Direct3D 9Ex-API aufgrund fehlender Unterstützung für das WDDM nie in älteren Versionen von Windows angezeigt wird, decken die Direct3D 9-Standardschnittstellen eine viel größere Gruppe von Systemen ab. Für Hochleistungsanwendungen, die die nächste Generation von Videohardware nutzen können, bietet die vollständig neue Version 10 von Direct3D viele neue Funktionen, die nicht von Direct3D 9Ex verfügbar gemacht werden. Daher ist Direct3D 9 oder Direct3D 10 für Spiele und die meisten anderen Anwendungen die empfohlene API.

> [!Note]  
> Das DirectX SDK stellt keine Beispiele, Header oder Bibliotheken für die Direct3D 9Ex-Schnittstelle bereit. Die MSDN Library und Windows SDK (früher als Plattform-SDK bezeichnet) enthalten die verfügbaren Dokumentationen, Header und Bibliotheken.

 

Weitere Informationen zu Direct3D 9Ex finden Sie unter [DirectX für Windows Vista](/previous-versions//ms681824(v=vs.85)) unter MDSN.

## <a name="direct3d-10"></a>Direct3D 10

Um das Potenzial des neuen Windows Vista-Treibermodells und der Hardware der nächsten Generation vollständig zu nutzen, wurde eine völlig neue Version der Direct3D-API erstellt. Während WDDM einige der Leistungseinschränkungen im vorhandenen Grafiksystem beseitigt, geht Direct3D 10 noch weiter, indem Entwurfsengpässe in der vorhandenen Direct3D-API beseitigt werden, und vereinfacht die Programmierung der GPU erheblich.

Die neue API entfernt alle aspekte mit einigen festen Funktionen vollständig, ersetzt sie durch programmierbare Konstrukte und rationalisierungiert die interne Implementierung erheblich. Die Hunderte von Funktionsbits in früheren Versionen von Direct3D wurden vollständig entfernt und durch einen klar definierten, inklusiven Satz von Funktionen ersetzt, der nur wenige optionale Verwendungsszenarien für bestimmte Ressourcenformate aufweist. Die CPU-intensive Ressourcenerstellung und -überprüfung weist jetzt eine explizite Semantik in der neuen API auf. Dies ermöglicht ein deutlich besser vorhersagbares Leistungsverhalten und reduziert den Mehraufwand pro Zeichnen erheblich. Ressourcen können in mehreren Formen neu konfiguriert werden, um eine effiziente Verwendung in verschiedenen Phasen zu ermöglichen, und der Featuresatz erzwingt deutlich weniger Einschränkungen für Verwendungsszenarien für Formate. Es gibt auch neue blockkomprimierte Normalmaptexturformate.

In der neuen API sind Shaderkonstanten und der Gerätezustand explizite Ressourcen, die eine wesentlich effizientere Zwischenspeicherung auf der Hardware und eine erheblich vereinfachte Treibervalidierung ermöglichen. Das programmierbare Shadermodell wurde sowohl für Vertex- als auch für Pixel-Shader vereinheitlicht und mit einem klar definierten Berechnungsmodell und Operatorsatz ausdrucksstärker. Darüber hinaus wurde eine neue Geometrie-Shader-Stufe hinzugefügt, um nach der Vertex-Shader-Stufe mit Primitiven zu arbeiten. Die Ergebnisse der GPU-Arbeit in den Scheitelpunkt- und Geometrie-Shaderstufen der Pipeline können zur Wiederverwendung an den Video-RAM gestreamt werden, was die Möglichkeit extrem komplexer GPU-Vorgänge mit mehreren Durchgängen mit minimaler CPU-Interaktion ermöglicht.

Alle diese Erweiterungen ermöglichen die Grafiktechnologie der nächsten Generation und erweitern die Fähigkeit von Anwendungen, Arbeitslasten auf die GPU zu deaktivieren. Die Auslagerung ermöglicht komplexeres GPU-basiertes Zeichenskinning, beschleunigte Morphingtechniken, Schattenvolumengenerierung und -extrusion, Partikel- und Physikalische Systeme, die vollständig GPU-basiert sind, komplexere Materialien, kombiniert in effizienten Batches mit umfangreichem Zeichnen, prozedurale Details, Echtzeit-Ray-Traced-Verschiebungszuordnung, Singlepass-Cube-Map-Generierung und viele weitere Techniken – und das alles, während CPU-Ressourcen für komplexere Anwendungen freigegeben werden.

Um diesen Innovationsgrad in Direct3D 10 bereitzustellen, kann ältere Hardware nicht als teilimplementierte neue Schnittstelle ausgedrückt werden. Eine Grafikkarte kann entweder alle neuen Features unterstützen, oder sie ist keine Direct3D 10-fähige Karte. Während Direct3D 9 Hardware aus der DirectX7-Zeit mit vielen fehlenden Funktionsbits und Nutzungseinschränkungen steuern könnte, funktioniert Direct3D 10 nur für eine neue Generation von Grafikkarten. Damit eine Anwendung ältere Videohardware unterstützt, muss sie auch die Direct3D 9-Schnittstellen unterstützen. Zukünftige Versionen von Direct3D bauen auf Version 10 auf und erweitern sie auf neue Versionen der API und stellen gleichzeitig eine strikte Obermenge der Direct3D 10-Funktionalität sicher.

Weitere Informationen zu Direct3D 10 finden Sie unter [Direct3D 10.](/windows/desktop/direct3d10/d3d10-graphics)

## <a name="direct3d-101"></a>Direct3D 10.1

Windows Vista Service Pack 1 erweitert die Direct3D 10-API um Direct3D 10.1, wodurch optionale Schnittstellen und ein zusätzliches Shadermodell hinzugefügt werden, um neue Hardwarefeatures von Grafikkarten zu unterstützen, die Direct3D 10.1 unterstützen. Alle Hardwarekomponenten, die Direct3D 10.1 unterstützen können, unterstützen auch alle Features von Direct3D 10 vollständig, und Spieleentwickler können die zusätzlichen Features von Direct3D 10.1 nutzen, sofern verfügbar.

> [!Note]  
> Direct3D 10.1 ist die Grafik-API, die vom desktop Windows 7 verwendet wird.

 

> [!Note]  
> Windows 7 und das Update für Windows Vista ([KB 971644](https://support.microsoft.com/kb/971644)) fügen der vorhandenen Direct3D 10.1-API Unterstützung für DXGI 1.1, 10level9-Featureebenen und das WARP10-Gerät hinzu.

 

## <a name="direct3d-11"></a>Direct3D 11

Windows 7 unterstützt eine neue Revision von Direct3D, Direct3D 11, die auf dem Entwurf der Direct3D 10.1-API basiert. Zu den neuen Features der API gehören Multithreadring und Ressourcenerstellung, Compute-Shader, Unterstützung für 10level9-Featureebenen und das WARP10-Softwarerenderinggerät sowie neue Hardwarefeatures der Direct3D 11-Klasse, z.B. Mosaik mit Hüllen & Domänen-Shadern, BC6H- und BC7-Texturkomprimierungsformate, Shadermodell 5.0 und Dynamische Shaderverknüpfung. Die neue API kann vorhandene Direct3D 10- und 10.1-Klassenvideokarten, einige Direct3D 9-Karten über die 10level9-Featureebenen mit eingeschränkter Featureunterstützung und die neuesten Direct3D 11-Klassenvideokarten verwenden.

Zusätzlich zur Direct3D 11-API umfasst Windows 7 DXGI 1.1, Direct2D, DirectWrite und Unterstützung für WDDM 1.1-Treiber.

> [!Note]  
> Direct3D 11 und zugehörige APIs sind auch als Update für Windows Vista verfügbar (siehe [KB 971644](https://support.microsoft.com/kb/971644)).

 

## <a name="direct3d-111"></a>Direct3D 11.1

Windows 8 erweitert die [Direct3D 11-API](#direct3d-11) um Direct3D 11.1. Direct3D 11.1 unterstützt alle vorhandenen Hardwarekomponenten, die die [Features der Ebenen](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11, 10 x und \_ 9 x \_ unterstützen, sowie eine neue \_ 11 1-Featureebene.

Zusätzlich zur [Direct3D 11.1-API](/windows/desktop/direct3d11/direct3d-11-1-features)umfasst Windows 8 [DXGI 1.2,](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements) [Direct2D-Gerätekontexte](/windows/desktop/Direct2D/devices-and-device-contexts)und Unterstützung für WDDM 1.2-Treiber.

> [!Note]  
> Wenn Sie möchten, dass Ihre Windows Store-Apps 3D-Grafiken mit DirectX programmieren, können Sie die Direct3D 11.1-API verwenden. Weitere Informationen zum Programmieren von 3D-Grafiken mit DirectX finden Sie unter [Einführung in 3D-Grafiken mit DirectX.](/previous-versions/windows/apps/hh465137(v=win.10))

 

**Plattformupdate für Windows 7:** Teilunterstützung ist für die [Direct3D 11.1-API](/windows/desktop/direct3d11/direct3d-11-1-features) auf Windows 7 oder Windows Server 2008 R2 mit installiertem [Plattformupdate für Windows 7](https://support.microsoft.com/kb/2670838) verfügbar. Weitere Informationen zum Plattformupdate für Windows 7 finden Sie unter [Plattformupdate für Windows 7.](platform-update-for-windows-7.md)

## <a name="opengl"></a>Opengl

Windows Vista, Windows 7 und Windows 8 bieten die gleiche Unterstützung wie Windows XP für OpenGL, wodurch Hersteller von Grafikkarten einen installierbaren Clienttreiber (ICD) für OpenGL bereitstellen können, der hardwarebeschleunigte Unterstützung bietet. Beachten Sie, dass neuere Versionen solcher ICDs erforderlich sind, um Windows Vista, Windows 7 oder Windows 8. Wenn keine ICD installiert ist, wird das System in den meisten Fällen auf die OpenGL v1.1-Softwareebene zurückfallen.

## <a name="application-compatibility-gdi-and-older-versions-of-direct3d"></a>Anwendungskompatibilität, GDI und ältere Versionen von Direct3D

Die Windows Vista-, Windows 7- und Windows 8-Grafiksysteme sind so konzipiert, dass sie eine Vielzahl von Hardware- und Verwendungsszenarien unterstützen, um neue Technologien zu ermöglichen und gleichzeitig weiterhin vorhandene Systeme zu unterstützen. Vorhandene Grafikschnittstellen wie GDI, GDI+ und ältere Versionen von Direct3D funktionieren weiterhin unter Windows Vista und Windows 7, werden aber nach Möglichkeit intern neu zugeordnet. Dies bedeutet, dass die meisten Windows weiterhin funktionieren.

Windows Vista, Windows 7 und Windows 8 unterstützen weiterhin die gleichen Direct3D- und DirectDraw-Schnittstellen wie Windows XP, zurück zu Version 3 von DirectX (mit Ausnahme des beibehaltenen Modus von Direct3D, der entfernt wurde). Wie bei Windows XP Professional x64 Edition sind native 64-Bit-Anwendungen in neueren Versionen von Windows auf Direct3D9, DirectDraw7 oder neuere Schnittstellen beschränkt. Hochleistungsanwendungen sollten Direct3D 9 oder höher verwenden, um sicherzustellen, dass sie den Hardwarefunktionen am nächsten sind.

## <a name="recommendations"></a>Empfehlungen

Berücksichtigen Sie beim Auswählen einer API für Ihre grafische Anwendung die folgenden Empfehlungen:

-   Verwenden Sie Direct3D 9, wenn Ihre Anwendung Windows XP oder eine frühere Version von Windows.
-   Verwenden Sie Direct3D 9, wenn Sie Windows Vista oder Windows 7 mit XPDM-Treibern unterstützen möchten. Für Windows Vista- oder Windows 7-Systeme ohne Direct3D 10 oder eine bessere Videohardware können Sie entweder den vorhandenen Windows XP Direct3D 9-Codepfad oder die Featureebenen 10level9 über die Direct3D 10.1- oder Direct3D 11-API verwenden.
-   Verwenden Sie Direct3D 11, um die Vorteile der nächsten Generation von Videohardware auf Windows Vista, Windows 7 und Windows 8. Windows Store Müssen Direct3D 11 oder höher verwenden.

 

 