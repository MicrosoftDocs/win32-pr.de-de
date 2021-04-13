---
title: CB_GETCOMBOBOXINFO Meldung (Winuser. h)
description: Ruft Informationen über das angegebene Kombinations Feld ab.
ms.assetid: 3239dfa8-7301-48e3-ba8e-29c5d5f43b39
keywords:
- Windows-Steuerelemente für CB_GETCOMBOBOXINFO Meldung
topic_type:
- apiref
api_name:
- CB_GETCOMBOBOXINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd7052ef4feca8a8704258c7c34d6516c7cd6cd4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475408"
---
# <a name="cb_getcomboboxinfo-message"></a><span data-ttu-id="7725a-104">CB \_ getcomboboxinfo-Meldung</span><span class="sxs-lookup"><span data-stu-id="7725a-104">CB\_GETCOMBOBOXINFO message</span></span>

<span data-ttu-id="7725a-105">Ruft Informationen über das angegebene Kombinations Feld ab.</span><span class="sxs-lookup"><span data-stu-id="7725a-105">Gets information about the specified combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="7725a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7725a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7725a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7725a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7725a-108">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="7725a-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7725a-109">*LPARAM* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7725a-109">*lParam* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7725a-110">Ein Zeiger auf eine [**comboboxinfo**](/windows/win32/api/winuser/ns-winuser-comboboxinfo) -Struktur, die die Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="7725a-110">A pointer to a [**COMBOBOXINFO**](/windows/win32/api/winuser/ns-winuser-comboboxinfo) structure that receives the information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7725a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7725a-111">Return value</span></span>

<span data-ttu-id="7725a-112">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ungleich Null.</span><span class="sxs-lookup"><span data-stu-id="7725a-112">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="7725a-113">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="7725a-113">If the function fails, the return value is zero.</span></span> <span data-ttu-id="7725a-114">Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.</span><span class="sxs-lookup"><span data-stu-id="7725a-114">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="7725a-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7725a-115">Remarks</span></span>

<span data-ttu-id="7725a-116">Diese Meldung entspricht [**getcomboboxinfo**](/windows/desktop/api/Winuser/nf-winuser-getcomboboxinfo).</span><span class="sxs-lookup"><span data-stu-id="7725a-116">This message is equivalent to [**GetComboBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getcomboboxinfo).</span></span>

## <a name="requirements"></a><span data-ttu-id="7725a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7725a-117">Requirements</span></span>



| <span data-ttu-id="7725a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7725a-118">Requirement</span></span> | <span data-ttu-id="7725a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="7725a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7725a-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7725a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7725a-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7725a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7725a-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7725a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7725a-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7725a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7725a-124">Header</span><span class="sxs-lookup"><span data-stu-id="7725a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7725a-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="7725a-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7725a-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7725a-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="7725a-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="7725a-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7725a-128">**Comboboxinfo**</span><span class="sxs-lookup"><span data-stu-id="7725a-128">**COMBOBOXINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-comboboxinfo)
</dt> <dt>

[<span data-ttu-id="7725a-129">**Getcomboboxinfo**</span><span class="sxs-lookup"><span data-stu-id="7725a-129">**GetComboBoxInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getcomboboxinfo)
</dt> </dl>

 

