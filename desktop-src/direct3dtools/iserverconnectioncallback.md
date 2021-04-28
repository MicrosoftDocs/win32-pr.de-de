---
description: '<span id="vspixengine.iserverconnectioncallback"></span>IServerConnectionCallback-Schnittstelle: Nicht verwendet.'
MS-HAID: vspixengine.IServerConnectionCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IServerConnectionCallback-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E140C0EA-2DAB-4F86-B1AE-4AE9214DE40A
api_name:
- IServerConnectionCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: eb41908bd23fcd1c719b692f2680fd7d1dda3e77
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087908"
---
# <a name="span-idvspixengineiserverconnectioncallbackspaniserverconnectioncallback-interface"></a><span data-ttu-id="ffc40-103"><span id="vspixengine.iserverconnectioncallback"></span>IServerConnectionCallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ffc40-103"><span id="vspixengine.iserverconnectioncallback"></span>IServerConnectionCallback interface</span></span>

<span data-ttu-id="ffc40-104">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ffc40-104">Not used.</span></span>

## <a name="members"></a><span data-ttu-id="ffc40-105">Member</span><span class="sxs-lookup"><span data-stu-id="ffc40-105">Members</span></span>

<span data-ttu-id="ffc40-106">Die **IServerConnectionCallback-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="ffc40-106">The **IServerConnectionCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ffc40-107">**IServerConnectionCallback** verfügt auch über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ffc40-107">**IServerConnectionCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="ffc40-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="ffc40-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="ffc40-109"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="ffc40-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="ffc40-110">Die **IServerConnectionCallback-Schnittstelle** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="ffc40-110">The **IServerConnectionCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="ffc40-111">Methode</span><span class="sxs-lookup"><span data-stu-id="ffc40-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="ffc40-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ffc40-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="ffc40-113"><a href="/windows/desktop/direct3dtools/iserverconnectioncallback-connecttoengine-bool-bstr-ipixengine-ptr-ptr"><strong>ConnectToEngine</strong></a></span><span class="sxs-lookup"><span data-stu-id="ffc40-113"><a href="/windows/desktop/direct3dtools/iserverconnectioncallback-connecttoengine-bool-bstr-ipixengine-ptr-ptr"><strong>ConnectToEngine</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="ffc40-114">Stellen Sie eine Verbindung mit einer anderen Instanz einer Remote-Engine auf dem lokalen Computer her.</span><span class="sxs-lookup"><span data-stu-id="ffc40-114">Connect to another instance of a remote engine on the local machine.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="ffc40-115"><a href="/windows/desktop/direct3dtools/iserverconnectioncallback-waitforshutdown-ipixengine-ptr"><strong>WaitForShutdown</strong></a></span><span class="sxs-lookup"><span data-stu-id="ffc40-115"><a href="/windows/desktop/direct3dtools/iserverconnectioncallback-waitforshutdown-ipixengine-ptr"><strong>WaitForShutdown</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="ffc40-116">Warten Sie auf das Herunterfahren der angegebenen Engine (Blockierender Aufruf).</span><span class="sxs-lookup"><span data-stu-id="ffc40-116">Wait for shutdown of the specified engine (Blocking call).</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="ffc40-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ffc40-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ffc40-118">Header</span><span class="sxs-lookup"><span data-stu-id="ffc40-118">Header</span></span></p></td><td><span data-ttu-id="ffc40-119">Vspixengine.h</span><span class="sxs-lookup"><span data-stu-id="ffc40-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
