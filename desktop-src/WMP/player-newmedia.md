---
title: Player. newmedia-Methode
description: Die newmedia-Methode erstellt ein neues Medienobjekt.
ms.assetid: fccf1559-bac3-4edf-bd88-da2c72cdec21
keywords:
- newmedia-Methode, Windows-Media Player
- newmedia-Methode, Windows Media Player, Player-Klasse
- Player-Klasse, Windows Media Player, newmedia-Methode
topic_type:
- apiref
api_name:
- Player.newMedia
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaafb97f836135aa9dd112372b1931c8561cb40b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354765"
---
# <a name="playernewmedia-method"></a><span data-ttu-id="e00f8-106">Player. newmedia-Methode</span><span class="sxs-lookup"><span data-stu-id="e00f8-106">Player.newMedia method</span></span>

<span data-ttu-id="e00f8-107">Die **newmedia** -Methode erstellt ein neues **Medien** Objekt.</span><span class="sxs-lookup"><span data-stu-id="e00f8-107">The **newMedia** method creates a new **Media** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e00f8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e00f8-108">Syntax</span></span>


```JScript
retVal = Player.newMedia(
  URL
)
```



## <a name="parameters"></a><span data-ttu-id="e00f8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e00f8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e00f8-110">*URL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e00f8-110">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e00f8-111">**Zeichenfolge** , die die URL der digitalen Mediendatei enthält, mit der das **Medien** Objekt erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e00f8-111">**String** containing the URL of the digital media file to create the **Media** object with.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e00f8-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e00f8-112">Return value</span></span>

<span data-ttu-id="e00f8-113">Diese Methode gibt ein **Medien** Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="e00f8-113">This method returns a **Media** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e00f8-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e00f8-114">Remarks</span></span>

<span data-ttu-id="e00f8-115">Der *URL* -Parameter darf keine leere Zeichenfolge oder NULL sein.</span><span class="sxs-lookup"><span data-stu-id="e00f8-115">The *URL* parameter must not be an empty string or null.</span></span>

## <a name="requirements"></a><span data-ttu-id="e00f8-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e00f8-116">Requirements</span></span>



| <span data-ttu-id="e00f8-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e00f8-117">Requirement</span></span> | <span data-ttu-id="e00f8-118">Wert</span><span class="sxs-lookup"><span data-stu-id="e00f8-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e00f8-119">Version</span><span class="sxs-lookup"><span data-stu-id="e00f8-119">Version</span></span><br/> | <span data-ttu-id="e00f8-120">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="e00f8-120">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="e00f8-121">DLL</span><span class="sxs-lookup"><span data-stu-id="e00f8-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="e00f8-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e00f8-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e00f8-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e00f8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e00f8-124">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="e00f8-124">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





