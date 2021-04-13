---
description: 'Mit der IWiaDevMgr2:: registereventcallbackclsid-Methode wird eine Anwendung zum Empfangen von Ereignissen registriert, auch wenn die Anwendung nicht ausgeführt wird.'
ms.assetid: e0d421a7-ef49-4e27-9661-c358ac819712
title: 'IWiaDevMgr2:: registereventcallbackclsid-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackCLSID
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 63e69d12d47f90ba40f5cc785d8b864c40158774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527074"
---
# <a name="iwiadevmgr2registereventcallbackclsid-method"></a><span data-ttu-id="216a4-103">IWiaDevMgr2:: registereventcallbackclsid-Methode</span><span class="sxs-lookup"><span data-stu-id="216a4-103">IWiaDevMgr2::RegisterEventCallbackCLSID method</span></span>

<span data-ttu-id="216a4-104">Mit der **IWiaDevMgr2:: registereventcallbackclsid** -Methode wird eine Anwendung zum Empfangen von Ereignissen registriert, auch wenn die Anwendung nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="216a4-104">The **IWiaDevMgr2::RegisterEventCallbackCLSID** method registers an application to receive events even if the application is not running.</span></span>

## <a name="syntax"></a><span data-ttu-id="216a4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="216a4-105">Syntax</span></span>


```C++
HRESULT RegisterEventCallbackCLSID(
  [in]               LONG lFlags,
  [in]               BSTR bstrDeviceID,
  [in]         const GUID *pEventGUID,
  [in, unique] const GUID *pClsID,
  [in]               BSTR bstrName,
  [in]               BSTR bstrDescription,
  [in]               BSTR bstrIcon
);
```



## <a name="parameters"></a><span data-ttu-id="216a4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="216a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="216a4-107">*lFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="216a4-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="216a4-108">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="216a4-108">Type: **LONG**</span></span>

<span data-ttu-id="216a4-109">Gibt Registrierungsflags an.</span><span class="sxs-lookup"><span data-stu-id="216a4-109">Specifies registration flags.</span></span> <span data-ttu-id="216a4-110">Kann auf die folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="216a4-110">Can be set to the following values:</span></span>



| <span data-ttu-id="216a4-111">Registrierungsflag</span><span class="sxs-lookup"><span data-stu-id="216a4-111">Registration Flag</span></span>                | <span data-ttu-id="216a4-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="216a4-112">Meaning</span></span>                                           |
|----------------------------------|---------------------------------------------------|
| <span data-ttu-id="216a4-113">WIA- \_ Register \_ Ereignis \_ Rückruf</span><span class="sxs-lookup"><span data-stu-id="216a4-113">WIA\_REGISTER\_EVENT\_CALLBACK</span></span>   | <span data-ttu-id="216a4-114">Registrieren Sie sich für das-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="216a4-114">Register for the event.</span></span>                           |
| <span data-ttu-id="216a4-115">\_ \_ Ereignis Rückruf für die Aufhebung der Registrierung \_</span><span class="sxs-lookup"><span data-stu-id="216a4-115">WIA\_UNREGISTER\_EVENT\_CALLBACK</span></span> | <span data-ttu-id="216a4-116">Löschen Sie die Registrierung für das Ereignis.</span><span class="sxs-lookup"><span data-stu-id="216a4-116">Delete the registration for the event.</span></span>            |
| <span data-ttu-id="216a4-117">WIA \_ - \_ Standard \_ Handler festlegen</span><span class="sxs-lookup"><span data-stu-id="216a4-117">WIA\_SET\_DEFAULT\_HANDLER</span></span>       | <span data-ttu-id="216a4-118">Legen Sie die Anwendung als Standard Ereignishandler fest.</span><span class="sxs-lookup"><span data-stu-id="216a4-118">Set the application as the default event handler.</span></span> |



 

</dd> <dt>

<span data-ttu-id="216a4-119">*bstraude viceid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="216a4-119">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="216a4-120">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="216a4-120">Type: **BSTR**</span></span>

<span data-ttu-id="216a4-121">Gibt einen Geräte Bezeichner an.</span><span class="sxs-lookup"><span data-stu-id="216a4-121">Specifies a device identifier.</span></span> <span data-ttu-id="216a4-122">Übergeben Sie **null** , um für das Ereignis auf allen WIA 2,0-Geräten zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="216a4-122">Pass **NULL** to register for the event on all WIA 2.0 devices.</span></span>

</dd> <dt>

<span data-ttu-id="216a4-123">" *Peer-GUID* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="216a4-123">*pEventGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="216a4-124">Geben Sie Folgendes ein: \* Konstante *GUID \** _</span><span class="sxs-lookup"><span data-stu-id="216a4-124">Type: \**const GUID\** _</span></span>

<span data-ttu-id="216a4-125">Gibt das Ereignis an, für das die Anwendung registriert wird.</span><span class="sxs-lookup"><span data-stu-id="216a4-125">Specifies the event that the application is registering for.</span></span> <span data-ttu-id="216a4-126">Eine Liste der Standard Ereignisse finden Sie unter [WIA-Ereignis](-wia-wia-event-identifiers.md)Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="216a4-126">For a list of standard events, see [WIA Event Identifiers](-wia-wia-event-identifiers.md).</span></span>

</dd> <dt>

<span data-ttu-id="216a4-127">_pClsID \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="216a4-127">_pClsID\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="216a4-128">Geben Sie Folgendes ein: \* Konstante *GUID \** _</span><span class="sxs-lookup"><span data-stu-id="216a4-128">Type: \**const GUID\** _</span></span>

<span data-ttu-id="216a4-129">Zeiger auf die Anwendungs Klassen-ID (_ \* CLSID \* \*).</span><span class="sxs-lookup"><span data-stu-id="216a4-129">Pointer to the application class ID (_\*CLSID\*\*).</span></span> <span data-ttu-id="216a4-130">Das WIA 2,0-Laufzeitsystem verwendet die Anwendungs- **CLSID** , um die Anwendung zu starten, wenn ein Ereignis auftritt, das für registriert ist.</span><span class="sxs-lookup"><span data-stu-id="216a4-130">The WIA 2.0 run-time system uses the application **CLSID** to start the application when an event occurs that it is registered for.</span></span>

</dd> <dt>

<span data-ttu-id="216a4-131">*bstrinname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="216a4-131">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="216a4-132">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="216a4-132">Type: **BSTR**</span></span>

<span data-ttu-id="216a4-133">Gibt den Namen der Anwendung an, die für das Ereignis registriert wird.</span><span class="sxs-lookup"><span data-stu-id="216a4-133">Specifies the name of the application that registers for the event.</span></span>

</dd> <dt>

<span data-ttu-id="216a4-134">*bstraudescription* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="216a4-134">*bstrDescription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="216a4-135">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="216a4-135">Type: **BSTR**</span></span>

<span data-ttu-id="216a4-136">Gibt eine Textbeschreibung der Anwendung an, die für das Ereignis registriert wird.</span><span class="sxs-lookup"><span data-stu-id="216a4-136">Specifies a text description of the application that registers for the event.</span></span>

</dd> <dt>

<span data-ttu-id="216a4-137">*bstricon* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="216a4-137">*bstrIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="216a4-138">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="216a4-138">Type: **BSTR**</span></span>

<span data-ttu-id="216a4-139">Gibt den Namen einer Bilddatei an, die für das Symbol für die Anwendung verwendet werden soll, die für das Ereignis registriert wird.</span><span class="sxs-lookup"><span data-stu-id="216a4-139">Specifies the name of an image file to use for the icon for the application that registers for the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="216a4-140">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="216a4-140">Return value</span></span>

<span data-ttu-id="216a4-141">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="216a4-141">Type: **HRESULT**</span></span>

<span data-ttu-id="216a4-142">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="216a4-142">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="216a4-143">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="216a4-143">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="216a4-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="216a4-144">Remarks</span></span>

<span data-ttu-id="216a4-145">WIA 2,0-Anwendungen verwenden diese Methode, um sich für den Empfang von Hardware Geräte Ereignissen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="216a4-145">WIA 2.0 applications use this method to register to receive hardware device events.</span></span> <span data-ttu-id="216a4-146">Nachdem **IWiaDevMgr2:: registereventcallbackclsid** aufgerufen wurde, wird die Anwendung für den Empfang von WIA 2,0-Geräte Ereignissen registriert, auch wenn Sie nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="216a4-146">After **IWiaDevMgr2::RegisterEventCallbackCLSID** is called, the application is registered to receive WIA 2.0 device events even if it is not running.</span></span>

<span data-ttu-id="216a4-147">Wenn das Ereignis auftritt, bestimmt das WIA 2,0-System, welche Anwendung registriert ist, um das Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="216a4-147">When the event occurs, the WIA 2.0 system determines which application is registered to receive the event.</span></span> <span data-ttu-id="216a4-148">Er verwendet die [cokreateinstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion und die im *pclsid* -Parameter angegebene CLSID, um eine Instanz der Anwendung zu erstellen, und ruft dann die [**imageeventcallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) -Methode auf, um die Ereignis Informationen an die Anwendung zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="216a4-148">It uses the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function and the CLSID specified in the *pClsID* parameter to create an instance of the application, and then calls the [**ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) method to transmit the event information to the application.</span></span>

<span data-ttu-id="216a4-149">Eine Anwendung kann die [**enumregistereventinfo**](-wia-iwiaitem2-enumregistereventinfo.md) -Methode aufrufen, um Ereignis Registrierungsinformationen aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="216a4-149">An application can invoke the [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) method to enumerate event registration information.</span></span>

<span data-ttu-id="216a4-150">Wenn die Anwendung keine registrierte Component Object Model (com)-Komponente ist und nicht mit der WIA 2,0-Architektur kompatibel ist, verwenden Sie die [**IWiaDevMgr2:: registereventcallbackprogram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) -Methode, um eine Anwendung für Geräte Ereignisse zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="216a4-150">If the application is not a registered Component Object Model (COM) component and is not compatible with the WIA 2.0 architecture, use the [**IWiaDevMgr2::RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) method to register an application for device events.</span></span>

> [!Note]  
> <span data-ttu-id="216a4-151">In einer Multithreadanwendung gibt es keine Garantie dafür, dass der Rückruf der Ereignis Benachrichtigung für denselben Thread zurückgegeben wird, der den Rückruf registriert hat.</span><span class="sxs-lookup"><span data-stu-id="216a4-151">In a multi-threaded application, there is no guarantee that the event notification callback is returned on the same thread that registered the callback.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="216a4-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="216a4-152">Requirements</span></span>



| <span data-ttu-id="216a4-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="216a4-153">Requirement</span></span> | <span data-ttu-id="216a4-154">Wert</span><span class="sxs-lookup"><span data-stu-id="216a4-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="216a4-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="216a4-155">Minimum supported client</span></span><br/> | <span data-ttu-id="216a4-156">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="216a4-156">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="216a4-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="216a4-157">Minimum supported server</span></span><br/> | <span data-ttu-id="216a4-158">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="216a4-158">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="216a4-159">Header</span><span class="sxs-lookup"><span data-stu-id="216a4-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="216a4-160"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="216a4-160"><dt>Wia.h</dt></span></span> </dl> |



 

 
