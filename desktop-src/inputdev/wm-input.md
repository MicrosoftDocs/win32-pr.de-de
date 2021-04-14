---
title: WM_INPUT Meldung (Winuser. h)
description: Wird an das Fenster gesendet, das roheingaben erhält. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: a014d68c-841c-4120-b752-4b3fac60e12d
keywords:
- Tastatur-und Maus Eingaben für WM_INPUT Nachricht
topic_type:
- apiref
api_name:
- WM_INPUT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 04/17/2020
ms.openlocfilehash: ffe64a5ca79bbe886ddae31661c06dae695259a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391793"
---
# <a name="wm_input-message"></a><span data-ttu-id="e2ebf-105">WM- \_ Eingabe Meldung</span><span class="sxs-lookup"><span data-stu-id="e2ebf-105">WM\_INPUT message</span></span>

<span data-ttu-id="e2ebf-106">Wird an das Fenster gesendet, das roheingaben erhält.</span><span class="sxs-lookup"><span data-stu-id="e2ebf-106">Sent to the window that is getting raw input.</span></span>

<span data-ttu-id="e2ebf-107">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="e2ebf-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```cpp
#define WM_INPUT 0x00FF
```

## <a name="parameters"></a><span data-ttu-id="e2ebf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2ebf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2ebf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e2ebf-109">*wParam*</span></span>

</dt> <dd>

<span data-ttu-id="e2ebf-110">Der Eingabecode.</span><span class="sxs-lookup"><span data-stu-id="e2ebf-110">The input code.</span></span> <span data-ttu-id="e2ebf-111">Verwenden Sie das Makro [**get \_ rawinput \_ Code \_ wParam**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) , um den Wert zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e2ebf-111">Use [**GET\_RAWINPUT\_CODE\_WPARAM**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) macro to get the value.</span></span>

<span data-ttu-id="e2ebf-112">Folgenden Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="e2ebf-112">Can be one of the following values:</span></span>

| <span data-ttu-id="e2ebf-113">Wert</span><span class="sxs-lookup"><span data-stu-id="e2ebf-113">Value</span></span> | <span data-ttu-id="e2ebf-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e2ebf-114">Meaning</span></span> |
|---|---|
| <span id="RIM_INPUT"></span><span id="rim_input"></span><dl> <span data-ttu-id="e2ebf-115"><dt>**Rand \_ Eingabe**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e2ebf-115"><dt>**RIM\_INPUT**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="e2ebf-116">Die Eingabe ist aufgetreten, während sich die Anwendung im Vordergrund befand.</span><span class="sxs-lookup"><span data-stu-id="e2ebf-116">Input occurred while the application was in the foreground.</span></span> </br> <span data-ttu-id="e2ebf-117">Die Anwendung muss [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) aufzurufen, damit das System eine Bereinigung durchführen kann.</span><span class="sxs-lookup"><span data-stu-id="e2ebf-117">The application must call [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) so the system can perform cleanup.</span></span> |
| <span id="RIM_INPUTSINK"></span><span id="rim_inputsink"></span><dl> <span data-ttu-id="e2ebf-118"><dt>**Rand \_ Inputsink**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e2ebf-118"><dt>**RIM\_INPUTSINK**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="e2ebf-119">Die Eingabe ist aufgetreten, während sich die Anwendung nicht im Vordergrund befand.</span><span class="sxs-lookup"><span data-stu-id="e2ebf-119">Input occurred while the application was not in the foreground.</span></span> |

</dd> <dt>

<span data-ttu-id="e2ebf-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2ebf-120">*lParam*</span></span> 

</dt> <dd>

<span data-ttu-id="e2ebf-121">Ein **hrawinput** -Handle für die [**rawinput**](/windows/win32/api/winuser/ns-winuser-rawinput) -Struktur, die die unformatierte Eingabe des Geräts enthält.</span><span class="sxs-lookup"><span data-stu-id="e2ebf-121">A **HRAWINPUT** handle to the [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) structure that contains the raw input from the device.</span></span> <span data-ttu-id="e2ebf-122">Verwenden Sie zum Abrufen der Rohdaten dieses Handle im-Befehl von " [**getrawinputdata**](/windows/win32/api/winuser/nf-winuser-getrawinputdata)".</span><span class="sxs-lookup"><span data-stu-id="e2ebf-122">To get the raw data, use this handle in the call to [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2ebf-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2ebf-123">Return value</span></span>

<span data-ttu-id="e2ebf-124">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e2ebf-124">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2ebf-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2ebf-125">Remarks</span></span>

<span data-ttu-id="e2ebf-126">Unformatierte Eingaben sind nur verfügbar, wenn die Anwendung [**registerrawinputdevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) mit gültigen Gerätespezifikationen aufruft.</span><span class="sxs-lookup"><span data-stu-id="e2ebf-126">Raw input is available only when the application calls [**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) with valid device specifications.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2ebf-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2ebf-127">Requirements</span></span>

| <span data-ttu-id="e2ebf-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2ebf-128">Requirement</span></span> | <span data-ttu-id="e2ebf-129">Wert</span><span class="sxs-lookup"><span data-stu-id="e2ebf-129">Value</span></span> |
|--------------------------|-------------------------------------------|
| <span data-ttu-id="e2ebf-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e2ebf-130">Minimum supported client</span></span> | <span data-ttu-id="e2ebf-131">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2ebf-131">Windows XP \[desktop apps only\]</span></span> |
| <span data-ttu-id="e2ebf-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e2ebf-132">Minimum supported server</span></span> | <span data-ttu-id="e2ebf-133">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2ebf-133">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="e2ebf-134">Header</span><span class="sxs-lookup"><span data-stu-id="e2ebf-134">Header</span></span> | <dl> <span data-ttu-id="e2ebf-135"><dt>**Winuser. h (Windows. h einschließen)**</dt></span><span class="sxs-lookup"><span data-stu-id="e2ebf-135"><dt>**Winuser.h (include Windows.h)** </dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="e2ebf-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2ebf-136">See also</span></span>

<span data-ttu-id="e2ebf-137">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="e2ebf-137">**Reference**</span></span>

[<span data-ttu-id="e2ebf-138">**Getrawinputdata**</span><span class="sxs-lookup"><span data-stu-id="e2ebf-138">**GetRawInputData**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputdata)

[<span data-ttu-id="e2ebf-139">**Registerrawinputdevices**</span><span class="sxs-lookup"><span data-stu-id="e2ebf-139">**RegisterRawInputDevices**</span></span>](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[<span data-ttu-id="e2ebf-140">**Rawinput**</span><span class="sxs-lookup"><span data-stu-id="e2ebf-140">**RAWINPUT**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinput)

[<span data-ttu-id="e2ebf-141">**GET \_ rawinput \_ Code \_ wParam**</span><span class="sxs-lookup"><span data-stu-id="e2ebf-141">**GET\_RAWINPUT\_CODE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam)

<span data-ttu-id="e2ebf-142">**Licher**</span><span class="sxs-lookup"><span data-stu-id="e2ebf-142">**Conceptual**</span></span>

[<span data-ttu-id="e2ebf-143">Rohdaten Eingabe</span><span class="sxs-lookup"><span data-stu-id="e2ebf-143">Raw Input</span></span>](raw-input.md)
