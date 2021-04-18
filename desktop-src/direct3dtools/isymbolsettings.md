---
description: Übergibt Symbol Server Informationen an die Desktop Erfassungs-Engine.
MS-HAID: vspixengine.ISymbolSettings
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Isymbolsettings-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A0696E96-8996-4E5C-AEBC-604E9F9F7321
api_name:
- ISymbolSettings
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 26e045fdb269e3b0f852265e621c991561a9ad3b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106341113"
---
# <a name="span-idvspixengineisymbolsettingsspanisymbolsettings-interface"></a><span data-ttu-id="6d324-103"><span id="vspixengine.isymbolsettings"></span>Isymbolsettings-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6d324-103"><span id="vspixengine.isymbolsettings"></span>ISymbolSettings interface</span></span>

<span data-ttu-id="6d324-104">Übergibt Symbol Server Informationen an die Desktop Erfassungs-Engine.</span><span class="sxs-lookup"><span data-stu-id="6d324-104">Passes symbol server information to the desktop capture engine.</span></span>

## <a name="members"></a><span data-ttu-id="6d324-105">Member</span><span class="sxs-lookup"><span data-stu-id="6d324-105">Members</span></span>

<span data-ttu-id="6d324-106">Die **isymbolsettings** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="6d324-106">The **ISymbolSettings** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6d324-107">**Isymbolsettings** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6d324-107">**ISymbolSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="6d324-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="6d324-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="6d324-109"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="6d324-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="6d324-110">Die **isymbolsettings** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="6d324-110">The **ISymbolSettings** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="6d324-111">Methode</span><span class="sxs-lookup"><span data-stu-id="6d324-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="6d324-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6d324-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="6d324-113"><a href="/windows/desktop/direct3dtools/isymbolsettings-updatesymbolsettings-symbolserverinfo"><strong>Updatesymbolsettings</strong></a></span><span class="sxs-lookup"><span data-stu-id="6d324-113"><a href="/windows/desktop/direct3dtools/isymbolsettings-updatesymbolsettings-symbolserverinfo"><strong>UpdateSymbolSettings</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="6d324-114">Eine Anforderung zum Senden von debugsymbolpfaden an die lokale Engine (nicht Remote).</span><span class="sxs-lookup"><span data-stu-id="6d324-114">A request to send debug symbol paths to the local (non-remote) engine.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="6d324-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d324-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="6d324-116">Header</span><span class="sxs-lookup"><span data-stu-id="6d324-116">Header</span></span></p></td><td><span data-ttu-id="6d324-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="6d324-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
