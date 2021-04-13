---
description: Ursprüngliche Schnittstelle für die Kommunikation von Daten über einen vsglog.
MS-HAID: vspixengine.IPixEngine
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Ipixengine-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 87AB1D07-8E90-49F0-B44D-F6185923B8D4
api_name:
- IPixEngine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2f02538f7acbd88daf166af657382e507a4e5661
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482643"
---
# <a name="span-idvspixengineipixenginespanipixengine-interface"></a><span data-ttu-id="aabe1-103"><span id="vspixengine.ipixengine"></span>Ipixengine-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="aabe1-103"><span id="vspixengine.ipixengine"></span>IPixEngine interface</span></span>

<span data-ttu-id="aabe1-104">Ursprüngliche Schnittstelle für die Kommunikation von Daten über einen vsglog.</span><span class="sxs-lookup"><span data-stu-id="aabe1-104">Original interface for communicating data about a vsglog .</span></span>

## <a name="members"></a><span data-ttu-id="aabe1-105">Member</span><span class="sxs-lookup"><span data-stu-id="aabe1-105">Members</span></span>

<span data-ttu-id="aabe1-106">Die **ipixengine** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="aabe1-106">The **IPixEngine** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="aabe1-107">**Ipixengine** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="aabe1-107">**IPixEngine** also has these types of members:</span></span>

-   [<span data-ttu-id="aabe1-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="aabe1-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="aabe1-109"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="aabe1-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="aabe1-110">Die **ipixengine** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="aabe1-110">The **IPixEngine** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="aabe1-111">Methode</span><span class="sxs-lookup"><span data-stu-id="aabe1-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="aabe1-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aabe1-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="aabe1-113"><a href="/windows/desktop/direct3dtools/ipixengine-openfile-bstr-bstr-inewframescallback-ptr-ifileiocallback-ptr-lcid"><strong>OpenFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="aabe1-113"><a href="/windows/desktop/direct3dtools/ipixengine-openfile-bstr-bstr-inewframescallback-ptr-ifileiocallback-ptr-lcid"><strong>OpenFile</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="aabe1-114">Öffnet ein Grafik Protokoll.</span><span class="sxs-lookup"><span data-stu-id="aabe1-114">Opens a graphics log.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="aabe1-115"><a href="/windows/desktop/direct3dtools/ipixengine-runexperiment-experiment-irunexperimentcallback-ptr-inewframescallback-ptr-ifileiocallback-ptr-dword-experimenttrigger-arr"><strong>Runexperiment</strong></a></span><span class="sxs-lookup"><span data-stu-id="aabe1-115"><a href="/windows/desktop/direct3dtools/ipixengine-runexperiment-experiment-irunexperimentcallback-ptr-inewframescallback-ptr-ifileiocallback-ptr-dword-experimenttrigger-arr"><strong>RunExperiment</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="aabe1-116">Führt ein Experiment aus.</span><span class="sxs-lookup"><span data-stu-id="aabe1-116">Runs an experiment.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="aabe1-117"><a href="/windows/desktop/direct3dtools/ipixengine-savefile-bstr-ifileiocallback-ptr"><strong>SaveFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="aabe1-117"><a href="/windows/desktop/direct3dtools/ipixengine-savefile-bstr-ifileiocallback-ptr"><strong>SaveFile</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="aabe1-118">Speichert das Grafik Protokoll an der angegebenen Position.</span><span class="sxs-lookup"><span data-stu-id="aabe1-118">Saves the graphics log to the specified location.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="aabe1-119"><a href="/windows/desktop/direct3dtools/ipixengine-setparentprocess-dword"><strong>SetParser-Prozess</strong></a></span><span class="sxs-lookup"><span data-stu-id="aabe1-119"><a href="/windows/desktop/direct3dtools/ipixengine-setparentprocess-dword"><strong>SetParentProcess</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="aabe1-120">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="aabe1-120">Not used.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="aabe1-121"><a href="/windows/desktop/direct3dtools/ipixengine-shutdown"><strong>Abschlusses</strong></a></span><span class="sxs-lookup"><span data-stu-id="aabe1-121"><a href="/windows/desktop/direct3dtools/ipixengine-shutdown"><strong>ShutDown</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="aabe1-122">Fährt die Engine herunter.</span><span class="sxs-lookup"><span data-stu-id="aabe1-122">Shuts down the engine.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="aabe1-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aabe1-123">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="aabe1-124">Header</span><span class="sxs-lookup"><span data-stu-id="aabe1-124">Header</span></span></p></td><td><span data-ttu-id="aabe1-125">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="aabe1-125">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
