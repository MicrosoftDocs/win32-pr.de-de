---
description: Das Medien Streaming-Terminal (MST) ist ein dynamisches Terminal, das auf der Verwendung von DirectShow-Filtern basiert. Ein msp, der mit den TAPI 3-MSP-Basisklassen geschrieben wurde, integriert eine MST, aber MSP-Autoren können diese ohne die Basisklassen implementieren.
ms.assetid: 21015c33-2ad1-4472-b346-167953d06a21
title: Medien Streaming-Terminal (MST)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afb9bb4b97d0e741aec96454b187beefe2d21eb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961156"
---
# <a name="media-streaming-terminal-mst"></a><span data-ttu-id="31818-104">Medien Streaming-Terminal (MST)</span><span class="sxs-lookup"><span data-stu-id="31818-104">Media Streaming Terminal (MST)</span></span>

<span data-ttu-id="31818-105">Das Medien Streaming-Terminal (MST) ist ein dynamisches Terminal, das auf der Verwendung von DirectShow-Filtern basiert.</span><span class="sxs-lookup"><span data-stu-id="31818-105">The Media Streaming Terminal (MST) is a dynamic terminal based on use of DirectShow filters.</span></span> <span data-ttu-id="31818-106">Ein msp, der mit den [TAPI 3-MSP-Basisklassen](tapi-3-msp-base-classes.md) geschrieben wurde, integriert eine MST, aber MSP-Autoren können diese ohne die Basisklassen implementieren.</span><span class="sxs-lookup"><span data-stu-id="31818-106">An MSP written using the [TAPI 3 MSP Base Classes](tapi-3-msp-base-classes.md) will incorporate an MST, but MSP authors may choose to implement it without using the base classes.</span></span>

<span data-ttu-id="31818-107">Um die MST-Erstellung aufzurufen, ruft eine Anwendung [**itterminalsupport:: | ateterminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal) mithilfe von *pterminalclass* auf, die auf CLSID \_ mediastreamterminal festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="31818-107">To invoke MST creation, an application makes a call to [**ITTerminalSupport::CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal) using *pTerminalClass* set to CLSID\_MediaStreamTerminal.</span></span>

<span data-ttu-id="31818-108">Die Schnittstellen [**itammediaformat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat) und [**itzugenorproperties**](/windows/win32/api/tapi3/nn-tapi3-itallocatorproperties) werden dann im Terminal verfügbar gemacht, sodass eine Anwendung die Streamingleistung optimieren kann.</span><span class="sxs-lookup"><span data-stu-id="31818-108">The [**ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat) and [**ITAllocatorProperties**](/windows/win32/api/tapi3/nn-tapi3-itallocatorproperties) interfaces are then exposed on the terminal, allowing an application to tune streaming performance.</span></span> <span data-ttu-id="31818-109">Diese Schnittstellen werden in Tapi3. h deklariert.</span><span class="sxs-lookup"><span data-stu-id="31818-109">These interfaces are declared in Tapi3.h.</span></span>

<span data-ttu-id="31818-110">Die Implementierung und Verwendung eines MST erfordert Vertrautheit mit DirectShow-Filtern und der Filter Diagramm Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="31818-110">Implementation and use of an MST requires familiarity with DirectShow filters and filter graph management.</span></span> <span data-ttu-id="31818-111">Weitere Informationen finden Sie im DirectShow-Material unter dem Grafik-und Multimedia Services-Knoten des Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="31818-111">Please refer to the DirectShow material under the Graphic and Multimedia Services node of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="31818-112">Der multimediastreamingverweis ist besonders nützlich für MSP-Autoren.</span><span class="sxs-lookup"><span data-stu-id="31818-112">The Multimedia Streaming Reference will be particularly useful to MSP authors.</span></span>

 

 
