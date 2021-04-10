---
description: Benachrichtigt eine Anwendung, wenn eine ausgewählte IME eine Zeichenfolge für die erneute Konvertierung benötigt. Die Anwendung empfängt diesen Befehl über die WM- \_ IME- \_ Anforderungs Nachricht mit den Parametereinstellungen, wie unten gezeigt.
ms.assetid: 82ef20b5-bdfa-4bde-abb4-3d14ae35c116
title: IMR_RECONVERTSTRING Benachrichtigungs Code (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cbb1caeedb729b176f116a15e64879d79d519fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864883"
---
# <a name="imr_reconvertstring-notification-code"></a><span data-ttu-id="79900-104">IMR \_ reconvertstring-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="79900-104">IMR\_RECONVERTSTRING notification code</span></span>

<span data-ttu-id="79900-105">Benachrichtigt eine Anwendung, wenn eine ausgewählte IME eine Zeichenfolge für die erneute Konvertierung benötigt.</span><span class="sxs-lookup"><span data-stu-id="79900-105">Notifies an application when a selected IME needs a string for reconversion.</span></span> <span data-ttu-id="79900-106">Die Anwendung empfängt diesen Befehl über die [**WM- \_ IME- \_ Anforderungs**](wm-ime-request.md) Nachricht mit den Parametereinstellungen, wie unten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="79900-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMR_RECONVERTSTRING
```



## <a name="parameters"></a><span data-ttu-id="79900-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="79900-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79900-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="79900-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="79900-109">Legen Sie auf IMR \_ reconvertstring fest.</span><span class="sxs-lookup"><span data-stu-id="79900-109">Set to IMR\_RECONVERTSTRING.</span></span>

</dd> <dt>

<span data-ttu-id="79900-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="79900-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="79900-111">Zeiger auf einen Puffer, der die [**reconvertstring**](/windows/win32/api/imm/ns-imm-reconvertstring) -Struktur und Zeichen folgen enthält.</span><span class="sxs-lookup"><span data-stu-id="79900-111">Pointer to a buffer containing the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure and strings.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79900-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="79900-112">Return Value</span></span>

<span data-ttu-id="79900-113">Gibt die aktuelle Zeichen folgen Struktur der erneuten Konvertierung zurück.</span><span class="sxs-lookup"><span data-stu-id="79900-113">Returns the current reconversion string structure.</span></span> <span data-ttu-id="79900-114">Wenn *LPARAM* auf **null** festgelegt ist, gibt die Anwendung die Größe des Puffers zurück, der zum Speichern der Struktur erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="79900-114">If *lParam* is set to **NULL**, the application returns the size for the buffer required to hold the structure.</span></span> <span data-ttu-id="79900-115">Der Befehl gibt 0 (null) zurück, wenn er nicht erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="79900-115">The command returns 0 if it does not succeed.</span></span>

## <a name="requirements"></a><span data-ttu-id="79900-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79900-116">Requirements</span></span>



| <span data-ttu-id="79900-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79900-117">Requirement</span></span> | <span data-ttu-id="79900-118">Wert</span><span class="sxs-lookup"><span data-stu-id="79900-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79900-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="79900-119">Minimum supported client</span></span><br/> | <span data-ttu-id="79900-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79900-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="79900-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="79900-121">Minimum supported server</span></span><br/> | <span data-ttu-id="79900-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79900-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="79900-123">Header</span><span class="sxs-lookup"><span data-stu-id="79900-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="79900-124"><dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="79900-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79900-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79900-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79900-126">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="79900-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="79900-127">Eingabemethoden-Manager-Befehle</span><span class="sxs-lookup"><span data-stu-id="79900-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="79900-128">**Reconvertstring**</span><span class="sxs-lookup"><span data-stu-id="79900-128">**RECONVERTSTRING**</span></span>](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[<span data-ttu-id="79900-129">**WM- \_ IME- \_ Anforderung**</span><span class="sxs-lookup"><span data-stu-id="79900-129">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> </dl>

 

 




