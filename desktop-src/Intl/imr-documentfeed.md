---
description: Benachrichtigt eine Anwendung, wenn der ausgewählte IME die konvertierte Zeichenfolge aus der Anwendung benötigt. Die Anwendung empfängt diesen Befehl über die WM- \_ IME- \_ Anforderungs Nachricht mit den festgelegten Parametern, wie unten gezeigt.
ms.assetid: 1a007bed-15e5-4400-9d2f-32e37e1765d2
title: IMR_DOCUMENTFEED Benachrichtigungs Code (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc4fe46f95b7ad17ba7bb7850ec3fb9ca980519f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215922"
---
# <a name="imr_documentfeed-notification-code"></a><span data-ttu-id="2c4f0-104">IMR- \_ documentfeed-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="2c4f0-104">IMR\_DOCUMENTFEED notification code</span></span>

<span data-ttu-id="2c4f0-105">Benachrichtigt eine Anwendung, wenn der ausgewählte IME die konvertierte Zeichenfolge aus der Anwendung benötigt.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-105">Notifies an application when the selected IME needs the converted string from the application.</span></span> <span data-ttu-id="2c4f0-106">Die Anwendung empfängt diesen Befehl über die [**WM- \_ IME- \_ Anforderungs**](wm-ime-request.md) Nachricht mit den festgelegten Parametern, wie unten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameters set as shown below.</span></span>


```C++
LRESULT IMR_DOCUMENTFEED
```



## <a name="parameters"></a><span data-ttu-id="2c4f0-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c4f0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c4f0-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="2c4f0-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="2c4f0-109">Legen Sie auf IMR \_ documentfeed fest.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-109">Set to IMR\_DOCUMENTFEED.</span></span>

</dd> <dt>

<span data-ttu-id="2c4f0-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="2c4f0-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="2c4f0-111">Zeiger auf einen Puffer, der die [**reconvertstring**](/windows/win32/api/imm/ns-imm-reconvertstring) -Struktur enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-111">Pointer to a buffer to contain the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c4f0-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2c4f0-112">Return Value</span></span>

<span data-ttu-id="2c4f0-113">Gibt die aktuelle Zeichen folgen Struktur der erneuten Konvertierung zurück.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-113">Returns the current reconversion string structure.</span></span> <span data-ttu-id="2c4f0-114">Wenn *LPARAM* auf **null** festgelegt ist, gibt die Anwendung die erforderliche Größe für den Puffer zum Speichern der Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-114">If *lParam* is set to **NULL**, the application returns the required size for the buffer to hold the structure.</span></span> <span data-ttu-id="2c4f0-115">Der Befehl gibt 0 (null) zurück, wenn er nicht erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-115">The command returns 0 if it does not succeed.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c4f0-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c4f0-116">Remarks</span></span>

<span data-ttu-id="2c4f0-117">Der IME speichert konvertierte Zeichen folgen für eine höhere Konvertierungs Genauigkeit zwischen.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-117">The IME caches converted strings for higher conversion accuracy.</span></span> <span data-ttu-id="2c4f0-118">Eine zwischen Speicherungs Einschränkung für den IME besteht darin, dass die konvertierte Zeichenfolge in den folgenden Situationen verloren geht:</span><span class="sxs-lookup"><span data-stu-id="2c4f0-118">One caching limitation of the IME is that it loses the converted string under the following circumstances:</span></span>

-   <span data-ttu-id="2c4f0-119">Die Position der Einfügemarke für die Anwendung wird durch einen Schlüssel verschoben, z. b. eine Cursor Taste.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-119">The caret position for the application is moved by a key, for example, a cursor key.</span></span>
-   <span data-ttu-id="2c4f0-120">Die Position der Einfügemarke für die Anwendung wird mit der Maus bewegt.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-120">The caret position for the application is moved by the mouse.</span></span>
-   <span data-ttu-id="2c4f0-121">Ein neues Dokument wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-121">A new document is opened.</span></span>

<span data-ttu-id="2c4f0-122">Mit dem **IMR \_ documentfeed** -Befehl kann der IME seine zwischengespeicherten Zeichen folgen jederzeit aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-122">With the **IMR\_DOCUMENTFEED** command, the IME can refresh its cached strings any time.</span></span> <span data-ttu-id="2c4f0-123">Die Verwendung dieses Befehls verbessert die Konvertierungs Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-123">Use of this command improves conversion accuracy.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c4f0-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c4f0-124">Requirements</span></span>



| <span data-ttu-id="2c4f0-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c4f0-125">Requirement</span></span> | <span data-ttu-id="2c4f0-126">Wert</span><span class="sxs-lookup"><span data-stu-id="2c4f0-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c4f0-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c4f0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2c4f0-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c4f0-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2c4f0-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c4f0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2c4f0-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c4f0-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2c4f0-131">Header</span><span class="sxs-lookup"><span data-stu-id="2c4f0-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c4f0-132"><dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c4f0-132"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c4f0-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c4f0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c4f0-134">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="2c4f0-134">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="2c4f0-135">Eingabemethoden-Manager-Befehle</span><span class="sxs-lookup"><span data-stu-id="2c4f0-135">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="2c4f0-136">**Reconvertstring**</span><span class="sxs-lookup"><span data-stu-id="2c4f0-136">**RECONVERTSTRING**</span></span>](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[<span data-ttu-id="2c4f0-137">**WM- \_ IME- \_ Anforderung**</span><span class="sxs-lookup"><span data-stu-id="2c4f0-137">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> </dl>

 

 




