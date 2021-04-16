---
title: Treffer Treffer Test-Ergebnisse
description: Die folgenden Konstanten identifizieren die möglichen Treffer Testergebnisse für ein Objekt relativ zu anderen Objekten, die den Berührungs Kontaktbereich überschneiden.
ms.assetid: EACDE6DB-ADBD-4F0C-8C31-7321AB6A73EA
topic_type:
- apiref
api_name:
- TOUCH_HIT_TESTING_PROXIMITY_CLOSEST
- TOUCH_HIT_TESTING_PROXIMITY_FARTHEST
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: f6590e7d56c1c9d92f0ff20524b6e4222d8655b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517618"
---
# <a name="touch-hit-testing-scores"></a><span data-ttu-id="d7443-103">Treffer Treffer Test-Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="d7443-103">Touch Hit Testing Scores</span></span>

<span data-ttu-id="d7443-104">Die folgenden Konstanten identifizieren die möglichen Treffer Testergebnisse für ein Objekt relativ zu anderen Objekten, die den Berührungs Kontaktbereich überschneiden.</span><span class="sxs-lookup"><span data-stu-id="d7443-104">The following constants identify the possible hit test scores for an object, relative to other objects that intersect the touch contact area.</span></span>

| <span data-ttu-id="d7443-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="d7443-105">Constant/value</span></span> | <span data-ttu-id="d7443-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d7443-106">Description</span></span> |
|---|---|
| <span data-ttu-id="d7443-107">**TOUCH_HIT_TESTING_PROXIMITY_CLOSEST** 0x0</span><span class="sxs-lookup"><span data-stu-id="d7443-107">**TOUCH_HIT_TESTING_PROXIMITY_CLOSEST** 0x0</span></span>      | <span data-ttu-id="d7443-108">Das-Objekt ist das wahrscheinlichste Ziel.</span><span class="sxs-lookup"><span data-stu-id="d7443-108">The object is the most probable target.</span></span><br/>  |
| <span data-ttu-id="d7443-109">**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST** 0xfff</span><span class="sxs-lookup"><span data-stu-id="d7443-109">**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST** 0xFFF</span></span> | <span data-ttu-id="d7443-110">Das-Objekt ist das am wenigsten wahrscheinliche Ziel.</span><span class="sxs-lookup"><span data-stu-id="d7443-110">The object is the least probable target.</span></span><br/> |

## <a name="requirements"></a><span data-ttu-id="d7443-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d7443-111">Requirements</span></span>

| <span data-ttu-id="d7443-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d7443-112">Requirement</span></span> | <span data-ttu-id="d7443-113">Wert</span><span class="sxs-lookup"><span data-stu-id="d7443-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d7443-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d7443-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d7443-115">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7443-115">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d7443-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d7443-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d7443-117">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d7443-117">None supported</span></span><br/>                                                            |
| <span data-ttu-id="d7443-118">Header</span><span class="sxs-lookup"><span data-stu-id="d7443-118">Header</span></span><br/>                   | <span data-ttu-id="d7443-119">Winuser. h</span><span class="sxs-lookup"><span data-stu-id="d7443-119">Winuser.h</span></span> |
