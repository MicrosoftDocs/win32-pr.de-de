---
title: WM_INPUT_DEVICE_CHANGE Meldung (Winuser. h)
description: Wird an das Fenster gesendet, das für den Empfang von roheingaben registriert ist. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: 2f98d8ea-b47b-4dea-9c38-f9697b18053a
keywords:
- Tastatur-und Maus Eingaben für WM_INPUT_DEVICE_CHANGE Nachricht
topic_type:
- apiref
api_name:
- WM_INPUT_DEVICE_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0edb6dbfbcfa9e024ba85613e3b7671e5f416397
ms.sourcegitcommit: 47d1f3859035a69340571bf50c3d36e0abeb2126
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "104039783"
---
# <a name="wm_input_device_change-message"></a><span data-ttu-id="88777-105">WM_INPUT_DEVICE_CHANGE Meldung</span><span class="sxs-lookup"><span data-stu-id="88777-105">WM_INPUT_DEVICE_CHANGE message</span></span>

## <a name="description"></a><span data-ttu-id="88777-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="88777-106">Description</span></span>

<span data-ttu-id="88777-107">Wird an das Fenster gesendet, das für den Empfang von roheingaben registriert ist.</span><span class="sxs-lookup"><span data-stu-id="88777-107">Sent to the window that registered to receive raw input.</span></span> 

<span data-ttu-id="88777-108">Unformatierte Eingabe Benachrichtigungen sind erst verfügbar, nachdem die Anwendung [registerrawinputdevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) mit [RIDEV_DEVNOTIFY](/windows/win32/api/winuser/ns-winuser-rawinputdevice) -Flag aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="88777-108">Raw input notifications are available only after the application calls [RegisterRawInputDevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) with [RIDEV_DEVNOTIFY](/windows/win32/api/winuser/ns-winuser-rawinputdevice) flag.</span></span>

<span data-ttu-id="88777-109">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="88777-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

```C++
#define WM_INPUT_DEVICE_CHANGE          0x00FE
```

## <a name="parameters"></a><span data-ttu-id="88777-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="88777-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88777-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="88777-111">*wParam*</span></span>

</dt> <dd>

<span data-ttu-id="88777-112">Typ: **wParam**</span><span class="sxs-lookup"><span data-stu-id="88777-112">Type: **WPARAM**</span></span>

<span data-ttu-id="88777-113">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="88777-113">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="88777-114">Wert</span><span class="sxs-lookup"><span data-stu-id="88777-114">Value</span></span>                    | <span data-ttu-id="88777-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="88777-115">Meaning</span></span>                                    |
|--------------------------|--------------------------------------------|
| <span data-ttu-id="88777-116">**gidc- \_ Ankunft**</span><span class="sxs-lookup"><span data-stu-id="88777-116">**GIDC\_ARRIVAL**</span></span> </br><span data-ttu-id="88777-117">1</span><span class="sxs-lookup"><span data-stu-id="88777-117">1</span></span> | <span data-ttu-id="88777-118">Dem System wurde ein neues Gerät hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="88777-118">A new device has been added to the system.</span></span> </br> <span data-ttu-id="88777-119">Sie können " [getrawinputdeviceinfo](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) " anrufen, um weitere Informationen zum Gerät zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="88777-119">You can call [GetRawInputDeviceInfo](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) to get more information regarding the device.</span></span> |
| <span data-ttu-id="88777-120">**Entfernen von gidc \_**</span><span class="sxs-lookup"><span data-stu-id="88777-120">**GIDC\_REMOVAL**</span></span> </br><span data-ttu-id="88777-121">2</span><span class="sxs-lookup"><span data-stu-id="88777-121">2</span></span> | <span data-ttu-id="88777-122">Ein Gerät wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="88777-122">A device has been removed from the system.</span></span> |

</dd> <dt>

<span data-ttu-id="88777-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="88777-123">*lParam*</span></span> 

</dt> <dd>

<span data-ttu-id="88777-124">Typ: **LPARAM**</span><span class="sxs-lookup"><span data-stu-id="88777-124">Type: **LPARAM**</span></span>

<span data-ttu-id="88777-125">Das **handle** für das unformatierte Eingabegerät.</span><span class="sxs-lookup"><span data-stu-id="88777-125">The **HANDLE** to the raw input device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88777-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="88777-126">Return value</span></span>

<span data-ttu-id="88777-127">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="88777-127">If an application processes this message, it should return zero.</span></span>

## <a name="see-also"></a><span data-ttu-id="88777-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88777-128">See also</span></span>

<span data-ttu-id="88777-129">**Licher**</span><span class="sxs-lookup"><span data-stu-id="88777-129">**Conceptual**</span></span>

[<span data-ttu-id="88777-130">Rohdaten Eingabe</span><span class="sxs-lookup"><span data-stu-id="88777-130">Raw Input</span></span>](/windows/desktop/inputdev/raw-input)

<span data-ttu-id="88777-131">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="88777-131">**Reference**</span></span>

[<span data-ttu-id="88777-132">Registerrawinputdevices</span><span class="sxs-lookup"><span data-stu-id="88777-132">RegisterRawInputDevices</span></span>](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[<span data-ttu-id="88777-133">RAWINPUTDEVICE-Struktur</span><span class="sxs-lookup"><span data-stu-id="88777-133">RAWINPUTDEVICE structure</span></span>](/windows/win32/api/winuser/ns-winuser-rawinputdevice)
 

