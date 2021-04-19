---
description: Rückruf, der die Versionen aller unterstützten Schnittstellen zurückgibt. Dadurch kann der Consumer nicht mehr mit der Erfassungs-Engine synchronisiert werden.
MS-HAID: vspixengine.IVersionCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Iversioncallback-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 7135E175-C537-4B0C-8F0A-CB77E3F2D945
api_name:
- IVersionCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c53008e625d63e2e876bef9ab8cbdd376508c2f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343136"
---
# <a name="span-idvspixengineiversioncallbackspaniversioncallback-interface"></a><span data-ttu-id="06846-104"><span id="vspixengine.iversioncallback"></span>Iversioncallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="06846-104"><span id="vspixengine.iversioncallback"></span>IVersionCallback interface</span></span>

<span data-ttu-id="06846-105">Rückruf, der die Versionen aller unterstützten Schnittstellen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="06846-105">Callback to return the versions of all the interfaces supported.</span></span> <span data-ttu-id="06846-106">Dadurch kann der Consumer nicht mehr mit der Erfassungs-Engine synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="06846-106">This allows the consumer to be out of sync with the capture engine.</span></span>

## <a name="members"></a><span data-ttu-id="06846-107">Member</span><span class="sxs-lookup"><span data-stu-id="06846-107">Members</span></span>

<span data-ttu-id="06846-108">Die **iversioncallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="06846-108">The **IVersionCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="06846-109">**Iversioncallback** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="06846-109">**IVersionCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="06846-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="06846-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="06846-111"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="06846-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="06846-112">Die **iversioncallback** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="06846-112">The **IVersionCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="06846-113">Methode</span><span class="sxs-lookup"><span data-stu-id="06846-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="06846-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06846-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="06846-115"><a href="/windows/desktop/direct3dtools/iversioncallback-versiontableready-guid-arr-uint"><strong>Versiontableready</strong></a></span><span class="sxs-lookup"><span data-stu-id="06846-115"><a href="/windows/desktop/direct3dtools/iversioncallback-versiontableready-guid-arr-uint"><strong>VersionTableReady</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="06846-116">Eine Rückruffunktion, mit der der Host darüber benachrichtigt wird, welche Schnittstellen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="06846-116">A callback function used to notify the host of which interfaces are supported.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="06846-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06846-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="06846-118">Header</span><span class="sxs-lookup"><span data-stu-id="06846-118">Header</span></span></p></td><td><span data-ttu-id="06846-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="06846-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
