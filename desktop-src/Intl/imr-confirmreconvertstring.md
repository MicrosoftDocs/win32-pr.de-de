---
description: Benachrichtigt eine Anwendung, wenn der IME die reconvertstring-Struktur ändern muss. Die Anwendung empfängt diesen Befehl über die WM- \_ IME- \_ Anforderungs Nachricht mit den Parametereinstellungen, wie unten gezeigt.
ms.assetid: 035a7072-d292-4883-bc3e-d1e9ed64d9ec
title: IMR_CONFIRMRECONVERTSTRING Benachrichtigungs Code (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c500a155be14f447bb07ad506e12d5bece66e225
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756493"
---
# <a name="imr_confirmreconvertstring-notification-code"></a><span data-ttu-id="e9c9a-104">IMR \_ confirmreconvertstring-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="e9c9a-104">IMR\_CONFIRMRECONVERTSTRING notification code</span></span>

<span data-ttu-id="e9c9a-105">Benachrichtigt eine Anwendung, wenn der IME die [**reconvertstring**](/windows/win32/api/imm/ns-imm-reconvertstring) -Struktur ändern muss.</span><span class="sxs-lookup"><span data-stu-id="e9c9a-105">Notifies an application when the IME needs to change the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure.</span></span> <span data-ttu-id="e9c9a-106">Die Anwendung empfängt diesen Befehl über die [**WM- \_ IME- \_ Anforderungs**](wm-ime-request.md) Nachricht mit den Parametereinstellungen, wie unten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="e9c9a-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMR_CONFIRMRECONVERTSTRING
```



## <a name="parameters"></a><span data-ttu-id="e9c9a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9c9a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9c9a-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="e9c9a-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="e9c9a-109">Legen Sie auf IMR \_ confirmreconvertstring fest.</span><span class="sxs-lookup"><span data-stu-id="e9c9a-109">Set to IMR\_CONFIRMRECONVERTSTRING.</span></span>

</dd> <dt>

<span data-ttu-id="e9c9a-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="e9c9a-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="e9c9a-111">Zeiger auf eine [**reconvertstring**](/windows/win32/api/imm/ns-imm-reconvertstring) -Struktur aus dem IME.</span><span class="sxs-lookup"><span data-stu-id="e9c9a-111">Pointer to a [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure from the IME.</span></span> <span data-ttu-id="e9c9a-112">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="e9c9a-112">For more information, see the Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9c9a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e9c9a-113">Return Value</span></span>

<span data-ttu-id="e9c9a-114">Gibt einen Wert ungleich 0 (null) zurück, wenn die Anwendung die geänderte [**reconvertstring**](/windows/win32/api/imm/ns-imm-reconvertstring) -Struktur akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="e9c9a-114">Returns a nonzero value if the application accepts the changed [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure.</span></span> <span data-ttu-id="e9c9a-115">Andernfalls gibt der Befehl 0 zurück, und der IME verwendet die ursprüngliche **reconvertstring** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e9c9a-115">Otherwise, the command returns 0 and the IME uses the original **RECONVERTSTRING** structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9c9a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9c9a-116">Remarks</span></span>

<span data-ttu-id="e9c9a-117">Die Anwendung füllt die [**reconvertstring**](/windows/win32/api/imm/ns-imm-reconvertstring) -Struktur auf, wenn der [IMR \_ reconvertstring](imr-reconvertstring.md) -Befehl empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="e9c9a-117">The application fills in the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure upon receiving the [IMR\_RECONVERTSTRING](imr-reconvertstring.md) command.</span></span>

<span data-ttu-id="e9c9a-118">Nachdem die Anwendung [IMR \_ reconvertstring](imr-reconvertstring.md)verarbeitet hat, kann der IME die [**reconvertstring**](/windows/win32/api/imm/ns-imm-reconvertstring) -Struktur ggf. nicht mehr anpassen.</span><span class="sxs-lookup"><span data-stu-id="e9c9a-118">After the application has handled [IMR\_RECONVERTSTRING](imr-reconvertstring.md), the IME might or might not adjust the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure.</span></span> <span data-ttu-id="e9c9a-119">Der IME sendet eine WM \_ IME- \_ Anforderung mit **IMR \_ confirmreconvertstring** , um die Änderungen an der **reconvertstring** -Struktur zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="e9c9a-119">The IME sends WM\_IME\_REQUEST with **IMR\_CONFIRMRECONVERTSTRING** to confirm the changes to the **RECONVERTSTRING** structure.</span></span> <span data-ttu-id="e9c9a-120">Wenn die Anwendung **true** für **IMR \_ confirmreconvertstring** zurückgibt, generiert der IME eine neue Kompositions Zeichenfolge auf der Grundlage der **reconvertstring** -Struktur für den **IMR \_ confirmreconvertstring** -Befehl.</span><span class="sxs-lookup"><span data-stu-id="e9c9a-120">If the application returns **TRUE** for **IMR\_CONFIRMRECONVERTSTRING**, the IME generates a new composition string based on the **RECONVERTSTRING** structure for the **IMR\_CONFIRMRECONVERTSTRING** command.</span></span> <span data-ttu-id="e9c9a-121">Wenn die Anwendung für **IMR \_ confirmreconvertstring** **false** zurückgibt, generiert der IME eine neue Kompositions Zeichenfolge auf der Grundlage der ursprünglichen **reconvertstring** -Struktur, die von der Anwendung im IMR- \_ Befehl "reconvertstring" angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e9c9a-121">If the application returns **FALSE** for **IMR\_CONFIRMRECONVERTSTRING**, the IME generates a new composition string based on the original **RECONVERTSTRING** structure specified by the application in the IMR\_RECONVERTSTRING command.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9c9a-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9c9a-122">Requirements</span></span>



| <span data-ttu-id="e9c9a-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e9c9a-123">Requirement</span></span> | <span data-ttu-id="e9c9a-124">Wert</span><span class="sxs-lookup"><span data-stu-id="e9c9a-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9c9a-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e9c9a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e9c9a-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9c9a-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e9c9a-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e9c9a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e9c9a-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9c9a-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e9c9a-129">Header</span><span class="sxs-lookup"><span data-stu-id="e9c9a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9c9a-130"><dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9c9a-130"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9c9a-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9c9a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9c9a-132">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="e9c9a-132">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="e9c9a-133">Eingabemethoden-Manager-Befehle</span><span class="sxs-lookup"><span data-stu-id="e9c9a-133">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="e9c9a-134">IMR \_ reconvertstring</span><span class="sxs-lookup"><span data-stu-id="e9c9a-134">IMR\_RECONVERTSTRING</span></span>](imr-reconvertstring.md)
</dt> <dt>

[<span data-ttu-id="e9c9a-135">**Reconvertstring**</span><span class="sxs-lookup"><span data-stu-id="e9c9a-135">**RECONVERTSTRING**</span></span>](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[<span data-ttu-id="e9c9a-136">**WM- \_ IME- \_ Anforderung**</span><span class="sxs-lookup"><span data-stu-id="e9c9a-136">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> </dl>

 

 




