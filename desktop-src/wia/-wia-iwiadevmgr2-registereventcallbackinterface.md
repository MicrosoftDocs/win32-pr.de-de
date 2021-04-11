---
description: Registriert eine laufende Anwendung für die Windows-Image Erfassung (WIA) 2,0-Ereignis Benachrichtigung.
ms.assetid: 978dcd41-d63b-421d-b7e1-8e9368b36180
title: 'IWiaDevMgr2:: registereventcallbackinterface-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackInterface
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 7cd3a7e00cff56bc5d91bfc843ab79fe71aa1123
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216049"
---
# <a name="iwiadevmgr2registereventcallbackinterface-method"></a><span data-ttu-id="f0d7d-103">IWiaDevMgr2:: registereventcallbackinterface-Methode</span><span class="sxs-lookup"><span data-stu-id="f0d7d-103">IWiaDevMgr2::RegisterEventCallbackInterface method</span></span>

<span data-ttu-id="f0d7d-104">Registriert eine laufende Anwendung für die Windows-Image Erfassung (WIA) 2,0-Ereignis Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-104">Registers a running application for Windows Image Acquisition (WIA) 2.0 event notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0d7d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0d7d-105">Syntax</span></span>


```C++
HRESULT RegisterEventCallbackInterface(
  [in]        LONG              lFlags,
  [in]        BSTR              bstrDeviceID,
  [in]  const GUID              *pEventGUID,
  [in]        IWiaEventCallback *pIWiaEventCallback,
  [out]       IUnknown          **pEventObject
);
```



## <a name="parameters"></a><span data-ttu-id="f0d7d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0d7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0d7d-107">*lFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0d7d-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0d7d-108">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="f0d7d-108">Type: **LONG**</span></span>

<span data-ttu-id="f0d7d-109">Derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-109">Currently unused.</span></span> <span data-ttu-id="f0d7d-110">Sollte auf Null festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="f0d7d-111">*bstraude viceid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0d7d-111">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0d7d-112">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f0d7d-112">Type: **BSTR**</span></span>

<span data-ttu-id="f0d7d-113">Gibt den eindeutigen Bezeichner eines WIA 2,0-Geräts an.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-113">Specifies the unique identifier of a WIA 2.0 device.</span></span> <span data-ttu-id="f0d7d-114">Legen Sie diesen Parameter auf **null** fest, um für das Ereignis auf allen WIA 2,0-Geräten zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-114">Set this parameter to **NULL** to register for the event on all WIA 2.0 devices.</span></span>

</dd> <dt>

<span data-ttu-id="f0d7d-115">" *Peer-GUID* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="f0d7d-115">*pEventGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0d7d-116">Geben Sie Folgendes ein: \* Konstante *GUID \** _</span><span class="sxs-lookup"><span data-stu-id="f0d7d-116">Type: \**const GUID\** _</span></span>

<span data-ttu-id="f0d7d-117">Gibt einen Zeiger auf den Ereignis Bezeichner an, für den die Anwendung registriert wird.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-117">Specifies a pointer to the event identifier that the application is registering for.</span></span> <span data-ttu-id="f0d7d-118">Weitere Informationen finden Sie unter [WIA-Ereignis](-wia-wia-event-identifiers.md) Bezeichner für Standard Ereignis Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-118">See [WIA Event Identifiers](-wia-wia-event-identifiers.md) for standard event identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="f0d7d-119">_pIWiaEventCallback \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0d7d-119">_pIWiaEventCallback\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0d7d-120">Typ: \**[**iwiaeventcallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) \** _</span><span class="sxs-lookup"><span data-stu-id="f0d7d-120">Type: \**[**IWiaEventCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback)\** _</span></span>

<span data-ttu-id="f0d7d-121">Gibt einen Zeiger auf die [_ *iwiaeventcallback* \*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) -Schnittstelle an, die von WIA 2,0 zum Senden der Ereignis Benachrichtigung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-121">Specifies a pointer to the [_ *IWiaEventCallback*\*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) interface that the WIA 2.0 uses to send event notification.</span></span>

</dd> <dt>

<span data-ttu-id="f0d7d-122">" *Peer-Object* \[ " vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f0d7d-122">*pEventObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0d7d-123">Typ: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span><span class="sxs-lookup"><span data-stu-id="f0d7d-123">Type: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span></span>

<span data-ttu-id="f0d7d-124">Empfängt die Adresse eines Zeigers auf die [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-124">Receives the address of a pointer to the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0d7d-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0d7d-125">Return value</span></span>

<span data-ttu-id="f0d7d-126">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f0d7d-126">Type: **HRESULT**</span></span>

<span data-ttu-id="f0d7d-127">Gibt die Standard-COM-Fehlercodes oder die folgenden zurück.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-127">Returns the standard COM error codes or the following.</span></span>



| <span data-ttu-id="f0d7d-128">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f0d7d-128">Return code</span></span>                                                                               | <span data-ttu-id="f0d7d-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f0d7d-129">Description</span></span>                                                            |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f0d7d-130"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="f0d7d-130"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="f0d7d-131">Die [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle kann nicht zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-131">The [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface cannot be returned.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="f0d7d-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f0d7d-132">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="f0d7d-133">Das Verwenden der [**iwiadevmgr:: registereventcallbackinterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface)-Methode, der **IWiaDevMgr2:: registereventcallbackinterface**-Methode und der [**DeviceManager. registerevent**](/previous-versions/windows/desktop/wiaaut/-wiaaut-idevicemanager-registerevent) -Methode aus demselben Prozess, nachdem der weiterhin Image Dienst neu gestartet wurde, kann zu einer Zugriffsverletzung führen, wenn die Funktionen vor dem Beenden des Dienstes verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-133">Using the [**IWiaDevMgr::RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface), **IWiaDevMgr2::RegisterEventCallbackInterface**, and [**DeviceManager.RegisterEvent**](/previous-versions/windows/desktop/wiaaut/-wiaaut-idevicemanager-registerevent) methods from the same process after the Still Image Service is restarted may cause an access violation, if the functions were used before the service was stopped.</span></span>

 

<span data-ttu-id="f0d7d-134">Wenn WIA 2,0-Anwendungen mit der Ausführung beginnen, wird diese Methode verwendet, um sich für den Empfang von Hardware Geräte Ereignissen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-134">When WIA 2.0 applications begin executing, they use this method to register to receive hardware device events.</span></span> <span data-ttu-id="f0d7d-135">Dadurch wird verhindert, dass die Anwendung neu gestartet wird, wenn ein anderes Ereignis registriert wird.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-135">This prevents the application from being restarted when another event for which it is registered occurs.</span></span> <span data-ttu-id="f0d7d-136">Sobald eine Anwendung **IWiaDevMgr2:: registereventcallbackinterface** aufruft, um sich für das Empfangen von WIA 2,0-Ereignissen von einem Gerät zu registrieren, werden die registrierten Ereignisse von WIA 2,0 an das Programm weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-136">Once an application calls **IWiaDevMgr2::RegisterEventCallbackInterface** to register itself to receive WIA 2.0 events from a device, the registered events are routed to the program by WIA 2.0.</span></span>

<span data-ttu-id="f0d7d-137">Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für die Schnittstellen Zeiger aufrufen, die Sie über den Parameter " *Peer-Object* " empfangen.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-137">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *pEventObject* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="f0d7d-138">In einer Multithreadanwendung kann der Ereignis Benachrichtigungs Rückruf in einem anderen Thread als dem auftreten, der den Rückruf registriert hat.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-138">In a multithreaded application, the event notification callback may come in on a different thread from the one that registered the callback.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f0d7d-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0d7d-139">Requirements</span></span>



| <span data-ttu-id="f0d7d-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0d7d-140">Requirement</span></span> | <span data-ttu-id="f0d7d-141">Wert</span><span class="sxs-lookup"><span data-stu-id="f0d7d-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f0d7d-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f0d7d-142">Minimum supported client</span></span><br/> | <span data-ttu-id="f0d7d-143">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0d7d-143">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f0d7d-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f0d7d-144">Minimum supported server</span></span><br/> | <span data-ttu-id="f0d7d-145">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0d7d-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f0d7d-146">Header</span><span class="sxs-lookup"><span data-stu-id="f0d7d-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0d7d-147"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0d7d-147"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="f0d7d-148">IDL</span><span class="sxs-lookup"><span data-stu-id="f0d7d-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f0d7d-149"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f0d7d-149"><dt>Wia.idl</dt></span></span> </dl> |



 

 
