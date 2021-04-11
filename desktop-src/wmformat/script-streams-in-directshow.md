---
title: Skripterstellung für Datenströme in DirectShow
description: Skripterstellung für Datenströme in DirectShow
ms.assetid: ad467897-1d25-4bb0-a0ec-84560fe7063b
keywords:
- Windows Media-Format-SDK, DirectShow
- Windows Media-Format-SDK, Skript Datenströme
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), Skript Datenströme
- ASF (Advanced Systems Format), Skript Datenströme
- DirectShow, Skript Datenströme
- Skript Datenströme, DirectShow
- Streams, Skript Datenströme in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09f08fab54dbdfe61dcc2ce78790cd471985cdeb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311159"
---
# <a name="script-streams-in-directshow"></a><span data-ttu-id="b73a3-112">Skripterstellung für Datenströme in DirectShow</span><span class="sxs-lookup"><span data-stu-id="b73a3-112">Script Streams in DirectShow</span></span>

<span data-ttu-id="b73a3-113">Wenn der WM-ASF-Reader-Filter eine Datei erhält, die einen Datenstrom des Typs wmmediatype- \_ Skript enthält, erstellt er eine Ausgabepin für diese, die mit dem Editor für den Renderer des internen Skript Befehls von DirectShow verbunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="b73a3-113">When the WM ASF Reader filter is given a file that includes a stream of type WMMEDIATYPE\_Script, it creates an output pin for it that can be connected to the DirectShow Internal Script Command Renderer filter.</span></span> <span data-ttu-id="b73a3-114">Beim Aufruf von **igraphbuilder:: RenderFile** wird dieser Filter automatisch dem Diagramm hinzugefügt und verbunden.</span><span class="sxs-lookup"><span data-stu-id="b73a3-114">When you call **IGraphBuilder::RenderFile**, that filter is automatically added to the graph and connected.</span></span> <span data-ttu-id="b73a3-115">Wenn der Renderer des internen Skript Befehls ein Beispiel mit einem Skript Befehl empfängt, löst es ein **EC- \_ OLE- \_ Ereignis** aus, dessen **LPARAM** das Skript enthält.</span><span class="sxs-lookup"><span data-stu-id="b73a3-115">When the Internal Script Command Renderer receives a sample containing a script command, it fires an **EC\_OLE\_EVENT** whose **lParam** contains the script.</span></span> <span data-ttu-id="b73a3-116">Die Anwendung ist vollständig für die Behandlung dieses Ereignisses verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="b73a3-116">The application is entirely responsible for handling this event.</span></span> <span data-ttu-id="b73a3-117">Weitere Informationen zu **EC- \_ OLE- \_ Ereignissen** finden Sie in der DirectShow-SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="b73a3-117">For more information on **EC\_OLE\_EVENT**, see the DirectShow SDK documentation.</span></span>

 

 




