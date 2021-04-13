---
description: Bereinigt den Zustand für die Sitzung, die geöffnet wird, oder die aktuell geöffnete Sitzung.
ms.assetid: 8247AFA9-F471-4CCD-972D-D0C827E86880
title: WF-displaysink CloseSession-Funktion (wsdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDCloseDisplaySinkSession
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 7697bc7ff1aa42569cf954b3f0b037f66ec67ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528160"
---
# <a name="wfddisplaysinkclosesession-function"></a><span data-ttu-id="cae6e-103">WF-displaysink CloseSession-Funktion</span><span class="sxs-lookup"><span data-stu-id="cae6e-103">WFDDisplaySinkCloseSession function</span></span>

<span data-ttu-id="cae6e-104">Bereinigt den Zustand für die Sitzung, die geöffnet wird, oder die aktuell geöffnete Sitzung.</span><span class="sxs-lookup"><span data-stu-id="cae6e-104">Cleans up the state for the session being opened, or the currently open session.</span></span>

## <a name="syntax"></a><span data-ttu-id="cae6e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cae6e-105">Syntax</span></span>


```C++
DWORD WINAPI WFDCloseDisplaySinkSession(
  _In_ HANDLE hSessionHandle
);
```



## <a name="parameters"></a><span data-ttu-id="cae6e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cae6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cae6e-107">*hsessionhandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cae6e-107">*hSessionHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cae6e-108">Das Handle, das über den letzten WFD-Aufruf empfangen wurde, zeigt den Rückruf Aufruf für [**\_ \_ \_ senkenbenachrichtigungen \_**](wfd-display-sink-notification-callback.md) an, der einen enthält</span><span class="sxs-lookup"><span data-stu-id="cae6e-108">The handle received via the most recent [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md) invocation that included one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cae6e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cae6e-109">Return value</span></span>

<span data-ttu-id="cae6e-110">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="cae6e-110">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

## <a name="remarks"></a><span data-ttu-id="cae6e-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cae6e-111">Remarks</span></span>

<span data-ttu-id="cae6e-112">Ihre APP kann diese Funktion zum Beenden der miracast-Sitzung aus irgendeinem Grund aufruft.</span><span class="sxs-lookup"><span data-stu-id="cae6e-112">Your app can call this function to terminate the Miracast session for any reason.</span></span> <span data-ttu-id="cae6e-113">Ihre APP muss nicht aufgerufen werden, wenn Sie den **disconnectednotification** -Typ im Rückruf empfängt.</span><span class="sxs-lookup"><span data-stu-id="cae6e-113">Your app is not required to call it when it receives the **DisconnectedNotification** type in its callback.</span></span>

## <a name="requirements"></a><span data-ttu-id="cae6e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cae6e-114">Requirements</span></span>



| <span data-ttu-id="cae6e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cae6e-115">Requirement</span></span> | <span data-ttu-id="cae6e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="cae6e-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="cae6e-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cae6e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cae6e-118">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="cae6e-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="cae6e-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cae6e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cae6e-120">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cae6e-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cae6e-121">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="cae6e-121">End of client support</span></span><br/>    | <span data-ttu-id="cae6e-122">Windows 10</span><span class="sxs-lookup"><span data-stu-id="cae6e-122">Windows 10</span></span><br/>                                                                      |
| <span data-ttu-id="cae6e-123">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="cae6e-123">End of server support</span></span><br/>    | <span data-ttu-id="cae6e-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="cae6e-124">Windows Server 2016</span></span><br/>                                                             |
| <span data-ttu-id="cae6e-125">Header</span><span class="sxs-lookup"><span data-stu-id="cae6e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cae6e-126"><dt>WF-Senke. h</dt></span><span class="sxs-lookup"><span data-stu-id="cae6e-126"><dt>Wfdsink.h</dt></span></span> </dl>       |
| <span data-ttu-id="cae6e-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cae6e-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="cae6e-128"><dt>Wifdisplay. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cae6e-128"><dt>Wifidisplay.lib</dt></span></span> </dl> |
| <span data-ttu-id="cae6e-129">DLL</span><span class="sxs-lookup"><span data-stu-id="cae6e-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cae6e-130"><dt>Wifidisplay.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cae6e-130"><dt>Wifidisplay.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cae6e-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cae6e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cae6e-132">**WFD- \_ Anzeige \_ Senke- \_ Benachrichtigungs \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="cae6e-132">**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**</span></span>](wfd-display-sink-notification-callback.md)
</dt> </dl>

 

 




