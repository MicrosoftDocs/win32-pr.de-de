---
title: EM_SETTARGETDEVICE Meldung (RichEdit. h)
description: Legt das Zielgerät und die für \ 0034 verwendete Linienbreite fest. was Sie sehen, ist das, was Sie erhalten \ 0034; (WYSIWYG) Formatierung in einem Rich-Edit-Steuerelement.
ms.assetid: dfc829f5-e711-419e-abb5-c1e8df994c4a
keywords:
- Windows-Steuerelemente für EM_SETTARGETDEVICE Meldung
topic_type:
- apiref
api_name:
- EM_SETTARGETDEVICE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f82d6ee5df86572564cffcf192395ccee1fbd05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104216"
---
# <a name="em_settargetdevice-message"></a><span data-ttu-id="9b151-104">EM \_ SetTargetDevice-Meldung</span><span class="sxs-lookup"><span data-stu-id="9b151-104">EM\_SETTARGETDEVICE message</span></span>

<span data-ttu-id="9b151-105">Legt das Zielgerät und die Linienbreite fest, die für die Formatierung "was Sie sehen, was Sie erhalten" (WYSIWYG) in einem Rich-Edit-Steuerelement verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9b151-105">Sets the target device and line width used for "what you see is what you get" (WYSIWYG) formatting in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9b151-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b151-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b151-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9b151-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b151-108">HDC für das Zielgerät.</span><span class="sxs-lookup"><span data-stu-id="9b151-108">HDC for the target device.</span></span>

</dd> <dt>

<span data-ttu-id="9b151-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9b151-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b151-110">Linienstärke, die für die Formatierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b151-110">Line width to use for formatting.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b151-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9b151-111">Return value</span></span>

<span data-ttu-id="9b151-112">Der Rückgabewert ist 0 (null), wenn der Vorgang fehlschlägt, oder ungleich NULL, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="9b151-112">The return value is zero if the operation fails, or nonzero if it succeeds.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b151-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b151-113">Remarks</span></span>

<span data-ttu-id="9b151-114">Der HDC für den Standarddrucker kann wie folgt abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="9b151-114">The HDC for the default printer can be obtained as follows.</span></span>


```
PRINTDLG pd = { sizeof(pd) };
pd.Flags = PD_RETURNDC | PD_RETURNDEFAULT;
if (PrintDlg(&pd))
{
    HDC hdc = pd.hDC;
    ...
}
```



<span data-ttu-id="9b151-115">Wenn *LPARAM* gleich 0 (null) ist, werden keine Zeilenumbrüche erstellt.</span><span class="sxs-lookup"><span data-stu-id="9b151-115">If *lParam* is zero, no line breaks are created.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b151-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b151-116">Requirements</span></span>



| <span data-ttu-id="9b151-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b151-117">Requirement</span></span> | <span data-ttu-id="9b151-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9b151-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9b151-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9b151-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9b151-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9b151-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9b151-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9b151-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9b151-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9b151-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9b151-123">Header</span><span class="sxs-lookup"><span data-stu-id="9b151-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b151-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b151-124"><dt>Richedit.h</dt></span></span> </dl> |



 

 





