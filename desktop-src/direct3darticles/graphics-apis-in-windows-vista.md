---
title: Grafik-APIs in Windows
description: In diesem Artikel werden Windows-Grafik Features und-APIs behandelt.
ms.assetid: 54cd5027-cdcf-fc4a-40a9-beacfaa08681
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7543ee7c5e3cdbfb022cc9299dd5ddd3cdd36981
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390867"
---
# <a name="graphics-apis-in-windows"></a>Grafik-APIs in Windows

Windows Vista bietet Unterstützung für ein völlig neues Anzeigetreiber Modell, das seit der Einführung des Windows-Treibermodell (WDM) für Windows 98 eine wesentliche Überarbeitung des Entwurfs von Video Treibern darstellt. Dieses neu gestaltete Modell spiegelt die Entwicklung von Video Hardware aus der Welt von 2D-Raster Vorgängen und GDI-Anwendungen zu der 3D-Spiele mit fester Funktions Grafikhardware und schließlich zu der modernen programmierbaren Grafikverarbeitungseinheit (GPU), die eine große Bandbreite an hochleistungsfähigen Grafikanwendungen unterstützt. Windows 7 und Windows 8 bauen auf der Windows Vista-Grafik Infrastruktur auf, indem Sie zusätzliche Grafik Features und APIs bereitstellen. In diesem Artikel werden Windows-Grafik Features und-APIs behandelt.

-   [Hintergrund](#background)
-   [Direct3D 9](#direct3d-9)
-   [Direct3D 9Ex](#direct3d-9ex)
-   [Direct3D 10](#direct3d-10)
-   [Direct3D 10,1](#direct3d-101)
-   [Direct3D 11](#direct3d-11)
-   [Direct3D 11,1](#direct3d-111)
-   [OpenGL](#opengl)
-   [Anwendungs Kompatibilität, GDI und ältere Versionen von Direct3D](#application-compatibility-gdi-and-older-versions-of-direct3d)
-   [Empfehlungen](#recommendations)

## <a name="background"></a>Hintergrund

Die primäre API für das Programmieren von Grafiken seit den frühen Tagen von Windows ist die grafische Geräteschnittstelle (Graphics Device Interface, GDI). Diese API wurde für die Verarbeitung zahlreicher 2D-Ausgabegeräte entwickelt und ist die Grundlage für die Benutzeroberfläche der Windows-Benutzeroberfläche. DirectDraw und Direct3D wurden als Alternative APIs eingeführt, um voll Bild Spiele und 3D-Rendering als Erweiterungen der vorhandenen Hardware der Zeit zu unterstützen. Interaktionen mit GDI waren kompliziert. Die effektive Interaktion von herkömmlichen GDI-Elementen mit Direct3D Elementen wurde durch diesen Entwurf eingeschränkt. Die Windows XP-Version von WDM, die als XPDM bezeichnet wird, spiegelt die parallele Natur von GDI und Direct3D wider (siehe Abbildung 1).

**Abbildung 1. Grafik-APIs in Windows XP**

![XPDM](images/graphics-apis-in-windows-xp.gif)

Im Laufe der Jahre hat sich die Leistung von 3D-Grafikkarten erheblich bis zu dem Punkt vergrößert, an dem die große Mehrzahl der Hardware für diese Funktion vorgesehen ist. Ein neues Treibermodell, Windows Display Driver Model (WDDM), bringt die GPU und Direct3D in den Vordergrund und ermöglicht so die Erstellung einer völlig neuen Umgebung, des 3D-Desktops, der die 2D-Welt von GDI nahtlos mit der Leistungsfähigkeit moderner programmierbarer GPUs verbindet. Mit WDDM wird die Video Hardware vollständig von Direct3D gesteuert, und alle anderen Grafik Schnittstellen kommunizieren mit der Video Hardware über das neue Direct3D – zentrierte Treibermodell (siehe Abbildung 2).

**Abbildung 2. Grafik-APIs in Windows Vista**

![WDDM](images/graphics-apis-in-windows-vista.gif)

Weitere Informationen zu WDDM finden Sie im [Entwurfs Handbuch für Windows Vista-Anzeigetreiber Modell (WDDM)](/windows-hardware/drivers/display/windows-vista-display-driver-model-design-guide) auf MSDN.

## <a name="direct3d-9"></a>Direct3D 9

Version 9 von DirectX wurde erstmals für Windows in 2002 veröffentlicht, mit nachfolgenden Updates in 2003 und 2004. Diese API stellt eine jahrzehntelange Entwicklung der DirectX-Technologien dar, die Einführung von leistungsfähigeren shaderprogrammierungs Modellen für Direct3D und eine Reife, die von Tausenden von Liefer Titeln unterstützt wird. Direct3D 9 ist die primäre Grafikschnittstelle in Windows Vista. Es bleibt die ideale API, um 3D-Spiele und-Anwendungen zu schreiben, die auf der breiten Palette vorhandener Hardware-und Windows-Versionen ausgeführt werden müssen. Die Details des neuen Treiber Modells werden in Anwendungen mit den Direct3D 9-Schnittstellen ausgeblendet, aber im Hintergrund nutzt das Betriebssystem die neuen Funktionen, um ein echtes Multitasking der GPU, effizientere Ressourcenverwaltung und stabile Leistung zu bieten.

Um die vollständige Kompatibilität mit älteren Versionen von Windows sicherzustellen, müssen einige Quiri des alten Treiber Modells auch mit dem neuen Windows Vista-Anzeigetreiber Modell emuliert werden. Wenn eine Vollbildanwendung z. b. den Fokus verliert, muss Sie davon ausgehen, dass Sie alle Ressourcen im Videospeicher (VRAM) verloren hat und Sie als nicht verwaltete Ressourcen neu laden, auch wenn das neue Treibermodell die Ressourcen transparent verarbeitet, ohne Sie aus dem Gerätekontext zu löschen. Auch das Konzept eines verwalteten oder standardmäßigen Ressourcentyps ist spezifisch für das alte Treibermodell. Ein weiteres Beispiel ist die Annahme von Fehlern beim Zuordnen nicht verwalteter Ressourcen (Standard Pool Ressourcen), die über den verfügbaren VRAM hinausgehen, obwohl das neue Treibermodell eine nahezu unbegrenzte Menge an virtuellem Videospeicher bereitstellen kann. Aufgrund dieser Anforderungen erhalten Direct3D-Anwendungen, die unter Windows Vista ausgeführt werden, weiterhin diese Fehlerbedingungen. Daher sind Sie in der Lage, die grundlegenden Direct3D 9-Schnittstellen zu verwenden, um einige Features des neuen Treiber Modells vollständig zu nutzen.

Während neue Systeme, die mit Windows Vista ausgeliefert werden, Videokarten mit WDDM-Treibern enthalten, und neue Treiber für eine Reihe beliebter Grafikkarten enthalten sind, unterstützt Windows Vista weiterhin die Möglichkeit, ältere XPDM-Treiber für Upgrades und Unternehmens Editionen zu verwenden. Auf Systemen mit dem alten Treibermodell müssen Direct3D 9 und ältere Schnittstellen verwendet werden, und der Betrieb des Grafik Systems ähnelt der von Windows XP (Abbildung 1). WDDM ist erforderlich, damit Anwendungen Direct3D 9Ex, Direct3D 10 und höhere Versionen verwenden können.

## <a name="direct3d-9ex"></a>Direct3D 9Ex

Die Direct3D 9Ex-Schnittstelle bietet Zugriff auf eine geringfügige Erweiterung der Standard-Direct3D 9-API, die die virtualisierte Ressourcen Zuordnung, die neue verlorene Geräte Semantik und einige andere neue Features verfügbar macht, die bei der Ausführung unter Windows Vista verfügbar sind. Durch das Erstellen dieses erweiterten Objekts verwendet die Direct3D 9-API die neue Semantik und erfordert daher, dass die Anwendung unterschiedliche Logik (und somit unterschiedliche Codepfade) für die Erstellung, Verwaltung und Fehlerbehandlung von Ressourcen für neue Arten von Bedingungen verwendet. Diese API ist nur unter Windows Vista verfügbar und erfordert WDDM-Treiber. Da Direct3D 9Ex einen separaten API-und Treiber Codepfad als Direct3D 9 verwendet, erfordert die Unterstützung dieser API zusätzliche Testfälle für Ihre Anwendung.

Der Hauptgrund für die Erstellung der neuen Direct3D 9Ex-API bestand darin, den vollständigen Zugriff auf die neuen Funktionen von WDDM zu ermöglichen und gleichzeitig die Kompatibilität für vorhandene Direct3D-Anwendungen aufrechtzuerhalten. Der neue 3D-Desktop und viele Windows Vista-spezifische Anwendungen verwenden diese Version von Direct3D 9, Sie sind jedoch nicht funktionsfähig, wenn Sie für ältere XPDM-Treiber ausgeführt werden. Da die Direct3D 9Ex-API in älteren Versionen von Windows aufgrund fehlender Unterstützung für WDDM nie angezeigt wird, decken die standardmäßigen Direct3D 9-Schnittstellen eine viel umfassendere Gruppe von Systemen ab. Bei hochleistungsfähigen Anwendungen, die die nächste Generation von Video Hardware nutzen können, bietet die vollständige neue Version 10 von Direct3D viele neue Funktionen, die von Direct3D 9Ex nicht verfügbar gemacht werden. Daher ist Direct3D 9 oder Direct3D 10 die empfohlene API für Spiele und die meisten anderen Anwendungen.

> [!Note]  
> Das DirectX SDK stellt keine Beispiele, Header oder Bibliotheken für die Direct3D 9Ex-Schnittstelle bereit. Die MSDN Library und Windows SDK (ehemals Platform SDK) enthalten die verfügbare Dokumentation, Header und Bibliotheken.

 

Weitere Informationen zu Direct3D 9Ex finden Sie unter [DirectX for Windows Vista](/previous-versions//ms681824(v=vs.85)) on MDSN.

## <a name="direct3d-10"></a>Direct3D 10

Um das Potenzial des neuen Windows Vista-Treiber Modells und der Hardware der nächsten Generation voll ausschöpfen zu können, wurde eine völlig neue Version der Direct3D-API erstellt. Während WDDM einige der Einschränkungen hinsichtlich der Leistung im vorhandenen Grafiksystem beseitigt, geht Direct3D 10 weiter, indem Entwurfs Engpässe in der vorhandenen Direct3D-API entfernt werden und die Aufgabe der Programmierung der GPU erheblich vereinfacht wird.

Mit der neuen API werden alle außer einigen wenigen Funktionen mit fester Funktionsweise vollständig eliminiert, die durch programmierbare Konstrukte ersetzt und die interne Implementierung erheblich optimiert werden. Die Hunderte von Funktions Bits in früheren Versionen von Direct3D wurden vollständig eliminiert und durch einen klar definierten, inklusiven Satz von Funktionen ersetzt, die nur einige wenige optionale Verwendungs Szenarien für bestimmte Ressourcen Formate aufweisen. Die CPU-intensive Ressourcen Erstellung und-Validierung verfügen jetzt über eine explizite Semantik in der neuen API. Dies ermöglicht ein wesentlich vorhersagbares Leistungsverhalten und reduziert den pro-zeichnen-Aufwand erheblich. Ressourcen können in mehreren Formularen neu konfiguriert werden, um eine effiziente Verwendung in verschiedenen Phasen zu ermöglichen, und die Funktionsgruppe setzt weitaus weniger Einschränkungen für Verwendungs Szenarien für Formate mit sich. Es gibt auch neue, Block komprimierte Textur Formate für normale Karten.

In der neuen API sind shaderkonstanten und Gerätestatus explizite Ressourcen, die eine viel effizientere Zwischenspeicherung auf der Hardware und eine stark vereinfachte Treiber Validierung ermöglichen. Das programmierbare Shadermodell wurde sowohl über Scheitelpunkt-als auch Pixel-Shader hinweg vereinheitlicht und wurde mit einem klar definierten Berechnungsmodell und Operator Satz ausdrucksstärker gestaltet. Außerdem wurde eine neue Geometry-Shader-Phase hinzugefügt, die nach der Vertex-Shader-Phase für primitive verwendet werden kann. Die Ergebnisse der GPU-Arbeit in den Scheitelpunkt-und Geometry-Shader-Phasen der Pipeline können zur Wiederverwendung an den Video-RAM gestreamt werden, sodass extrem komplexe Multipass-GPU-Vorgänge mit minimaler CPU-Interaktion möglich sind.

Alle diese Verbesserungen ermöglichen Grafik Technologien der nächsten Generation und erweitern die Fähigkeit der Anwendungen, die Arbeit auf die GPU zu laden. Das Abladen ermöglicht eine komplexere GPU-basierte Zeichen Pflege, beschleunigte morphungs Techniken, Schatten Volume Generierung und-Verschlüsselung, Partikel-und Physik Systeme, bei denen es sich um vollständig GPU-basierte, komplexere Materialien handelt, die in effiziente große Mengen von Batches, ausführlichere Prozeduren, die Echtzeitverfolgung von Ray-Tracing-Verschiebungen, das Generieren von Single-Pass-cubezuordnungen und viele weitere Techniken kombiniert sind, d.

Um dieses Maß an Innovation in Direct3D 10 bereitzustellen, kann ältere Hardware nicht als partielle Implementierung einer neuen Schnittstelle ausgedrückt werden. Eine Grafikkarte ist entweder in der Lage, alle neuen Funktionen zu unterstützen, oder es handelt sich nicht um eine Direct3D 10 – fähige Karte. Obwohl Direct3D 9 DirectX7-ERA-Hardware mit vielen fehlenden Funktions Bits und Nutzungsbeschränkungen Steuern könnte, kann Direct3D 10 nur auf einer neuen Generation von Grafikkarten verwendet werden. Damit eine Anwendung ältere Video Hardware unterstützt, muss Sie auch die Direct3D 9-Schnittstellen unterstützen. Zukünftige Versionen von Direct3D bauen auf Version 10 auf, um Sie auf neue Versionen der API auszuweiten, während gleichzeitig eine strikte supermenge der Funktionen von Direct3D 10 sichergestellt wird.

Weitere Informationen zu Direct3D 10 finden Sie unter [Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics).

## <a name="direct3d-101"></a>Direct3D 10,1

Windows Vista Service Pack 1 erweitert die Direct3D 10-API mit Direct3D 10,1, wodurch optionale Schnittstellen und ein zusätzliches Shadermodell hinzugefügt werden, um neue Hardware Features von Videokarten zu unterstützen, die Direct3D 10,1 unterstützen. Alle Hardware, die Direct3D 10,1 unterstützen kann, unterstützt auch vollständig alle Features von Direct3D 10, und Spielentwickler können die zusätzlichen Features von Direct3D 10,1 nutzen, wenn diese verfügbar sind.

> [!Note]  
> Direct3D 10,1 ist die Grafik-API, die vom Windows 7-Desktop verwendet wird.

 

> [!Note]  
> Windows 7 und das Windows Vista-Update ([KB 971644](https://support.microsoft.com/kb/971644)) fügen Unterstützung für DXGI 1,1, 10level9-Funktionsebenen und das WARP10-Gerät der vorhandenen Direct3D 10,1-API hinzu.

 

## <a name="direct3d-11"></a>Direct3D 11

Windows 7 unterstützt eine neue Revision von Direct3D, Direct3D 11, die auf dem Entwurf der Direct3D 10,1-API basiert. Zu den neuen Funktionen der API zählen Multithread-Rendering und Ressourcen Erstellung, COMPUTE-Shader, Unterstützung für 10level9-Funktionsebenen und das WARP10-softwarrenderinggerät sowie neue Direct3D 11-Klassen Hardware Features wie Mosaik mithilfe von Hull & Domänen-Shader, BC6H-und bzw bc7-Textur Komprimierungs Formaten, Shadermodell 5,0 und dynamischer shaderverknüpfung Die neue API kann vorhandene Direct3D 10-und 10,1-Klassen-Grafikkarten, einige Direct3D 9-Karten über die 10level9-featureebenen mit eingeschränkter Funktions Unterstützung und die neuesten Generation Direct3D 11-Klassen Grafikkarten verwenden.

Zusätzlich zur Direct3D 11-API umfasst Windows 7 DXGI 1,1, Direct2D, DirectWrite und Unterstützung für WDDM 1,1-Treiber.

> [!Note]  
> Direct3D 11 und verwandte APIs sind auch als Update für Windows Vista verfügbar (siehe [KB 971644](https://support.microsoft.com/kb/971644)).

 

## <a name="direct3d-111"></a>Direct3D 11,1

Windows 8 erweitert die [Direct3D 11-API](#direct3d-11) mit Direct3D 11,1. Direct3D 11,1 unterstützt alle vorhandenen Hardware, die Unterstützung für die [Ebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11, 10 \_ x und 9 \_ x bietet, sowie eine neue \_ Funktionsebene von 11 1.

Zusätzlich zur [Direct3D 11,1-API](/windows/desktop/direct3d11/direct3d-11-1-features)enthält Windows 8 [DXGI 1,2](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements), Direct2D- [Geräte Kontexte](/windows/desktop/Direct2D/devices-and-device-contexts)und Unterstützung für WDDM 1,2-Treiber.

> [!Note]  
> Wenn Sie möchten, dass Ihre Windows Store-Apps 3D-Grafiken mit DirectX programmieren, können Sie die Direct3D 11,1-API verwenden. Weitere Informationen zum Programmieren von 3D-Grafiken mit DirectX finden [Sie unter Einführung in 3D-Grafiken mit DirectX](/previous-versions/windows/apps/hh465137(v=win.10)).

 

**Platt Form Update für Windows 7:** Teil Unterstützung steht für die [Direct3D 11,1-API](/windows/desktop/direct3d11/direct3d-11-1-features) unter Windows 7 oder Windows Server 2008 R2 mit installiertem [Platt Form Update für Windows 7](https://support.microsoft.com/kb/2670838) zur Verfügung. Weitere Informationen zum Platt Form Update für Windows 7 finden Sie unter [Platt Form Update für Windows 7](platform-update-for-windows-7.md).

## <a name="opengl"></a>OpenGL

Windows Vista, Windows 7 und Windows 8 bieten die gleiche Unterstützung wie Windows XP für OpenGL, mit dem Grafikkartenhersteller einen installierbaren Client Treiber (ICD) für OpenGL bereitstellen können, der hardwarebeschleunigte Unterstützung bietet. Beachten Sie, dass neuere Versionen dieser ICDs erforderlich sind, um Windows Vista, Windows 7 oder Windows 8 vollständig zu unterstützen. Wenn keine ICD installiert ist, greift das System in den meisten Fällen auf die OpenGL v 1.1-Software Schicht zurück.

## <a name="application-compatibility-gdi-and-older-versions-of-direct3d"></a>Anwendungs Kompatibilität, GDI und ältere Versionen von Direct3D

Die Grafik Systeme Windows Vista, Windows 7 und Windows 8 sind darauf ausgelegt, eine große Bandbreite an Hardware-und Verwendungs Szenarien zu unterstützen, um neue Technologien zu ermöglichen und vorhandene Systeme weiterhin zu unterstützen. Vorhandene Grafik Schnittstellen, wie z. b. GDI, GDI+ und ältere Versionen von Direct3D, funktionieren weiterhin unter Windows Vista und Windows 7, werden jedoch nach Möglichkeit intern neu zugeordnet. Dies bedeutet, dass die Mehrzahl vorhandener Windows-Anwendungen weiterhin funktionieren wird.

Windows Vista, Windows 7 und Windows 8 unterstützen weiterhin dieselben Direct3D-und DirectDraw-Schnittstellen wie Windows XP, zurück zu Version 3 von DirectX (mit Ausnahme des beibehaltenen Modus Direct3D's, der entfernt wurde). Ebenso wie bei Windows XP Professional x64 Edition sind systemeigene 64-Bit-Anwendungen auf neueren Versionen von Windows auf von Direct3D9, DirectDraw7 oder neuere Schnittstellen beschränkt. Hochleistungsanwendungen sollten Direct3D 9 oder höher verwenden, um sicherzustellen, dass Sie den Hardwarefunktionen am ehesten entsprechen.

## <a name="recommendations"></a>Empfehlungen

Beachten Sie bei der Auswahl einer API für Ihre grafische Anwendung die folgenden Empfehlungen:

-   Verwenden Sie Direct3D 9, wenn Ihre Anwendung Windows XP oder eine frühere Version von Windows unterstützen muss.
-   Verwenden Sie Direct3D 9, wenn Sie Windows Vista oder Windows 7 unterstützen möchten, das mit XPDM-Treibern ausgeführt wird. Für Windows Vista-oder Windows 7-Systeme, bei denen keine Direct3D 10 oder bessere Video Hardware vorhanden ist, können Sie entweder den vorhandenen Windows XP Direct3D 9-Codepfad verwenden oder die featureebenen von 10level9 über die Direct3D 10,1-oder Direct3D 11-API verwenden.
-   Verwenden Sie Direct3D 11, um die nächste Generation von Video Hardware unter Windows Vista, Windows 7 und Windows 8 zu nutzen. Für Windows Store-Apps muss Direct3D 11 oder höher verwendet werden.

 

 