---
title: Player. MediaError-Ereignis
description: Das MediaError-Ereignis tritt auf, wenn das Medienobjekt einen Fehlerzustand aufweist.
ms.assetid: b2e0176a-cc52-4f59-8894-440f426a1b6e
keywords:
- Media Player "MediaError-Ereignisfenster"
- MediaError-Ereignis, Windows Media Player, Player-Klasse
- Player-Klasse Windows Media Player, MediaError-Ereignis
topic_type:
- apiref
api_name:
- Player.MediaError
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8c22825f4aa720efa85275ce520eb81f082fd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372595"
---
# <a name="playermediaerror-event"></a><span data-ttu-id="2205d-106">Player. MediaError-Ereignis</span><span class="sxs-lookup"><span data-stu-id="2205d-106">Player.MediaError event</span></span>

<span data-ttu-id="2205d-107">Das **MediaError** -Ereignis tritt auf, wenn das **Medien** Objekt einen Fehlerzustand aufweist.</span><span class="sxs-lookup"><span data-stu-id="2205d-107">The **MediaError** event occurs when the **Media** object has an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="2205d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2205d-108">Syntax</span></span>


```JScript
Player.MediaError(
  pMediaObject
)
```



## <a name="parameters"></a><span data-ttu-id="2205d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2205d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2205d-110">*pmediaobject*</span><span class="sxs-lookup"><span data-stu-id="2205d-110">*pMediaObject*</span></span> 
</dt> <dd>

<span data-ttu-id="2205d-111">Ein **Medien** Objekt, das über eine Fehlerbedingung verfügt.</span><span class="sxs-lookup"><span data-stu-id="2205d-111">**Media** object that has an error condition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2205d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2205d-112">Return value</span></span>

<span data-ttu-id="2205d-113">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2205d-113">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2205d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2205d-114">Remarks</span></span>

<span data-ttu-id="2205d-115">Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich.</span><span class="sxs-lookup"><span data-stu-id="2205d-115">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="2205d-116">Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="2205d-116">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="2205d-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2205d-117">Requirements</span></span>



| <span data-ttu-id="2205d-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2205d-118">Requirement</span></span> | <span data-ttu-id="2205d-119">Wert</span><span class="sxs-lookup"><span data-stu-id="2205d-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2205d-120">Version</span><span class="sxs-lookup"><span data-stu-id="2205d-120">Version</span></span><br/> | <span data-ttu-id="2205d-121">Windows Media Player für Windows XP oder höher.</span><span class="sxs-lookup"><span data-stu-id="2205d-121">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="2205d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="2205d-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="2205d-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2205d-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2205d-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2205d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2205d-125">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="2205d-125">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





