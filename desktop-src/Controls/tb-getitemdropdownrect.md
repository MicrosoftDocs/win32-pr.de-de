---
title: TB_GETITEMDROPDOWNRECT Meldung (kommstrg. h)
description: Ruft das umgebende Rechteck des Dropdown Fensters für ein Symbolleisten Element mit der btns-Dropdown Liste für den Stil \_ ab.
ms.assetid: 4b59c96b-8d75-44c1-b771-c1d62502a2c2
keywords:
- Windows-Steuerelemente für TB_GETITEMDROPDOWNRECT Meldung
topic_type:
- apiref
api_name:
- TB_GETITEMDROPDOWNRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbcbcef725b0ade0bfc776200fa5b191618d2ccb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040231"
---
# <a name="tb_getitemdropdownrect-message"></a><span data-ttu-id="dccab-104">TB \_ getitemdropdownrect-Meldung</span><span class="sxs-lookup"><span data-stu-id="dccab-104">TB\_GETITEMDROPDOWNRECT message</span></span>

<span data-ttu-id="dccab-105">Ruft das umgebende Rechteck des Dropdown Fensters für ein Symbolleisten Element mit der [**btns- \_ Dropdown**](toolbar-control-and-button-styles.md)Liste für den Stil ab.</span><span class="sxs-lookup"><span data-stu-id="dccab-105">Gets the bounding rectangle of the dropdown window for a toolbar item with style [**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="dccab-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dccab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dccab-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dccab-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dccab-108">Der null basierte Index des Symbolleisten-Steuer Elements, für das das umgebende Rechteck abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="dccab-108">The zero-based index of the toolbar control item for which to retrieve the bounding rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="dccab-109">*LPARAM* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="dccab-109">*lParam* \[in, out\]</span></span>
</dt> <dd><span data-ttu-id="dccab-110">Ein Zeiger auf eine <a href="/previous-versions//dd162897(v=vs.85)">**Rect**</a> -Struktur, um die umschließenden Rechteck Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="dccab-110">A pointer to a <a href="/previous-versions//dd162897(v=vs.85)">**RECT**</a> structure to receive the bounding rectangle information.</span></span> <span data-ttu-id="dccab-111">Der Absender der Nachricht ist für die Zuordnung dieser Struktur verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="dccab-111">The message sender is responsible for allocating this structure.</span></span> <span data-ttu-id="dccab-112">Die in der **Rect** -Struktur zurückgegebenen Koordinaten werden als Client Koordinaten ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="dccab-112">The coordinates returned in the **RECT** structure are expressed as client coordinates.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dccab-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dccab-113">Return value</span></span>

<span data-ttu-id="dccab-114">Gibt immer einen Wert ungleich 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="dccab-114">Always returns nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="dccab-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dccab-115">Remarks</span></span>

<span data-ttu-id="dccab-116">Das Element muss den [**btns- \_ Dropdown**](toolbar-control-and-button-styles.md) Stil aufweisen.</span><span class="sxs-lookup"><span data-stu-id="dccab-116">The item must have the [**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="dccab-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dccab-117">Requirements</span></span>



| <span data-ttu-id="dccab-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dccab-118">Requirement</span></span> | <span data-ttu-id="dccab-119">Wert</span><span class="sxs-lookup"><span data-stu-id="dccab-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dccab-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dccab-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dccab-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dccab-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dccab-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dccab-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dccab-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dccab-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dccab-124">Header</span><span class="sxs-lookup"><span data-stu-id="dccab-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="dccab-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="dccab-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

