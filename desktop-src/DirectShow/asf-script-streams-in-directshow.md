---
description: ASF-Skript Datenströme in DirectShow
ms.assetid: afef1b8b-4be2-48a1-b72a-b2e6342a5e84
title: ASF-Skript Datenströme in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da279c654a581bdb9eba23371882c5cbefbf5849
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103958017"
---
# <a name="asf-script-streams-in-directshow"></a><span data-ttu-id="6e37b-103">ASF-Skript Datenströme in DirectShow</span><span class="sxs-lookup"><span data-stu-id="6e37b-103">ASF Script Streams in DirectShow</span></span>

<span data-ttu-id="6e37b-104">Wenn der [WM-ASF-Reader](wm-asf-reader-filter.md) -Filter eine Datei erhält, die einen Datenstrom des Typs wmmediatype- \_ Skript enthält, wird eine entsprechende Ausgabe-PIN erstellt, die mit dem [internen rendererfilter des Skript Befehls](internal-script-command-renderer-filter.md) verbunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="6e37b-104">When the [WM ASF Reader](wm-asf-reader-filter.md) filter is given a file that includes a stream of type WMMEDIATYPE\_Script, it creates an output pin for it that can be connected to the [Internal Script Command Renderer](internal-script-command-renderer-filter.md) filter.</span></span> <span data-ttu-id="6e37b-105">Beim Aufruf von [**igraphbuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)wird dieser Filter automatisch dem Diagramm hinzugefügt und verbunden.</span><span class="sxs-lookup"><span data-stu-id="6e37b-105">When you call [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile), that filter is automatically added to the graph and connected.</span></span> <span data-ttu-id="6e37b-106">Wenn der Renderer des internen Skript Befehls ein Beispiel mit einem Skript Befehl empfängt, löst es ein [**EC- \_ OLE- \_ Ereignis**](ec-ole-event.md) Ereignis aus, dessen *LPARAM* das Skript enthält.</span><span class="sxs-lookup"><span data-stu-id="6e37b-106">When the Internal Script Command Renderer receives a sample containing a script command, it fires an [**EC\_OLE\_EVENT**](ec-ole-event.md) event whose *lParam* contains the script.</span></span> <span data-ttu-id="6e37b-107">Die Anwendung ist vollständig für die Behandlung dieses Ereignisses verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="6e37b-107">The application is entirely responsible for handling this event.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e37b-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6e37b-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e37b-109">Lesen von ASF-Dateien in DirectShow</span><span class="sxs-lookup"><span data-stu-id="6e37b-109">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



