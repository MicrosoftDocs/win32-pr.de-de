---
title: TB_GETMAXSIZE Meldung (kommstrg. h)
description: Ruft die Gesamtgröße aller sichtbaren Schaltflächen und Trennzeichen auf der Symbolleiste ab.
ms.assetid: 560e6ce2-00ef-46c3-b1d8-fbe0ac79c888
keywords:
- Windows-Steuerelemente für TB_GETMAXSIZE Meldung
topic_type:
- apiref
api_name:
- TB_GETMAXSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4829e65d90c04181369dd73b9c54634f1077144
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346318"
---
# <a name="tb_getmaxsize-message"></a><span data-ttu-id="96849-104">TB \_ getmaxsize-Nachricht</span><span class="sxs-lookup"><span data-stu-id="96849-104">TB\_GETMAXSIZE message</span></span>

<span data-ttu-id="96849-105">Ruft die Gesamtgröße aller sichtbaren Schaltflächen und Trennzeichen auf der Symbolleiste ab.</span><span class="sxs-lookup"><span data-stu-id="96849-105">Retrieves the total size of all of the visible buttons and separators in the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="96849-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="96849-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96849-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="96849-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="96849-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="96849-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="96849-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="96849-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96849-110">Ein Zeiger auf eine [**Größen**](/previous-versions//dd145106(v=vs.85)) Struktur, die die Größe der Elemente empfängt.</span><span class="sxs-lookup"><span data-stu-id="96849-110">Pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure that receives the size of the items.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96849-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="96849-111">Return value</span></span>

<span data-ttu-id="96849-112">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="96849-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="96849-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96849-113">Requirements</span></span>



| <span data-ttu-id="96849-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96849-114">Requirement</span></span> | <span data-ttu-id="96849-115">Wert</span><span class="sxs-lookup"><span data-stu-id="96849-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96849-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="96849-116">Minimum supported client</span></span><br/> | <span data-ttu-id="96849-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="96849-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="96849-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="96849-118">Minimum supported server</span></span><br/> | <span data-ttu-id="96849-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="96849-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="96849-120">Header</span><span class="sxs-lookup"><span data-stu-id="96849-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="96849-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="96849-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

