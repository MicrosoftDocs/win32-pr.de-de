---
title: RB_PUSHCHEVRON Meldung (kommstrg. h)
description: Wird an ein Grund leisten-Steuerelement gesendet, um ein Chevron Programm gesteuert zu pushen.
ms.assetid: 00a8ce10-1fb2-488a-a6f9-1814f73f82bd
keywords:
- Windows-Steuerelemente für RB_PUSHCHEVRON Meldung
topic_type:
- apiref
api_name:
- RB_PUSHCHEVRON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e09e558d5574d4fd28cf01e9794657556dda4ae8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518275"
---
# <a name="rb_pushchevron-message"></a><span data-ttu-id="f53b4-104">RB \_ pushchevron-Nachricht</span><span class="sxs-lookup"><span data-stu-id="f53b4-104">RB\_PUSHCHEVRON message</span></span>

<span data-ttu-id="f53b4-105">Wird an ein Grund leisten-Steuerelement gesendet, um ein Chevron Programm gesteuert zu pushen.</span><span class="sxs-lookup"><span data-stu-id="f53b4-105">Sent to a rebar control to programmatically push a chevron.</span></span>

## <a name="parameters"></a><span data-ttu-id="f53b4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f53b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f53b4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f53b4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f53b4-108">NULL basierter Index des Bands, dessen Chevron per pushübertragung durchgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f53b4-108">Zero-based index of the band whose chevron is to be pushed.</span></span>

</dd> <dt>

<span data-ttu-id="f53b4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f53b4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f53b4-110">Ein von der Anwendung definierter 32-Bit-Wert.</span><span class="sxs-lookup"><span data-stu-id="f53b4-110">An application defined 32-bit value.</span></span> <span data-ttu-id="f53b4-111">Sie wird an die Anwendung als **lparamnm** -Member der [**nmrebarchevron**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) -Struktur zurückgegeben, die mit der [RBN- \_ chevronpushbenachrichtigung](rbn-chevronpushed.md) übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f53b4-111">It will be passed back to the application as the **lParamNM** member of the [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) structure that is passed with the [RBN\_CHEVRONPUSHED](rbn-chevronpushed.md) notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f53b4-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f53b4-112">Return value</span></span>

<span data-ttu-id="f53b4-113">Der Rückgabewert für diese Nachricht wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f53b4-113">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="f53b4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f53b4-114">Remarks</span></span>

<span data-ttu-id="f53b4-115">Wenn diese Nachricht gesendet wird, sendet das Grund leisten-Steuerelement der Anwendung einen [RBN- \_ chevronpushbenachrichtigungscode](rbn-chevronpushed.md) , der Sie auffordert, das Chevron-Menü anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f53b4-115">When this message is sent, the rebar control will send the application an [RBN\_CHEVRONPUSHED](rbn-chevronpushed.md) notification code, prompting it to display the chevron menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="f53b4-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f53b4-116">Requirements</span></span>



| <span data-ttu-id="f53b4-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f53b4-117">Requirement</span></span> | <span data-ttu-id="f53b4-118">Wert</span><span class="sxs-lookup"><span data-stu-id="f53b4-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f53b4-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f53b4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f53b4-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f53b4-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f53b4-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f53b4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f53b4-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f53b4-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f53b4-123">Header</span><span class="sxs-lookup"><span data-stu-id="f53b4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f53b4-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f53b4-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





