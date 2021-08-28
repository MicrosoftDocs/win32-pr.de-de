---
description: VMR-Fenstermodus (Kompatibilität)
ms.assetid: e9fb1c83-860a-44c1-9633-c86f5d0fdadd
title: VMR-Fenstermodus (Kompatibilität)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d27a5a115ac87475a27365a0211d93cf18e785983cda12ee338e73b24fb0f77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049294"
---
# <a name="vmr-windowed-compatibility-mode"></a>VMR-Fenstermodus (Kompatibilität)

Die VMR ist so konzipiert, dass sie mit allen vorhandenen DirectShow-Anwendungen kompatibel ist. Wenn sie mit einer vorhandenen Anwendung verwendet wird, wird die VMR im Fenstermodus mit einem einzelnen Videostream betrieben, der auch als Kompatibilitätsmodus bezeichnet wird. Dieser Modus wird bereitgestellt, da VMR-7 der Standardrenderer auf Windows XP ist und daher automatisch in Aufrufen von [Intelligent Verbinden](intelligent-connect.md) Methoden wie [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)verwendet wird. Wenn Ihre Anwendung Intelligent Verbinden verwendet und nur grundlegende Renderingfunktionen erfordert, benötigen Sie keinen speziellen Code, um mit VMR-7 auf Windows XP ordnungsgemäß gerendert zu werden.

DIE VMR-9 wird standardmäßig auch im Fenster-/Kompatibilitätsmodus ausgeführt. VMR-9 ist jedoch nie der Standardvideorenderer. Um VMR-9 in einer Anwendung zu verwenden, müssen Sie sie explizit dem Filterdiagramm hinzufügen. Aus diesem Grund und da der fensterlose Modus eine bessere Funktionalität als der Fenstermodus bietet, bietet die Verwendung von VMR-9 im Fenster-/Kompatibilitätsmodus keinen besonderen Vorteil.

**Verwenden von VMR-7 im Fenster-/Kompatibilitätsmodus**

Es ist keine spezielle Programmierung erforderlich, um VMR-7 im Fenster-/Kompatibilitätsmodus einzurichten oder zu steuern. Erstellen Sie einfach das Filterdiagramm mit den standardmäßigen Grapherstellungsaufrufen, und vmr-7 wird standardmäßig in diesen Modus versetzt.

Im Fenster-/Kompatibilitätsmodus erstellt VMR-7 ein eigenes Fenster zum Anzeigen des Videos. Dazu wird die Komponente Fenster-Manager geladen, die die Schnittstellen [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) und [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) verfügbar macht. Ihre Anwendung kann den Filter Graph Manager für diese Schnittstellen genau wie beim alten Videorenderer-Filter abfragen. Weitere Informationen finden Sie unter [Verwenden des Fenstermodus](using-windowed-mode.md).

Die folgende Abbildung zeigt die VMR-7 im Fenster-/Kompatibilitätsmodus.

![vmr im Kompatibilitätsmodus](images/vmr-compat-mode.png)

Um den maximalen Kompatibilitätsgrad zu gewährleisten, hat das Videofenster den gleichen Klassennamen wie der, der vom alten Videorendererfilter erstellt wurde, und der größte Teil des Fenster-Manager-Codes aus dem alten Videorenderer wird weiterhin von der VMR verwendet. Im Fenster-/Kompatibilitätsmodus verbraucht die VMR nicht mehr Systemressourcen als der alte Videorenderer. Da die VMR-7 nur über einen Eingabestream im Fenster-/Kompatibilitätsmodus verfügt, werden die Mixer- oder Compositorkomponenten nicht geladen.

Standardmäßig streckt die VMR das Image, um das Videofenster zu füllen. Um das Seitenverhältnis der Quelle beizubehalten, rufen Sie die [**IVMRAspectRatioControl::SetAspectRatioMode-Methode**](/windows/desktop/api/Strmif/nf-strmif-ivmraspectratiocontrol-setaspectratiomode) mit dem VMR \_ ARMODE \_ LETTER \_ BOX-Flag auf.

> [!Note]  
> MFC-Anwendungen, die das Videofenster in einem untergeordneten Fenster platzieren, müssen einen leeren WM \_ ERASEBKGND-Meldungshandler definieren. Andernfalls wird der Videoanzeigebereich nicht ordnungsgemäß neu maliert.

 

**Verwenden von VMR-7 im Fenster-/Kompatibilitätsmodus mit mehreren Streams**

Im Fenster-/Kompatibilitätsmodus erstellt VMR-7 standardmäßig einen einzelnen Eingabepin und deaktiviert den Gemischtmodus. Um den Gemischtmodus zu aktivieren, müssen Sie die VMR konfigurieren, bevor Sie eine Verbindung herstellen. Weitere Informationen finden Sie unter [VMR with Multiple Streams (Mixing Mode) (VMR mit mehreren Streams (Gemischter Modus)).](vmr-with-multiple-streams--mixing-mode.md) Im Gemischtmodus lädt die VMR die Mischen- und Compositorkomponenten, die mehr Systemressourcen erfordern.

**Verwenden von VMR-9 im Fenstermodus**

Da VMR-9 nicht der Standardrenderer ist, verfügt er nicht über einen Kompatibilitätsmodus. Stattdessen verwendet VMR-9 standardmäßig den Fenstermodus mit vier Eingabepins. Sie können diesen Modus verwenden, um bis zu vier Videostreams zu mischen. Wenn Sie eine größere Anzahl von Streams mischen müssen, müssen Sie sie wie unter [VMR mit Mehreren Streams (Gemischter Modus)](vmr-with-multiple-streams--mixing-mode.md)beschrieben konfigurieren. Andernfalls verhält sich VMR-9 im Fenstermodus genauso wie VMR-7 im Fenster-/Kompatibilitätsmodus.

 

 



