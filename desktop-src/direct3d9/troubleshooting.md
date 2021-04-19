---
description: In diesem Thema werden allgemeine Kategorien von Problemen aufgeführt, die beim Schreiben von Direct3D-Anwendungen auftreten können, und wie Sie verhindert werden.
ms.assetid: 27b87f0f-7118-4252-b6e8-6ea18a9399e4
title: Problembehandlung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6726e761dd8c15e2da18e6c370472a73e82cef0b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342741"
---
# <a name="troubleshooting-direct3d-9"></a>Problembehandlung (Direct3D 9)

In diesem Thema werden allgemeine Kategorien von Problemen aufgeführt, die beim Schreiben von Direct3D-Anwendungen auftreten können, und wie Sie verhindert werden.

## <a name="device-creation"></a>Geräte Erstellung

Wenn die Anwendung während der Geräte Erstellung ausfällt, überprüfen Sie, ob die folgenden allgemeinen Fehler auftreten.

-   Stellen Sie sicher, dass Sie die Gerätefunktionen überprüfen, insbesondere die rendertiefe.
-   Überprüfen Sie den Fehlercode. D3DERR \_ outef videomemory ist immer möglich.
-   Verwenden Sie die Debuggen DirectX-DLLs (Dynamic-Link Libraries), und überprüfen Sie die Ausgabemeldungen unter dem Debugger.

## <a name="using-lit-vertices"></a>Verwenden von beleuchteten Vertices

Anwendungen, die beleuchtete Scheitel Punkte verwenden, sollten das Direct3D-Beleuchtungs Modul deaktivieren, indem Sie den D3DRS- \_ Beleuchtungs renderzustand auf **false** festlegen. Standardmäßig legt das System bei aktivierter Beleuchtung die Farbe für alle Scheitel Punkte, die keinen normalen Vektor enthalten, auf 0 (schwarz) fest, auch wenn der Eingabe Scheitelpunkt einen Farbwert ungleich 0 (null) enthielt. Da lit-Vertices nicht in ihrer Natur einen Scheitelpunkt normal enthalten, gehen alle an Direct3D über gebenden Farbinformationen beim Rendern verloren, wenn die Beleuchtungs-Engine aktiviert ist.

Natürlich ist die Scheitelpunkt Farbe für jede Anwendung wichtig, die ihre eigene Beleuchtung ausführt. Stellen Sie sicher, dass Sie D3DRS- \_ Beleuchtung auf **false** festlegen, um zu verhindern, dass das System die Standardwerte erzwingt.

Wenn die Anwendung ausgeführt wird, aber nichts angezeigt wird, überprüfen Sie, ob die folgenden allgemeinen Fehler auftreten.

-   Stellen Sie sicher, dass die Dreiecke nicht generiert werden.
-   Stellen Sie sicher, dass Ihre Dreiecke nicht in der Hand ist.
-   Stellen Sie sicher, dass ihre Transformationen intern konsistent sind.
-   Überprüfen Sie die viewporteinstellungen, um sicherzustellen, dass Ihre Dreiecke angezeigt wird.

## <a name="debugging"></a>Debuggen

Das Debuggen einer Direct3D-Anwendung kann schwierig sein. Testen Sie zusätzlich zum Überprüfen aller Rückgabewerte die folgenden Techniken: ein besonders wichtiger Ratgeber bei der Direct3D-Programmierung, der von sehr unterschiedlichen Hardware Implementierungen abhängig ist.

-   Wechseln Sie zu debugdlls.
-   Erzwingen eines reinen Software Geräts und Ausschalten der Hardwarebeschleunigung, auch wenn diese verfügbar ist.
-   Erzwingen von Oberflächen in den System Arbeitsspeicher.
-   Erstellen Sie eine Option, die in einem Fenster ausgeführt werden soll, damit Sie einen integrierten Debugger verwenden können.

Mithilfe der zweiten und dritten Optionen in dieser Liste können Sie die Win16-Sperre vermeiden, die andernfalls dazu führen kann, dass der Debugger nicht mehr reagiert.

Fügen Sie auch die folgenden Einträge zu Win.ini hinzu.


```
[Direct3D] 
debug=3 
[DirectDraw] 
debug=3 
```



## <a name="borland-floating-point-initialization"></a>Borland-Floating-Point Initialisierung

Compiler von Borland melden Gleit Komma Ausnahmen auf eine Weise, die mit Direct3D nicht kompatibel ist. Um dieses Problem zu beheben, schließen Sie einen \_ Matherr-Ausnahmehandler wie den folgenden ein:


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

Aus Leistungsgründen führt die Debugversion der Laufzeit "Direct3D immediate Mode" mehr Parameter Validierung aus als die Verkaufsversion, die gelegentlich überhaupt keine Überprüfung ausführt. Dadurch können Anwendungen ein stabiles Debuggen mit der langsameren Debug-Laufzeitkomponente durchführen, bevor Sie die schnellere Einzelhandelsversion für die Leistungsoptimierung und die endgültige Version verwenden.

Obwohl mehrere Direct3D-Methoden für den unmittelbaren Modus Grenzwerte für die zu akzeptierenden Werte vorsehen, werden diese Grenzwerte häufig nur von der Debugversion der Laufzeit des Direct3D unmittelbaren Modus geprüft und erzwungen. Anwendungen müssen diesen Grenzwerten entsprechen, oder es können unvorhersehbare und unerwünschte Ergebnisse auftreten, wenn Sie in der Verkaufsversion von Direct3D ausgeführt werden. Beispielsweise akzeptiert die [**IDirect3DDevice9::D rawprimiprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) -Methode einen Parameter (primitivecount), der die Anzahl der primitiven angibt, die von der Methode gerrentet werden. Die-Methode kann nur Werte zwischen 0 und D3DMAXNUMPRIMITIVES akzeptieren. Wenn Sie in der Debugversion von Direct3D mehr als D3DMAXNUMPRIMITIVES primitive übergeben, schlägt die Methode ordnungsgemäß fehl, druckt eine Fehlermeldung in das Fehlerprotokoll und gibt einen Fehlerwert an die Anwendung zurück. Wenn die Anwendung dagegen denselben Fehler ausführt, wenn Sie mit der Verkaufsversion der Laufzeit ausgeführt wird, ist das Verhalten nicht definiert. Aus Leistungsgründen überprüft die-Methode die Parameter nicht, was zu unvorhersehbarem und vollständig veränderbarem Verhalten führt, wenn Sie nicht gültig sind. In einigen Fällen kann der-Befehl funktionieren, und in anderen Fällen kann er in Direct3D zu einem Speicherfehler führen. Wenn ein ungültiger-Rückruf konstant mit einer bestimmten Hardwarekonfiguration und DirectX-Version funktioniert, gibt es keine Garantie dafür, dass er weiterhin auf anderer Hardware oder mit späteren Versionen von DirectX funktioniert.

Wenn in Ihrer Anwendung bei der Ausführung mit der Direct3D-Lauf Zeit Datei für den Einzelhandel unerklärliche Fehler auftreten, testen Sie die Debugversion, und suchen Sie nach Fällen, in denen Ihre Anwendung ungültige Parameter übergibt. Verwenden Sie das DirectX-System Steuerungs Applet, wechseln Sie ggf. zur Debug-Laufzeit, und aktivieren Sie die Option "unterbrechen bei D3DError". Mit dieser Option wird die Laufzeit gezwungen, die Windows DebugBreak-Methode zu verwenden, um zu erzwingen, dass die Anwendung beendet wird, wenn ein Anwendungsfehler erkannt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmiertipps](programming-tips.md)
</dt> </dl>

 

 
