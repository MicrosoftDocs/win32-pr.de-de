---
title: TB_SETBOUNDINGSIZE Meldung (kommstrg. h)
description: Legt die Begrenzungs Größe für ein mehrspaltige Symbolleisten-Steuerelement fest.
ms.assetid: f406d9e3-1c40-4317-8cf1-51706f4c6adf
keywords:
- Windows-Steuerelemente für TB_SETBOUNDINGSIZE Meldung
topic_type:
- apiref
api_name:
- TB_SETBOUNDINGSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 419595da16148f7382da5053d3187e9cce9e00a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858636"
---
# <a name="tb_setboundingsize-message"></a><span data-ttu-id="300d1-104">TB \_ setboundingsize-Meldung</span><span class="sxs-lookup"><span data-stu-id="300d1-104">TB\_SETBOUNDINGSIZE message</span></span>

<span data-ttu-id="300d1-105">\[Zur internen Verwendung vorgesehen. wird nicht für die Verwendung in Anwendungen empfohlen.</span><span class="sxs-lookup"><span data-stu-id="300d1-105">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="300d1-106">Diese Meldung wird möglicherweise in zukünftigen Versionen von Windows nicht mehr unterstützt.\]</span><span class="sxs-lookup"><span data-stu-id="300d1-106">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="300d1-107">Legt die Begrenzungs Größe für ein mehrspaltige Symbolleisten-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="300d1-107">Sets the bounding size for a multi-column toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="300d1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="300d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="300d1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="300d1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="300d1-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="300d1-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="300d1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="300d1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="300d1-112">Zeiger auf eine [**Größen**](/previous-versions//dd145106(v=vs.85)) Struktur, deren **CY** -Member die umgebende Höhe enthält.</span><span class="sxs-lookup"><span data-stu-id="300d1-112">Pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure whose **cy** member contains the bounding height.</span></span> <span data-ttu-id="300d1-113">Der **CX** -Member (die Breite) wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="300d1-113">The **cx** member (the width) is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="300d1-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="300d1-114">Return value</span></span>

<span data-ttu-id="300d1-115">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="300d1-115">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="300d1-116">Überlegungen zur Sicherheit</span><span class="sxs-lookup"><span data-stu-id="300d1-116">Security Considerations</span></span>

<span data-ttu-id="300d1-117">Die Verwendung dieser Nachricht kann die Sicherheit des Programms beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="300d1-117">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="300d1-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="300d1-118">Remarks</span></span>

<span data-ttu-id="300d1-119">Die Begrenzungs Größe steuert, wie Schaltflächen in Spalten angeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="300d1-119">The bounding size controls how buttons are organized into columns.</span></span> <span data-ttu-id="300d1-120">Wenn das Symbolleisten-Steuerelement nicht über das Format [**tbstyle \_ Ex \_ MultiColumn**](toolbar-extended-styles.md) verfügt, hat diese Nachricht keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="300d1-120">If the toolbar control does not have the [**TBSTYLE\_EX\_MULTICOLUMN**](toolbar-extended-styles.md) style, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="300d1-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="300d1-121">Requirements</span></span>



| <span data-ttu-id="300d1-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="300d1-122">Requirement</span></span> | <span data-ttu-id="300d1-123">Wert</span><span class="sxs-lookup"><span data-stu-id="300d1-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="300d1-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="300d1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="300d1-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="300d1-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="300d1-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="300d1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="300d1-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="300d1-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="300d1-128">Header</span><span class="sxs-lookup"><span data-stu-id="300d1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="300d1-129"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="300d1-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

