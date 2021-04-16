---
description: VMR-Fenstermodus (Kompatibilitätsmodus)
ms.assetid: e9fb1c83-860a-44c1-9633-c86f5d0fdadd
title: VMR-Fenstermodus (Kompatibilitätsmodus)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7312274881642d15b844e0fa950f72e52f92db8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104571297"
---
# <a name="vmr-windowed-compatibility-mode"></a>VMR-Fenstermodus (Kompatibilitätsmodus)

Die VMR ist so konzipiert, dass Sie mit allen vorhandenen DirectShow-Anwendungen kompatibel ist. Wenn Sie mit einer vorhandenen Anwendung verwendet wird, arbeitet die VMR im Fenstermodus mit einem einzelnen Videostream, auch als Kompatibilitätsmodus bezeichnet. Dieser Modus wird bereitgestellt, weil VMR-7 der Standard-Renderer unter Windows XP ist und daher automatisch in Aufrufen von [intelligenten Verbindungs](intelligent-connect.md) Methoden wie [**igraphbuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)verwendet wird. Wenn Ihre Anwendung Intelligent Connect verwendet und nur grundlegende Renderingfunktionen erfordert, benötigen Sie keinen speziellen Code zum ordnungsgemäßen Rendern mit VMR-7 unter Windows XP.

VMR-9 wird standardmäßig auch im Fenster-/Kompatibilitäts Modus ausgeführt. VMR-9 ist jedoch nie der Standardvideorenderer. Um VMR-9 in einer Anwendung zu verwenden, müssen Sie Sie explizit dem Filter Diagramm hinzufügen. Aus diesem Grund und da der fensterlose Modus eine bessere Funktionalität als der Fenstermodus bietet, gibt es keinen besonderen Vorteil bei der Verwendung von VMR-9 im Fenstermodus/Kompatibilitätsmodus.

**Verwenden von VMR-7 im Fenstermodus/Kompatibilitätsmodus**

Zum Einrichten oder Steuern von VMR-7 im Fenstermodus/Kompatibilitätsmodus ist keine spezielle Programmierung erforderlich. Erstellen Sie einfach das Filter Diagramm mithilfe der standardmäßigen Graph-Erstellungs Aufrufe, und VMR-7 wird standardmäßig auf diesen Modus fest.

Im Fenstermodus/Kompatibilitätsmodus erstellt VMR-7 ein eigenes Fenster, um das Video anzuzeigen. Zu diesem Zweck lädt es die Fenster-Manager-Komponente, die die Schnittstellen [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) und [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) verfügbar macht. Die Anwendung kann den Filter Graph-Manager für diese Schnittstellen Abfragen, genau wie bei dem alten Videorendererfilter. Weitere Informationen finden Sie unter [verwenden](using-windowed-mode.md)des Fenstermodus.

Die folgende Abbildung zeigt VMR-7 im Fenstermodus/Kompatibilitätsmodus.

![VMR im Kompatibilitätsmodus](images/vmr-compat-mode.png)

Um die maximale Kompatibilitäts Stufe zu gewährleisten, hat das Videofenster denselben Klassennamen wie das, das von dem alten Videorendererfilter erstellt wurde, und der meiste Windows-Manager-Code aus dem alten Videorenderer wird weiterhin von VMR verwendet. Im Fenstermodus/Kompatibilitätsmodus verbraucht VMR nicht mehr Systemressourcen als der alte Videorenderer. Da VMR-7 nur über einen Eingabestream im Fenstermodus/Kompatibilitätsmodus verfügt, werden seine Mixer-oder compositorkomponenten nicht geladen.

Standardmäßig dehnt VMR das Bild, um das Videofenster auszufüllen. Wenn Sie das Seitenverhältnis der Quelle beibehalten möchten, können Sie die [**ivmraspectratiocontrol:: setaspectratiomode**](/windows/desktop/api/Strmif/nf-strmif-ivmraspectratiocontrol-setaspectratiomode) -Methode mit dem \_ \_ Textfeld-Flag für den VMR-armode-Buchstabe aufrufen \_ .

> [!Note]  
> MFC-Anwendungen, die das Videofenster in einem untergeordneten Fenster platzieren, müssen einen leeren WM \_ erasebkgnd-Nachrichten Handler definieren, oder der Videoanzeige Bereich wird nicht ordnungsgemäß neu gezeichnet.

 

**Verwenden von VMR-7 im Windowed-/Kompatibilitäts Modus mit mehreren Streams**

Im Fenstermodus/Kompatibilitätsmodus erstellt VMR-7 standardmäßig eine einzelne Eingabe-PIN und deaktiviert den Mischungs Modus. Um den Mischungs Modus zu aktivieren, müssen Sie die VMR konfigurieren, bevor Sie eine Verbindung herstellen. Weitere Informationen finden Sie unter [VMR mit mehreren Streams (Mischungs Modus)](vmr-with-multiple-streams--mixing-mode.md). Im Mischungs Modus lädt der VMR die Mischungs-und Compositor-Komponenten, die mehr Systemressourcen benötigen.

**Verwenden von VMR-9 im Fenstermodus**

Da VMR-9 nicht der Standardrenderer ist, verfügt es nicht über einen Kompatibilitätsmodus. Stattdessen wird für VMR-9 standardmäßig der Fenster-Modus mit vier Eingabe Pins verwendet. Sie können diesen Modus verwenden, um bis zu vier Videostreams zu mischen. Wenn Sie eine größere Anzahl von Streams mischen müssen, müssen Sie diese wie unter [VMR mit mehreren Streams (Mischungs Modus)](vmr-with-multiple-streams--mixing-mode.md)beschrieben konfigurieren. Andernfalls verhält sich VMR-9 im Fenstermodus genau wie VMR-7 im Fenstermodus/Kompatibilitätsmodus.

 

 



