---
description: Eine Schnittstelle für die Remote Kommunikation von Daten zu einem vsglog.
MS-HAID: vspixengine.IPeerToPeerEngine
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPeer-topeerengine-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C6C4783F-ED46-47C2-98BB-C618897F8FF8
api_name:
- IPeerToPeerEngine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 899e5eea28ffb769e082b2e0bd7bc165889b2d37
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342552"
---
# <a name="span-idvspixengineipeertopeerenginespanipeertopeerengine-interface"></a><span data-ttu-id="f84a5-103"><span id="vspixengine.ipeertopeerengine"></span>IPeer-topeerengine-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f84a5-103"><span id="vspixengine.ipeertopeerengine"></span>IPeerToPeerEngine interface</span></span>

<span data-ttu-id="f84a5-104">Eine Schnittstelle für die Remote Kommunikation von Daten zu einem vsglog.</span><span class="sxs-lookup"><span data-stu-id="f84a5-104">Interface for remote communicating data about a vsglog.</span></span>

## <a name="members"></a><span data-ttu-id="f84a5-105">Member</span><span class="sxs-lookup"><span data-stu-id="f84a5-105">Members</span></span>

<span data-ttu-id="f84a5-106">Die **iPeer-topeerengine** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f84a5-106">The **IPeerToPeerEngine** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f84a5-107">**Ietertopeerengine** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f84a5-107">**IPeerToPeerEngine** also has these types of members:</span></span>

-   [<span data-ttu-id="f84a5-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="f84a5-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="f84a5-109"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="f84a5-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="f84a5-110">Die **iPeer-topeerengine** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f84a5-110">The **IPeerToPeerEngine** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="f84a5-111">Methode</span><span class="sxs-lookup"><span data-stu-id="f84a5-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="f84a5-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f84a5-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="f84a5-113"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-cancelsetplaybackendpoint"><strong>Cancelsetplaybackendpoint</strong></a></span><span class="sxs-lookup"><span data-stu-id="f84a5-113"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-cancelsetplaybackendpoint"><strong>CancelSetPlaybackEndpoint</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="f84a5-114">Bricht eine vorherige Anforderung zum Einrichten einer Remote Verbindung ab.</span><span class="sxs-lookup"><span data-stu-id="f84a5-114">Cancels a previous request to set up a remote connection.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="f84a5-115"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-getplaybackendpoint-bool-bstr-ptr-bstr-ptr-remotingversion-ptr"><strong>Getplaybackendpoint</strong></a></span><span class="sxs-lookup"><span data-stu-id="f84a5-115"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-getplaybackendpoint-bool-bstr-ptr-bstr-ptr-remotingversion-ptr"><strong>GetPlaybackEndpoint</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="f84a5-116">Ruft die Endpunkt Adresse einer Remote-Engine ab.</span><span class="sxs-lookup"><span data-stu-id="f84a5-116">Gets the endpoint address of a remote engine.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="f84a5-117"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-setplaybackendpoint-bool-bstr-bstr-remotingversion"><strong>Setplaybackendpoint</strong></a></span><span class="sxs-lookup"><span data-stu-id="f84a5-117"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-setplaybackendpoint-bool-bstr-bstr-remotingversion"><strong>SetPlaybackEndpoint</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="f84a5-118">Legt die Endpunkt Adresse fest, die zum Herstellen einer Verbindung mit einem Remote Modul verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f84a5-118">Sets the endpoint address used to connect to a remote engine.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="f84a5-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f84a5-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f84a5-120">Header</span><span class="sxs-lookup"><span data-stu-id="f84a5-120">Header</span></span></p></td><td><span data-ttu-id="f84a5-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="f84a5-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
