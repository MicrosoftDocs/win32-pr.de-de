---
description: 'Die IWiaDevMgr2:: registereventcallbackprogram-Methode registriert eine Anwendung, um Geräte Ereignisse zu empfangen. Es wird hauptsächlich aus Gründen der Abwärtskompatibilität mit Anwendungen bereitgestellt, die nicht für die Windows-Abbild Beschaffung (WIA) 2,0 geschrieben wurden.'
ms.assetid: 6b427f19-719b-44ce-8e2c-3c44672345c8
title: 'IWiaDevMgr2:: registereventcallbackprogram-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackProgram
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 9b18b5833b7616493c24f0128caa7c910b685e37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353134"
---
# <a name="iwiadevmgr2registereventcallbackprogram-method"></a><span data-ttu-id="1b99f-104">IWiaDevMgr2:: registereventcallbackprogram-Methode</span><span class="sxs-lookup"><span data-stu-id="1b99f-104">IWiaDevMgr2::RegisterEventCallbackProgram method</span></span>

<span data-ttu-id="1b99f-105">Die **IWiaDevMgr2:: registereventcallbackprogram** -Methode registriert eine Anwendung, um Geräte Ereignisse zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="1b99f-105">The **IWiaDevMgr2::RegisterEventCallbackProgram** method registers an application to receive device events.</span></span> <span data-ttu-id="1b99f-106">Es wird hauptsächlich aus Gründen der Abwärtskompatibilität mit Anwendungen bereitgestellt, die nicht für die Windows-Abbild Beschaffung (WIA) 2,0 geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="1b99f-106">It is primarily provided for backward compatibility with applications that were not written for Windows Image Acquisition (WIA) 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b99f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b99f-107">Syntax</span></span>


```C++
HRESULT RegisterEventCallbackProgram(
  [in]       LONG lFlags,
  [in]       BSTR bstrDeviceID,
  [in] const GUID *pEventGUID,
  [in]       BSTR bstrFullAppName,
  [in]       BSTR bstrCommandlineArg,
  [in]       BSTR bstrName,
  [in]       BSTR bstrDescription,
  [in]       BSTR bstrIcon
);
```



## <a name="parameters"></a><span data-ttu-id="1b99f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b99f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b99f-109">*lFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b99f-109">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b99f-110">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="1b99f-110">Type: **LONG**</span></span>

<span data-ttu-id="1b99f-111">Die Registrierungsflags.</span><span class="sxs-lookup"><span data-stu-id="1b99f-111">The registration flags.</span></span> <span data-ttu-id="1b99f-112">Kann auf die folgenden Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1b99f-112">Can be set to the following values.</span></span>



| <span data-ttu-id="1b99f-113">Wert</span><span class="sxs-lookup"><span data-stu-id="1b99f-113">Value</span></span>                                                                                                                                                                                                           | <span data-ttu-id="1b99f-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1b99f-114">Meaning</span></span>                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="WIA_REGISTER_EVENT_CALLBACK"></span><span id="wia_register_event_callback"></span><dl> <span data-ttu-id="1b99f-115"><dt>**WIA- \_ Register \_ Ereignis \_ Rückruf**</dt></span><span class="sxs-lookup"><span data-stu-id="1b99f-115"><dt>**WIA\_REGISTER\_EVENT\_CALLBACK**</dt></span></span> </dl>       | <span data-ttu-id="1b99f-116">Registrieren Sie sich für das-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1b99f-116">Register for the event.</span></span><br/>                           |
| <span id="WIA_UNREGISTER_EVENT_CALLBACK"></span><span id="wia_unregister_event_callback"></span><dl> <span data-ttu-id="1b99f-117"><dt>**\_ \_ Ereignis Rückruf für die Aufhebung der Registrierung \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1b99f-117"><dt>**WIA\_UNREGISTER\_EVENT\_CALLBACK**</dt></span></span> </dl> | <span data-ttu-id="1b99f-118">Löschen Sie die Registrierung für das Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1b99f-118">Delete the registration for the event.</span></span><br/>            |
| <span id="WIA_SET_DEFAULT_HANDLER"></span><span id="wia_set_default_handler"></span><dl> <span data-ttu-id="1b99f-119"><dt>**WIA \_ - \_ Standard \_ Handler festlegen**</dt></span><span class="sxs-lookup"><span data-stu-id="1b99f-119"><dt>**WIA\_SET\_DEFAULT\_HANDLER**</dt></span></span> </dl>                   | <span data-ttu-id="1b99f-120">Legen Sie die Anwendung als Standard Ereignishandler fest.</span><span class="sxs-lookup"><span data-stu-id="1b99f-120">Set the application as the default event handler.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1b99f-121">*bstraude viceid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b99f-121">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b99f-122">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1b99f-122">Type: **BSTR**</span></span>

<span data-ttu-id="1b99f-123">Ein Geräte Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="1b99f-123">A device identifier.</span></span> <span data-ttu-id="1b99f-124">Übergeben Sie **null** , um für das Ereignis auf allen WIA 2,0-Geräten zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="1b99f-124">Pass **NULL** to register for the event on all WIA 2.0 devices.</span></span>

</dd> <dt>

<span data-ttu-id="1b99f-125">" *Peer-GUID* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="1b99f-125">*pEventGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b99f-126">Geben Sie Folgendes ein: \* Konstante *GUID \** _</span><span class="sxs-lookup"><span data-stu-id="1b99f-126">Type: \**const GUID\** _</span></span>

<span data-ttu-id="1b99f-127">Das Ereignis, für das die Anwendung registriert wird.</span><span class="sxs-lookup"><span data-stu-id="1b99f-127">The event that the application is registering for.</span></span> <span data-ttu-id="1b99f-128">Eine Liste gültiger Ereignis-GUIDs finden Sie unter [WIA-Ereignis](-wia-wia-event-identifiers.md)Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="1b99f-128">For a list of valid event GUIDs, see [WIA Event Identifiers](-wia-wia-event-identifiers.md).</span></span>

</dd> <dt>

<span data-ttu-id="1b99f-129">_bstrFullAppName \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b99f-129">_bstrFullAppName\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b99f-130">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1b99f-130">Type: **BSTR**</span></span>

<span data-ttu-id="1b99f-131">Der vollständige Pfadname der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="1b99f-131">The full path name of the application.</span></span>

</dd> <dt>

<span data-ttu-id="1b99f-132">*bstraucommandlinearg* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b99f-132">*bstrCommandlineArg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b99f-133">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1b99f-133">Type: **BSTR**</span></span>

<span data-ttu-id="1b99f-134">Die entsprechenden Befehlszeilenargumente für die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="1b99f-134">The appropriate command-line arguments for the application.</span></span>

</dd> <dt>

<span data-ttu-id="1b99f-135">*bstrinname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b99f-135">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b99f-136">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1b99f-136">Type: **BSTR**</span></span>

<span data-ttu-id="1b99f-137">Der Namen der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="1b99f-137">The name of the application.</span></span> <span data-ttu-id="1b99f-138">Der Name wird dem Benutzer angezeigt, wenn sich mehrere Anwendungen für dasselbe Ereignis registrieren.</span><span class="sxs-lookup"><span data-stu-id="1b99f-138">The name is displayed to the user when multiple applications register for the same event.</span></span>

</dd> <dt>

<span data-ttu-id="1b99f-139">*bstraudescription* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b99f-139">*bstrDescription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b99f-140">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1b99f-140">Type: **BSTR**</span></span>

<span data-ttu-id="1b99f-141">Die Beschreibung der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="1b99f-141">The description of the application.</span></span> <span data-ttu-id="1b99f-142">Die Beschreibung wird dem Benutzer angezeigt, wenn sich mehrere Anwendungen für dasselbe Ereignis registrieren.</span><span class="sxs-lookup"><span data-stu-id="1b99f-142">The description is displayed to the user when multiple applications register for the same event.</span></span>

</dd> <dt>

<span data-ttu-id="1b99f-143">*bstricon* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b99f-143">*bstrIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b99f-144">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1b99f-144">Type: **BSTR**</span></span>

<span data-ttu-id="1b99f-145">Das Symbol, das die Anwendung darstellt.</span><span class="sxs-lookup"><span data-stu-id="1b99f-145">The icon that represents the application.</span></span> <span data-ttu-id="1b99f-146">Das Symbol wird dem Benutzer angezeigt, wenn sich mehrere Anwendungen für dasselbe Ereignis registrieren.</span><span class="sxs-lookup"><span data-stu-id="1b99f-146">The icon is displayed to the user when multiple applications register for the same event.</span></span> <span data-ttu-id="1b99f-147">Die Zeichenfolge enthält den Namen der Anwendung und den NULL basierten Index des Symbols, getrennt durch ein Komma, z. b. "MyApp, 0".</span><span class="sxs-lookup"><span data-stu-id="1b99f-147">The string contains the name of the application and the zero-based index of the icon separated by a comma, for example, "MyApp, 0".</span></span> <span data-ttu-id="1b99f-148">Möglicherweise gibt es mehrere Symbole, die eine Anwendung darstellen.</span><span class="sxs-lookup"><span data-stu-id="1b99f-148">There might be more than one icon that represents an application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b99f-149">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b99f-149">Return value</span></span>

<span data-ttu-id="1b99f-150">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1b99f-150">Type: **HRESULT**</span></span>

<span data-ttu-id="1b99f-151">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="1b99f-151">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1b99f-152">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1b99f-152">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b99f-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b99f-153">Remarks</span></span>

<span data-ttu-id="1b99f-154">Verwenden Sie **IWiaDevMgr2:: registereventcallbackprogram** , um sich für Hardware Geräte Ereignisse zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="1b99f-154">Use **IWiaDevMgr2::RegisterEventCallbackProgram** to register for hardware device events.</span></span> <span data-ttu-id="1b99f-155">Wenn ein Ereignis auftritt, bei dem eine Anwendung für registriert ist, wird die Anwendung gestartet, und die Ereignis Informationen werden an die Anwendung übertragen.</span><span class="sxs-lookup"><span data-stu-id="1b99f-155">When an event occurs that an application is registered for, the application is launched, and the event information is transmitted to the application.</span></span>

<span data-ttu-id="1b99f-156">Verwenden Sie die [**enumregistereventinfo**](-wia-iwiaitem2-enumregistereventinfo.md) -Methode, um einen Zeiger auf ein Enumeratorobjekt für Ereignis Registrierungs Eigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1b99f-156">Use the [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) method to retrieve a pointer to an enumerator object for event registration properties.</span></span>

<span data-ttu-id="1b99f-157">Verwenden Sie die **IWiaDevMgr2:: registereventcallbackprogram** -Methode nur für die Abwärtskompatibilität mit Anwendungen, die nicht für die WIA 2,0-Architektur geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="1b99f-157">Only use the **IWiaDevMgr2::RegisterEventCallbackProgram** method for backward compatibility with applications not written for the WIA 2.0 architecture.</span></span> <span data-ttu-id="1b99f-158">Verwenden Sie die von der WIA 2,0-Architektur bereitgestellten Component Object Model (com)-Schnittstellen für neue Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="1b99f-158">Use the Component Object Model (COM) interfaces provided by the WIA 2.0 architecture for new applications.</span></span> <span data-ttu-id="1b99f-159">Rufen Sie insbesondere [**IWiaDevMgr2:: registereventcallbackinterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md) oder [**IWiaDevMgr2:: registereventcallbackclsid**](-wia-iwiadevmgr2-registereventcallbackclsid.md) auf, um eine neue Anwendung für Geräte Ereignisse zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="1b99f-159">Specifically, call [**IWiaDevMgr2::RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md) or [**IWiaDevMgr2::RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) to register a new application for device events.</span></span>

<span data-ttu-id="1b99f-160">In der Regel wird diese Methode von einem Installationsprogramm oder einem Skript aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1b99f-160">Typically, this method is called by an install program or a script.</span></span> <span data-ttu-id="1b99f-161">Das Installationsprogramm oder Skript registriert die Anwendung, um WIA 2,0-Geräte Ereignisse zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="1b99f-161">The install program or script registers the application to receive WIA 2.0 device events.</span></span> <span data-ttu-id="1b99f-162">Wenn das Ereignis auftritt, wird die Anwendung vom WIA 2,0-Laufzeitsystem gestartet.</span><span class="sxs-lookup"><span data-stu-id="1b99f-162">When the event occurs, the application is started by the WIA 2.0 run-time system.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b99f-163">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b99f-163">Requirements</span></span>



| <span data-ttu-id="1b99f-164">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b99f-164">Requirement</span></span> | <span data-ttu-id="1b99f-165">Wert</span><span class="sxs-lookup"><span data-stu-id="1b99f-165">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1b99f-166">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b99f-166">Minimum supported client</span></span><br/> | <span data-ttu-id="1b99f-167">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b99f-167">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1b99f-168">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b99f-168">Minimum supported server</span></span><br/> | <span data-ttu-id="1b99f-169">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b99f-169">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1b99f-170">Header</span><span class="sxs-lookup"><span data-stu-id="1b99f-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b99f-171"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b99f-171"><dt>Wia.h</dt></span></span> </dl> |



 

 




