---
title: Player. cdrommediachange-Ereignis
description: Das cdrommediachange-Ereignis tritt auf, wenn eine CD oder eine DVD in ein CD-oder DVD-Laufwerk eingefügt oder daraus entfernt wird. | Player. cdrommediachange-Ereignis
ms.assetid: d31a791a-55e5-49ee-bfe5-7488277e3fda
keywords:
- Cdrommediachange-Ereignisfenster Media Player
- Cdrommediachange-Ereignis, Windows Media Player, Player-Klasse
- Windows Media Player Player-Klasse, cdrommediachange-Ereignis
topic_type:
- apiref
api_name:
- Player.CdromMediaChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c3125235d5f8d19963b85284e7dbe40c7af408d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364664"
---
# <a name="playercdrommediachange-event"></a><span data-ttu-id="746f9-107">Player. cdrommediachange-Ereignis</span><span class="sxs-lookup"><span data-stu-id="746f9-107">Player.CdromMediaChange event</span></span>

<span data-ttu-id="746f9-108">Das **cdrommediachange** -Ereignis tritt auf, wenn eine CD oder eine DVD in ein CD-oder DVD-Laufwerk eingefügt oder daraus entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="746f9-108">The **CdromMediaChange** event occurs when a CD or DVD is inserted into or ejected from a CD or DVD drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="746f9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="746f9-109">Syntax</span></span>


```JScript
Player.CdromMediaChange(
  CdromNum
)
```



## <a name="parameters"></a><span data-ttu-id="746f9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="746f9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="746f9-111">*Cdromnum*</span><span class="sxs-lookup"><span data-stu-id="746f9-111">*CdromNum*</span></span> 
</dt> <dd>

<span data-ttu-id="746f9-112">**Zahl** (**Long**), die den Index des CD-oder DVD-Laufwerks angibt.</span><span class="sxs-lookup"><span data-stu-id="746f9-112">**Number** (**long**) specifying the index of the CD or DVD drive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="746f9-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="746f9-113">Return value</span></span>

<span data-ttu-id="746f9-114">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="746f9-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="746f9-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="746f9-115">Remarks</span></span>

<span data-ttu-id="746f9-116">Der Index des CD-Laufwerks entspricht dem Index eines **CDROM** -Objekts in der **cdromcollection**.</span><span class="sxs-lookup"><span data-stu-id="746f9-116">The index of the CD drive corresponds to the index of a **Cdrom** object in the **CdromCollection**.</span></span>

<span data-ttu-id="746f9-117">Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich.</span><span class="sxs-lookup"><span data-stu-id="746f9-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="746f9-118">Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="746f9-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="746f9-119">**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="746f9-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="746f9-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="746f9-120">Requirements</span></span>



| <span data-ttu-id="746f9-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="746f9-121">Requirement</span></span> | <span data-ttu-id="746f9-122">Wert</span><span class="sxs-lookup"><span data-stu-id="746f9-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="746f9-123">Version</span><span class="sxs-lookup"><span data-stu-id="746f9-123">Version</span></span><br/> | <span data-ttu-id="746f9-124">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="746f9-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="746f9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="746f9-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="746f9-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="746f9-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="746f9-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="746f9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="746f9-128">**Cdrom-Objekt**</span><span class="sxs-lookup"><span data-stu-id="746f9-128">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="746f9-129">**Cdromcollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="746f9-129">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="746f9-130">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="746f9-130">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





