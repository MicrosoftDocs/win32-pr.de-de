---
description: In diesem Thema werden allgemeine Kategorien von Problemen aufgeführt, die beim Schreiben von Direct3D-Anwendungen auftreten können, und wie sie verhindert werden können.
ms.assetid: 27b87f0f-7118-4252-b6e8-6ea18a9399e4
title: Problembehandlung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 637ac4b43e8947a6011e35ae9a36db7829ed47fd4d5740f93778116e4ee8f9ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044078"
---
# <a name="troubleshooting-direct3d-9"></a>Problembehandlung (Direct3D 9)

In diesem Thema werden allgemeine Kategorien von Problemen aufgeführt, die beim Schreiben von Direct3D-Anwendungen auftreten können, und wie sie verhindert werden können.

## <a name="device-creation"></a>Geräteerstellung

Wenn ihre Anwendung während der Geräteerstellung fehlschlägt, überprüfen Sie die folgenden allgemeinen Fehler.

-   Überprüfen Sie die Gerätefunktionen, insbesondere die Rendertiefe.
-   Untersuchen Sie den Fehlercode. D3DERR \_ OUTOFVIDEOMEMORY ist immer möglich.
-   Verwenden Sie die DlLs (Dynamic Link Libraries) zum Debuggen von DirectX, und überprüfen Sie ausgabemeldungen unter dem Debugger.

## <a name="using-lit-vertices"></a>Verwenden von Lit Vertices

Anwendungen, die leuchtete Scheitelpunkte verwenden, sollten die Direct3D-Beleuchtungs-Engine deaktivieren, indem sie den D3DRS \_ LIGHTING-Renderzustand auf **FALSE** festlegen. Wenn die Beleuchtung aktiviert ist, legt das System standardmäßig die Farbe für jeden Scheitelpunkt fest, der keinen normalen Vektor enthält, auf 0 (schwarz), auch wenn der Eingabevertex einen Farbwert ungleich 0 (null) enthielt. Da lit-vertices naturgemäß keine Scheitelpunktnorm normal enthalten, gehen alle an Direct3D übergebenen Farbinformationen während des Renderings verloren, wenn die Beleuchtungs-Engine aktiviert ist.

Natürlich ist die Scheitelpunktfarbe für jede Anwendung wichtig, die eine eigene Beleuchtung ausführt. Um zu verhindern, dass das System die Standardwerte erzwingt, stellen Sie sicher, dass Sie D3DRS \_ LIGHTING auf **FALSE** festlegen.

Wenn Ihre Anwendung ausgeführt wird, aber nichts sichtbar ist, überprüfen Sie die folgenden allgemeinen Fehler.

-   Stellen Sie sicher, dass Ihre Dreiecke nicht degeneriert sind.
-   Stellen Sie sicher, dass Ihre Dreiecke nicht culled werden.
-   Stellen Sie sicher, dass Ihre Transformationen intern konsistent sind.
-   Überprüfen Sie die Viewporteinstellungen, um sicherzustellen, dass ihre Dreiecke angezeigt werden können.

## <a name="debugging"></a>Debuggen

Das Debuggen einer Direct3D-Anwendung kann eine Herausforderung darstellen. Probieren Sie die folgenden Verfahren aus, zusätzlich zur Überprüfung aller Rückgabewerte. Dies ist ein besonders wichtiger Hinweis bei der Direct3D-Programmierung, die von sehr unterschiedlichen Hardwareimplementierungen abhängig ist.

-   Wechseln Sie zu Debug-DLLs.
-   Erzwingen Eines reinen Softwaregeräts, deaktivieren Sie die Hardwarebeschleunigung, auch wenn es verfügbar ist.
-   Erzwingen von Oberflächen in den Systemspeicher.
-   Erstellen Sie eine Option zum Ausführen in einem Fenster, damit Sie einen integrierten Debugger verwenden können.

Mit der zweiten und dritten Option in dieser Liste können Sie die Win16-Sperre vermeiden, die andernfalls dazu führen kann, dass Ihr Debugger hängt.

Versuchen Sie außerdem, die folgenden Einträge zu Win.ini hinzuzufügen.


```
[Direct3D] 
debug=3 
[DirectDraw] 
debug=3 
```



## <a name="borland-floating-point-initialization"></a>Borland Floating-Point Initialisierung

Compiler von Borland melden Gleitkomma-Ausnahmen auf eine Weise, die mit Direct3D nicht kompatibel ist. Um dieses Problem zu beheben, schließen Sie einen \_ matherr-Ausnahmehandler wie den folgenden ein:


```
// Borland floating point initialization 
#include <math.h>
#include <float.h>

void initfp(void)
{
    // Disable floating point exceptions
    _control87(MCW_EM,MCW_EM);
}

int _matherr(struct _exception  *e)
{
    e;               // Dummy reference to catch the warning
    return 1;        // Error has been handled
}
```



## <a name="parameter-validation"></a>Parameterüberprüfung

Aus Leistungsgründen führt die Debugversion der Direct3D Immediate Mode-Laufzeit mehr Parameterüberprüfungen aus als die Verkaufsversion, die manchmal überhaupt keine Validierung durchführt. Dadurch können Anwendungen ein robustes Debuggen mit der langsameren Debuglaufzeitkomponente durchführen, bevor die schnellere Verkaufsversion für die Leistungsoptimierung und endgültige Version verwendet wird.

Obwohl mehrere Methoden des direkten Direct3D-Modus Grenzwerte für die Werte festlegen, die sie akzeptieren können, werden diese Grenzwerte häufig nur von der Debugversion der Laufzeit des Direkten 3D-Direktmodus überprüft und erzwungen. Anwendungen müssen diesen Grenzwerten entsprechen, oder unvorhersehbare und unerwünschte Ergebnisse können auftreten, wenn sie in der Verkaufsversion von Direct3D ausgeführt werden. Beispielsweise akzeptiert die [**IDirect3DDevice9::D rawPrimitive-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) einen Parameter (PrimitiveCount), der die Anzahl der Primitive angibt, die die Methode rendert. Die -Methode kann nur Werte zwischen 0 und D3DMAXNUMPRIMITIVES akzeptieren. Wenn Sie in der Debugversion von Direct3D mehr als D3DMAXNUMPRIMITIVES-Primitive übergeben, schlägt die Methode ordnungsgemäß fehl, gibt eine Fehlermeldung in das Fehlerprotokoll aus und gibt einen Fehlerwert an Ihre Anwendung zurück. Wenn Ihre Anwendung umgekehrt bei der Ausführung mit der Verkaufsversion der Laufzeit den gleichen Fehler aufweist, ist das Verhalten nicht definiert. Aus Leistungsgründen überprüft die Methode die Parameter nicht, was zu unvorhersehbaren und vollständig situationsbedingten Verhaltensweisen führt, wenn sie nicht gültig sind. In einigen Fällen kann der Aufruf funktionieren, in anderen Fällen kann dies zu einem Speicherfehler in Direct3D führen. Wenn ein ungültiger Aufruf konsistent mit einer bestimmten Hardwarekonfiguration und DirectX-Version funktioniert, gibt es keine Garantie dafür, dass er weiterhin auf anderer Hardware oder mit späteren Versionen von DirectX funktioniert.

Wenn ihre Anwendung bei der Ausführung mit der Retail Direct3D-Laufzeitdatei auf unerklärliche Fehler stößt, testen Sie die Debugversion, und suchen Sie genau nach Fällen, in denen Ihre Anwendung ungültige Parameter übergibt. Verwenden Sie das DirectX-Systemsteuerungs-Applet, wechseln Sie bei Bedarf zur Debugruntime, und aktivieren Sie die Option "Bei D3DError unterbrechen". Diese Option zwingt die Runtime, die Windows DebugBreak-Methode zu verwenden, um zu erzwingen, dass die Anwendung beendet wird, wenn ein Anwendungsfehler erkannt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieren Tipps](programming-tips.md)
</dt> </dl>

 

 
