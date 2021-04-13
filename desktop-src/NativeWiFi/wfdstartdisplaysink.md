---
description: Führt die erforderliche Initialisierung aus, damit die aufrufenden App eine miracast-Anzeige Senke werden kann.
ms.assetid: D87B427B-0B7F-44BB-BC34-726FDF87CCCC
title: Wsddisplaysink Start-Funktion (WF-Sink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDStartDisplaySink
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 423ca68364fbe7c4beb89ab3b1d9f8e8fdb891be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528157"
---
# <a name="wfddisplaysinkstart-function"></a><span data-ttu-id="40675-103">Wsddisplaysink Start-Funktion</span><span class="sxs-lookup"><span data-stu-id="40675-103">WFDDisplaySinkStart function</span></span>

<span data-ttu-id="40675-104">Führt die erforderliche Initialisierung aus, damit die aufrufenden App eine miracast-Anzeige Senke werden kann.</span><span class="sxs-lookup"><span data-stu-id="40675-104">Performs the necessary initialization to allow the calling app to become a Miracast display sink.</span></span> <span data-ttu-id="40675-105">Ihre APP sollte diese einmal beim Start abrufen.</span><span class="sxs-lookup"><span data-stu-id="40675-105">Your app should call this once on startup.</span></span>

## <a name="syntax"></a><span data-ttu-id="40675-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="40675-106">Syntax</span></span>


```C++
DWORD WINAPI WFDStartDisplaySink(
  _In_     USHORT                                 uDeviceCategory,
  _In_     USHORT                                 uSubCategory,
  _In_opt_ PVOID                                  pCallbackContext,
  _In_     WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK *pfnCallback
);
```



## <a name="parameters"></a><span data-ttu-id="40675-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="40675-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40675-108">*ude vicecategory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40675-108">*uDeviceCategory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40675-109">Die Gerätekategorie.</span><span class="sxs-lookup"><span data-stu-id="40675-109">The device category.</span></span>

</dd> <dt>

<span data-ttu-id="40675-110">*usubcategory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40675-110">*uSubCategory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40675-111">Die Unterkategorie des Geräts.</span><span class="sxs-lookup"><span data-stu-id="40675-111">The device subcategory.</span></span>

</dd> <dt>

<span data-ttu-id="40675-112">*pcallbackcontext* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="40675-112">*pCallbackContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="40675-113">Ein optionaler Kontext Zeiger, der an die Rückruffunktion übergeben wird, die im *pfncallback* -Parameter angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="40675-113">An optional context pointer which is passed to the callback function specified in the *pfnCallback* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="40675-114">*pfncallback* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40675-114">*pfnCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40675-115">Ein Zeiger auf die Rückruffunktion, die aufgerufen werden soll, wenn eine Benachrichtigung für die APP vorliegt.</span><span class="sxs-lookup"><span data-stu-id="40675-115">A pointer to the callback function to be called whenever there is a notification for the app.</span></span> <span data-ttu-id="40675-116">Benachrichtigungen, die gesendet werden können, werden in [**WFD- \_ \_ \_ Benachrichtigungs \_ Rückruf-Benachrichtigungs Rückruf**](wfd-display-sink-notification-callback.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="40675-116">Notifications that can be sent are described in [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40675-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="40675-117">Return value</span></span>

<span data-ttu-id="40675-118">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="40675-118">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="40675-119">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Rückgabecodes sein.</span><span class="sxs-lookup"><span data-stu-id="40675-119">If the function fails, the return value may be one of the following return codes.</span></span>



| <span data-ttu-id="40675-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="40675-120">Return code</span></span>                                                                                          | <span data-ttu-id="40675-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="40675-121">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="40675-122"><dt>**Fehler \_ nicht \_ unterstützt**</dt></span><span class="sxs-lookup"><span data-stu-id="40675-122"><dt>**ERROR\_NOT\_SUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="40675-123">Die Anzeige Senke wird auf dieser Hardware nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="40675-123">The display sink is not supported on this hardware.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="40675-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40675-124">Remarks</span></span>

<span data-ttu-id="40675-125">Diese Funktion führt die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="40675-125">This function performs the following tasks:</span></span>

-   <span data-ttu-id="40675-126">Macht den PC auffallen</span><span class="sxs-lookup"><span data-stu-id="40675-126">Makes the PC discoverable</span></span>
-   <span data-ttu-id="40675-127">Legt die P2P-Geräteinformationen so fest, dass Sie die angegebene Kategorie und Unterkategorie reflektieren.</span><span class="sxs-lookup"><span data-stu-id="40675-127">Sets the P2P device info to reflect the category and sub category specified</span></span>
-   <span data-ttu-id="40675-128">Legt die miracast-IES in allen Wi-Fi direkten Frames mit dem Gerätetyp als Senke fest.</span><span class="sxs-lookup"><span data-stu-id="40675-128">Sets the Miracast IEs on all Wi-Fi Direct frames with the device type as the sink</span></span>
-   <span data-ttu-id="40675-129">Registriert den angegebenen Rückruf, der immer dann aufgerufen wird, wenn eine eingehende Verbindung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="40675-129">Registers the specified callback to be invoked whenever there is an incoming connection</span></span>

## <a name="requirements"></a><span data-ttu-id="40675-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40675-130">Requirements</span></span>



| <span data-ttu-id="40675-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40675-131">Requirement</span></span> | <span data-ttu-id="40675-132">Wert</span><span class="sxs-lookup"><span data-stu-id="40675-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="40675-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="40675-133">Minimum supported client</span></span><br/> | <span data-ttu-id="40675-134">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="40675-134">Windows 8.1 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="40675-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="40675-135">Minimum supported server</span></span><br/> | <span data-ttu-id="40675-136">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="40675-136">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="40675-137">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="40675-137">End of client support</span></span><br/>    | <span data-ttu-id="40675-138">Windows 10</span><span class="sxs-lookup"><span data-stu-id="40675-138">Windows 10</span></span><br/>                                                                      |
| <span data-ttu-id="40675-139">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="40675-139">End of server support</span></span><br/>    | <span data-ttu-id="40675-140">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="40675-140">Windows Server 2016</span></span><br/>                                                             |
| <span data-ttu-id="40675-141">Header</span><span class="sxs-lookup"><span data-stu-id="40675-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="40675-142"><dt>WF-Senke. h</dt></span><span class="sxs-lookup"><span data-stu-id="40675-142"><dt>Wfdsink.h</dt></span></span> </dl>       |
| <span data-ttu-id="40675-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="40675-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="40675-144"><dt>Wifdisplay. lib</dt></span><span class="sxs-lookup"><span data-stu-id="40675-144"><dt>Wifidisplay.lib</dt></span></span> </dl> |
| <span data-ttu-id="40675-145">DLL</span><span class="sxs-lookup"><span data-stu-id="40675-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40675-146"><dt>Wifidisplay.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40675-146"><dt>Wifidisplay.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40675-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40675-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40675-148">**WFD- \_ Anzeige \_ Senke- \_ Benachrichtigungs \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="40675-148">**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**</span></span>](wfd-display-sink-notification-callback.md)
</dt> </dl>

 

 




