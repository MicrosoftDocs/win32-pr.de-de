---
title: "\"Settings. Volume\""
description: Die Volume-Eigenschaft gibt das aktuelle Volume an oder ruft es ab.
ms.assetid: 60143eff-3a34-43eb-a86d-641c2a5cfc01
keywords:
- Windows-Media Player "Settings. Volume"
topic_type:
- apiref
api_name:
- Settings.volume
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f5ec4299bf33ed16143eec8570b65c548599e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369666"
---
# <a name="settingsvolume"></a><span data-ttu-id="f4f18-104">"Settings. Volume"</span><span class="sxs-lookup"><span data-stu-id="f4f18-104">Settings.volume</span></span>

<span data-ttu-id="f4f18-105">Die **Volume** -Eigenschaft gibt das aktuelle Volume an oder ruft es ab.</span><span class="sxs-lookup"><span data-stu-id="f4f18-105">The **volume** property specifies or retrieves the current volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4f18-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4f18-106">Syntax</span></span>

<span data-ttu-id="f4f18-107">Player. Settings. Volume</span><span class="sxs-lookup"><span data-stu-id="f4f18-107">player.settings.volume</span></span>

## <a name="possible-values"></a><span data-ttu-id="f4f18-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="f4f18-108">Possible Values</span></span>

<span data-ttu-id="f4f18-109">Diese Eigenschaft ist eine Lese-/schreibzahl (**Long**) im Bereich von 0 bis 100. </span><span class="sxs-lookup"><span data-stu-id="f4f18-109">This property is a read/write **Number** (**long**) ranging from 0 to 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4f18-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4f18-110">Remarks</span></span>

<span data-ttu-id="f4f18-111">NULL gibt kein Volume an, und 100 gibt das vollständige Volume an.</span><span class="sxs-lookup"><span data-stu-id="f4f18-111">Zero specifies no volume and 100 specifies full volume.</span></span> <span data-ttu-id="f4f18-112">Wenn für diese Eigenschaft kein Wert angegeben wird, wird standardmäßig die letzte für den Player festgelegte volumeeinstellung verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4f18-112">If no value is specified for this property, it defaults to the last volume setting established for the player.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4f18-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4f18-113">Requirements</span></span>



| <span data-ttu-id="f4f18-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f4f18-114">Requirement</span></span> | <span data-ttu-id="f4f18-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f4f18-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f4f18-116">Version</span><span class="sxs-lookup"><span data-stu-id="f4f18-116">Version</span></span><br/> | <span data-ttu-id="f4f18-117">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="f4f18-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f4f18-118">DLL</span><span class="sxs-lookup"><span data-stu-id="f4f18-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="f4f18-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4f18-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4f18-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4f18-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4f18-121">**Einstellungs Objekt**</span><span class="sxs-lookup"><span data-stu-id="f4f18-121">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





