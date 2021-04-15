---
description: FAQ zu DirectShow
ms.assetid: 198758b9-025a-44af-958c-9ddea8cbb12d
title: FAQ zu DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7d0959c4abb24509edd9c26d111e80a5af221d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521795"
---
# <a name="directshow-faq"></a>FAQ zu DirectShow

In diesem Artikel werden viele häufig gestellte Fragen zu Microsoft DirectShow beantwortet.

**Welche Betriebssysteme werden von DirectShow unterstützt?**

DirectShow ist in allen unterstützten Versionen von Windows verfügbar.

**Wie viel com-wissen muss ich mit DirectShow programmieren?**

Für die Anwendungsentwicklung müssen Sie die Grundlagen der Arbeit mit COM-Objekten verstehen: wie instanziieren Sie, greifen Sie auf die von Ihnen verfügbar gemachten Schnittstellen zu, und verwalten Sie Verweis Zähler für diese Schnittstellen. Die Filter Entwicklung erfordert mehr com-wissen.

**Welche Formate werden von DirectShow unterstützt?**

Siehe [Unterstützte Formate in DirectShow](supported-formats-in-directshow.md).

**Gibt es eine DirectShow-Hardware Kompatibilitätsliste (HCL)?**

Nein. In DirectShow werden die Hardwarefunktionen von Microsoft DirectDraw und Microsoft DirectSound verwendet, sofern diese verfügbar sind. Wenn keine spezielle Hardware verfügbar ist, verwendet DirectShow GDI zum Zeichnen von Video-und **waveout** \* -Multimedia-APIs zur Wiedergabe von Audiodaten.

**Welche Sprachen kann ich verwenden, um eine DirectShow-Anwendung zu schreiben?**

DirectShow ist hauptsächlich für die C++-Entwicklung konzipiert. Eine kleine Teilmenge der DirectShow-API wird durch Visual Basic 6,0 verfügbar gemacht; Diese Funktion ist jedoch veraltet.

**Ist DirectShow immer über verwalteten Code zugänglich?**

Microsoft hat keine aktuellen Pläne, eine verwaltete DirectShow-API zu implementieren.

**Welchen Compiler benötige ich für die DirectShow-Entwicklung?**

Alle Compiler, die Component Object Model (com)-Objekte erstellen können, sollten funktionieren, wenn die Umgebung des Compilers ordnungsgemäß konfiguriert wurde.

**Wie verhält sich DirectShow mit Microsoft DirectX?**

Intern verwendet DirectShow DirectSound und DirectDraw, wenn dies von der Hardware unterstützt wird. Der Videorenderer und die Überlagerungs Filter Filter verwenden DirectDraw 3 und DirectDraw 5-Oberflächen. Der Video Mischungs-Renderer 7 (nur Windows XP) verwendet DirectDraw 7-Oberflächen. Der Video Mischungs-Renderer 9 und der erweiterte Videorenderer verwenden die neuesten Microsoft Direct3D-APIs. Sie müssen nicht die anderen DirectX-APIs verwenden, um eine DirectShow-Anwendung zu schreiben, obwohl es möglich ist, diese zu kombinieren.

**Wie verhält sich DirectShow mit Microsoft ActiveMovie?**

ActiveMovie war der ursprüngliche Name für DirectShow. Der Begriff "ActiveMovie" wird nicht mehr verwendet.

**Ist der Quellcode für das Hilfsprogramm "GraphEdit" verfügbar? Kann GraphEdit neu verteilt werden?**

Nein, die Quelle ist nicht verfügbar, und Graphedt.exe ist nicht Verteil Bar.

**Ersetzen DMOS DirectShow-Filter?**

Microsoft DirectX Media Objects (DMOs) kann in einer DirectShow-Anwendung verwendet werden. Bei Encodern, Decodern und Effekten wird empfohlen, einen DMO anstelle eines DirectShow-Filters zu schreiben. (Hinweis: Wenn Sie die DirectX-Video Beschleunigung in Ihrem Decoder verwenden möchten, müssen Sie Sie als Filter implementieren.) Für andere Zwecke kann ein DirectShow-Filter besser geeignet sein. Weitere Informationen zu DMOS finden Sie unter [DirectX-Medienobjekte](directx-media-objects.md).

**Ich Spiele eine AVI-Format Datei mit Windows Media Player. Ich kann das Audiovideo hören, aber es scheint kein Video zu sein, sondern ich sehe nur schwarz. Was ist los?**

Wahrscheinlich wurde die Datei mit einem Codec codiert, der nicht auf Ihrem System vorhanden ist. Obwohl das AVI-Dateiformat Common ist, können AVI-Dateien mit vielen verschiedenen Komprimierungs Formaten (Codecs) erstellt werden. Wenn Sie versuchen, eine AVI-Datei wiederzugeben, die einen nicht unterstützten Codec verwendet, werden Sie möglicherweise die Audiokomponente hören, aber das Video wird als schwarzer Bildschirm angezeigt, oder die Bildschirminhalte bleiben unverändert.

> [!Note]  
> Windows Media Player versucht häufig, einen Codec herunterzuladen und zu installieren, wenn er nicht auf Ihrem System vorhanden ist.

 

**Gewusst wie meine Anwendung erstellen? Welche Bibliotheken und Header Dateien benötige ich?**

Weitere Informationen finden [Sie unter Einrichten der Buildumgebung](setting-up-the-build-environment.md).

**GraphEdit zeigt viele Filter an, die nicht dokumentiert sind. Was sind diese Filter?**

GraphEdit listet alle Filter auf, die auf Ihrem System in einer Filterkategorie registriert sind. Dies kann Filter enthalten, die von Drittanbieter Anwendungen installiert oder von anderen Microsoft-Technologien, wie z. b. Windows Media oder NetMeeting, installiert werden. Außerdem fungieren einige DirectShow-Filter als Wrapper für Codecs oder Hardware Geräte, wobei jeder Codec oder jedes Gerät als eindeutiger Filter angezeigt wird. Der Video-Codec von Microsoft H. 263 wird von NetMeeting verwendet und wird in DirectShow nicht mehr unterstützt. Weitere Informationen finden Sie unter Auflisten von [Geräten und Filtern](enumerating-devices-and-filters.md).

**Ich habe Probleme, das benutzerdefinierte Diagramm Programm gesteuert zu entwickeln.**

Versuchen Sie zunächst, das Filter Diagramm mit GraphEdit zu entwickeln. Mit diesem Tool können Sie schnell viele Möglichkeiten simulieren. GraphEdit ist immer ein guter Ausgangspunkt, um das Diagramm zu testen, bevor versucht wird, es mit Quellcode zu erstellen.

Weitere Informationen zur Diagramm Bildung finden Sie in den folgenden Artikeln:

-   [Aufbauen des Filter Diagramms](building-the-filter-graph.md)
-   [Auflisten von Objekten in einem Filter Diagramm](enumerating-objects-in-a-filter-graph.md)

**Wie kann ich erkennen, ob DirectShow auf einem bestimmten Computer installiert ist?**

Rufen Sie **cokreateinstance** auf, um eine Instanz des Filter Graph-Managers zu erstellen. Wenn dieser Vorgang erfolgreich ist, wird DirectShow auf dem Computer installiert. Dies wird im folgenden Code veranschaulicht:


```C++
IGraphBuilder *pGraph;

HRESULT hr = CoCreateInstance(CLSID_FilterGraph,
    NULL, CLSCTX_INPROC_SERVER,
    IID_IGraphBuilder, (void **) &pGraph);
```



**Gewusst wie die Einstellungen eines Filters ändern, ohne die Eigenschaften Seite anzuzeigen?**

Die meisten Filter machen eine oder mehrere Schnittstellen für das Festlegen von Eigenschaften für den Filter verfügbar. Weitere Informationen finden Sie auf der Referenzseite für den fraglichen Filter. (Siehe [DirectShow-Filter](directshow-filters.md).)

**Kann ich meinen Filter mit GraphEdit testen?**

Wenn Sie einen Filter entwickeln, kann GraphEdit Ihnen helfen, die Verbindungen zwischen den Filtern visuell darzustellen. Sie kann auch einen schnellen Test der Funktionalität eines Filters bereitstellen. Es ist jedoch nicht als stabile Testplattform gemeint.

**An welchem Berechtigungs Ring werden Filter ausgeführt?**

Filter werden in Ring 3 ausgeführt, obwohl einige Filter Streaminggeräte steuern, die mit Ring 0 ausgeführt werden. Weitere Informationen finden Sie unter [wie Hardware Geräte am Filter Diagramm teilnehmen](how-hardware-devices-participate-in-the-filter-graph.md).

**Muss ich einen Kernel Debugger verwenden?**

Das hängt von ihrem jeweiligen Projekt ab. Die Installation der DirectX-Debug-Laufzeitbibliotheken bedeutet, dass Sie debugtreiber und andere Kernelmoduskomponenten installieren. Wenn Ihre Anwendung in einer dieser Komponenten eine debuggingbestätigung auslöst, wird der Computer automatisch neu gestartet, es sei denn, Sie haben einen Kernel Debugger an den Prozess angefügt.

**Beim Ausführen der Anwendung im Debugger stürzt Sie ab.**

Einige Decoder sind so konzipiert, dass Sie nicht funktionieren, während die Anwendung an den Debugger angefügt wird. Versuchen Sie, die Anwendung außerhalb des Debuggers auszuführen.

**Wie \_ funktioniert das GUID-Makro definieren?**

Das **\_ GUID** -Makro definieren löst das Problem `extern` , dass Verweise auf GUID-Werte im Quellcode deklariert werden. Nehmen Sie beispielsweise an, dass das Projekt über drei Quelldateien verfügt: Quelle1. cpp, Quelle2. cpp und Src3. cpp, und alle drei Dateien verwenden einen bestimmten GUID-Wert, den Sie definiert haben. Der GUID-Wert muss im Projekt genau einmal definiert werden, und die anderen Quelldateien müssen `extern` Verweise darauf deklarieren. Mit dem **\_ GUID** -Makro definieren können Sie für beide Zwecke dieselbe Header Datei verwenden. Deklarieren Sie die GUID in der Header Datei wie folgt:


```C++
DEFINE_GUID(CLSID_MyObject, 
0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



(Wenn dieses Beispiel Nullen enthält, platzieren Sie die eigentlichen GUID-Werte.) Mit dem Guidgen.exe-Hilfsprogramm können Sie eine neue GUID erstellen und Sie in die Header Datei im **definierenden \_ GUID** -Format einfügen. Schließen Sie diese Header Datei in jede Quelldatei ein, die auf die GUID verweist. Fügen Sie in genau einer der Quelldateien die Header Datei Initguid. h vor der Header Datei ein. Beispiel:


```C++
// Src1.cpp
#include <initguid.h>
#include "MyGuids.h"

// Src2.cpp
#include "MyGuids.h"

// Src3.cpp
#include "MyGuids.h"
```



Wenn die Header Datei "Initguid. h" nicht eingeschlossen ist, erstellt das **\_ GUID** -Makro definieren einen `extern` Verweis auf den GUID-Wert. Wenn die Header Datei "Initguid. h" enthalten ist, wird das **definierende \_ GUID** -Makro neu definiert, sodass mit **define \_ GUID** eine definierende Deklaration der GUID erstellt wird.

Wenn Sie Initguid. h nicht in eine der Quelldateien einschließen, wird der Link Fehler "nicht aufgelöstes externes Symbol" angezeigt. Wenn Sie Initguid. h zweimal für dieselbe GUID einschließen, erhalten Sie den Kompilierungsfehler "Neudefinition; mehrfache Initialisierung. " Stellen Sie sicher, dass Initguid. h genau einmal enthalten ist, um diese Fehler zu beheben. Fügen Sie außerdem Initguid. h nicht in eine vorkompilierte Header Datei ein, da der vorkompilierte Header in jeder Quelldatei enthalten ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einführung in DirectShow](introduction-to-directshow.md)
</dt> </dl>

 

 



