---
title: Einstellungen. Balance
description: Die Balance-Eigenschaft gibt den aktuellen Stereo Saldo an oder ruft ihn ab.
ms.assetid: 26f04989-a1b1-4aec-8a15-c4e3737a4e62
keywords:
- Einstellungen. Balance für Windows-Media Player
topic_type:
- apiref
api_name:
- Settings.balance
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 248cd3b2bbf735ef54382fb5b1be52755cad3799
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359249"
---
# <a name="settingsbalance"></a><span data-ttu-id="34aa9-104">Einstellungen. Balance</span><span class="sxs-lookup"><span data-stu-id="34aa9-104">Settings.balance</span></span>

<span data-ttu-id="34aa9-105">Die **Balance** -Eigenschaft gibt den aktuellen Stereo Saldo an oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="34aa9-105">The **balance** property specifies or retrieves the current stereo balance.</span></span>

## <a name="syntax"></a><span data-ttu-id="34aa9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="34aa9-106">Syntax</span></span>

<span data-ttu-id="34aa9-107">Player. Settings. Balance</span><span class="sxs-lookup"><span data-stu-id="34aa9-107">player.settings.balance</span></span>

## <a name="possible-values"></a><span data-ttu-id="34aa9-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="34aa9-108">Possible Values</span></span>

<span data-ttu-id="34aa9-109">Diese Eigenschaft ist eine Lese-/schreibzahl (**Long**). </span><span class="sxs-lookup"><span data-stu-id="34aa9-109">This property is a read/write **Number** (**long**).</span></span> <span data-ttu-id="34aa9-110">Die Werte liegen im Bereich von 100 bis 100. der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="34aa9-110">Values range from  100 to 100, with a default value of zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="34aa9-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34aa9-111">Remarks</span></span>

<span data-ttu-id="34aa9-112">Der Wert 0 (null) gibt an, dass die Audiodaten gleichzeitig auf dem linken und rechten Kanal abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="34aa9-112">The value zero indicates that the audio plays at equal volume on both left and right channels.</span></span> <span data-ttu-id="34aa9-113">Der Wert 100 gibt an, dass Audioinhalte nur im linken Kanal abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="34aa9-113">A value of  100 indicates that audio plays only on the left channel.</span></span> <span data-ttu-id="34aa9-114">Der Wert 100 gibt an, dass Audioinhalte nur auf dem rechten Kanal abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="34aa9-114">A value of 100 indicates that audio plays only on the right channel.</span></span>

## <a name="requirements"></a><span data-ttu-id="34aa9-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34aa9-115">Requirements</span></span>



| <span data-ttu-id="34aa9-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34aa9-116">Requirement</span></span> | <span data-ttu-id="34aa9-117">Wert</span><span class="sxs-lookup"><span data-stu-id="34aa9-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="34aa9-118">Version</span><span class="sxs-lookup"><span data-stu-id="34aa9-118">Version</span></span><br/> | <span data-ttu-id="34aa9-119">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="34aa9-119">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="34aa9-120">DLL</span><span class="sxs-lookup"><span data-stu-id="34aa9-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="34aa9-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34aa9-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34aa9-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34aa9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34aa9-123">**Einstellungs Objekt**</span><span class="sxs-lookup"><span data-stu-id="34aa9-123">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





