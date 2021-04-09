---
description: Benachrichtigt eine Anwendung, dass eine zuvor geplante Connect-oder Disconnect-Anforderung an das MTP/Bluetooth-Gerät abgeschlossen wurde.
ms.assetid: 1588d0ec-0d6a-4379-bfdc-4ba5fdaa4665
title: 'Iconnectionrequestcallback:: OnComplete-Methode (devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IConnectionRequestCallback.OnComplete
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 922169b7e17335c47425665bb9a9e54891e68723
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866523"
---
# <a name="iconnectionrequestcallbackoncomplete-method"></a><span data-ttu-id="56fa6-103">Iconnectionrequestcallback:: OnComplete-Methode</span><span class="sxs-lookup"><span data-stu-id="56fa6-103">IConnectionRequestCallback::OnComplete method</span></span>

<span data-ttu-id="56fa6-104">Mit der **OnComplete** -Methode wird eine Anwendung benachrichtigt, dass eine zuvor geplante Connect-oder Disconnect-Anforderung an das MTP/Bluetooth-Gerät abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="56fa6-104">The **OnComplete** method notifies an application that a previously scheduled Connect or Disconnect request to the MTP/Bluetooth device has completed</span></span>

## <a name="syntax"></a><span data-ttu-id="56fa6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="56fa6-105">Syntax</span></span>


```C++
HRESULT OnComplete(
  [in] HRESULT hrStatus
);
```



## <a name="parameters"></a><span data-ttu-id="56fa6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="56fa6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56fa6-107">*hrStatus* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="56fa6-107">*hrStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56fa6-108">Der Status der Anforderung zum Verbinden oder Trennen eines bestimmten Geräts.</span><span class="sxs-lookup"><span data-stu-id="56fa6-108">The status of the request to connect or disconnect a given device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56fa6-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56fa6-109">Return value</span></span>

<span data-ttu-id="56fa6-110">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="56fa6-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="56fa6-111">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="56fa6-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="56fa6-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="56fa6-112">Return code</span></span>                                                                          | <span data-ttu-id="56fa6-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56fa6-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="56fa6-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="56fa6-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="56fa6-115">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="56fa6-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="56fa6-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56fa6-116">Remarks</span></span>

<span data-ttu-id="56fa6-117">Eine Anwendung implementiert die [**iconnectionrequestcallback**](iconnectionrequestcallback.md) -Schnittstelle zum Empfangen von Benachrichtigungen zu abgeschlossenen Anforderungen und zum Abbrechen ausstehender Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="56fa6-117">An application implements the [**IConnectionRequestCallback**](iconnectionrequestcallback.md) interface to receive notifications about completed requests and to cancel pending requests.</span></span>

<span data-ttu-id="56fa6-118">Windows Portable Devices (WPD) ruft diese Methode auf, um eine Anwendung zu benachrichtigen, dass eine zuvor geplante Anforderung abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="56fa6-118">Windows Portable Devices (WPD) calls this method to notify an application that a previously scheduled request has completed.</span></span> <span data-ttu-id="56fa6-119">Jede Anforderung kann durch den von der Anwendung bereitgestellten Rückruf nachverfolgt und abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="56fa6-119">Each request can be tracked and canceled by its application-supplied callback.</span></span> <span data-ttu-id="56fa6-120">Wenn die Anwendung also mehrere Anforderungen gleichzeitig mit demselben [**iportabledeviceconnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) -Objekt senden muss, sollte jeder Anforderung ein eindeutiges [**iconnectionrequestcallback**](iconnectionrequestcallback.md) -Objekt als Eingabeparameter an die [**iportabledeviceconnector:: Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) -und [**iportabledeviceconnector::D isconnect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) -Methoden übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="56fa6-120">Therefore, if the application needs to send multiple requests at the same time using the same [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) object, each request should be passed a unique [**IConnectionRequestCallback**](iconnectionrequestcallback.md) object as the input parameter to the [**IPortableDeviceConnector::Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) and [**IPortableDeviceConnector::Disconnect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="56fa6-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56fa6-121">Requirements</span></span>



| <span data-ttu-id="56fa6-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56fa6-122">Requirement</span></span> | <span data-ttu-id="56fa6-123">Wert</span><span class="sxs-lookup"><span data-stu-id="56fa6-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56fa6-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="56fa6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="56fa6-125">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="56fa6-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="56fa6-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="56fa6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="56fa6-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="56fa6-127">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="56fa6-128">Header</span><span class="sxs-lookup"><span data-stu-id="56fa6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="56fa6-129"><dt>Devpkey. h; </dt> <dt>Portablede viceconnectapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="56fa6-129"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="56fa6-130">IDL</span><span class="sxs-lookup"><span data-stu-id="56fa6-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="56fa6-131"><dt>Portablede viceconnectapi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="56fa6-131"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="56fa6-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="56fa6-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="56fa6-133"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="56fa6-133"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="56fa6-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56fa6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56fa6-135">**Iconnectionrequestcallback**</span><span class="sxs-lookup"><span data-stu-id="56fa6-135">**IConnectionRequestCallback**</span></span>](iconnectionrequestcallback.md)
</dt> </dl>

 

 




