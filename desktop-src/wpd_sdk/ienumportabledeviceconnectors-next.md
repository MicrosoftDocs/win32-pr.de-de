---
description: Ruft das nächste oder mehrere iportabledeviceconnector-Objekte in der enumerationssequenz ab.
ms.assetid: 5aed563a-5ecc-49c0-8a0c-622405453896
title: 'Ienumportabledeviceconnectors:: Next-Methode (devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Next
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 709e938c28f9bf09e34d918eea7be3029c7a11e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352708"
---
# <a name="ienumportabledeviceconnectorsnext-method"></a><span data-ttu-id="fd6a4-103">Ienumportabledeviceconnectors:: Next-Methode</span><span class="sxs-lookup"><span data-stu-id="fd6a4-103">IEnumPortableDeviceConnectors::Next method</span></span>

<span data-ttu-id="fd6a4-104">Die **Next** -Methode ruft das nächste oder mehrere [**iportabledeviceconnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) -Objekte in der enumerationssequenz ab.</span><span class="sxs-lookup"><span data-stu-id="fd6a4-104">The **Next** method retrieves the next one or more [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) objects in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd6a4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd6a4-105">Syntax</span></span>


```C++
HRESULT Next(
  [in]      UINT32                   cRequested,
  [out]     IPortableDeviceConnector **pConnectors,
  [in, out] UINT32                   *pcFetched
);
```



## <a name="parameters"></a><span data-ttu-id="fd6a4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd6a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd6a4-107">durch *forwalte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd6a4-107">*cRequested* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6a4-108">Die Anzahl der angeforderten Geräte.</span><span class="sxs-lookup"><span data-stu-id="fd6a4-108">The number of requested devices.</span></span> <span data-ttu-id="fd6a4-109">Dieser Wert gibt auch die Anzahl der Elemente im vom Aufrufer zugeordneten Array an, das durch den *pconnectors* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fd6a4-109">This value also indicates the number of elements in the caller-allocated array specified by the *pConnectors* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="fd6a4-110">*pconnectors* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fd6a4-110">*pConnectors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6a4-111">Ein Array von [**iportablede viceconnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) -Zeigern, das jeweils ein gekoppeltes MTP-Bluetooth-Gerät angibt.</span><span class="sxs-lookup"><span data-stu-id="fd6a4-111">An array of [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) pointers, each specifying a paired MTP Bluetooth device.</span></span> <span data-ttu-id="fd6a4-112">Der Aufrufer muss ein Array von **iportablede viceconnector** -Zeigern zuordnen, wobei die Array Länge durch den *erstellten Parameter angegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="fd6a4-112">The caller must allocate an array of **IPortableDeviceConnector** pointers, with the array length specified by the *cRequested* parameter.</span></span> <span data-ttu-id="fd6a4-113">Bei erfolgreicher Rückgabe muss der Aufrufer sowohl das Array als auch den zurückgegebenen Zeiger freigeben.</span><span class="sxs-lookup"><span data-stu-id="fd6a4-113">On successful return, the caller must free both the array and the returned pointers.</span></span> <span data-ttu-id="fd6a4-114">Die **iportabledeviceconnector** -Schnittstellen werden durch Aufrufen der **IUnknown:: Release** -Methode freigegeben.</span><span class="sxs-lookup"><span data-stu-id="fd6a4-114">The **IPortableDeviceConnector** interfaces are freed by calling the **IUnknown::Release** method.</span></span>

</dd> <dt>

<span data-ttu-id="fd6a4-115">*pcfetch* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fd6a4-115">*pcFetched* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6a4-116">Die Anzahl von [**iportabledeviceconnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) -Schnittstellen, die tatsächlich abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="fd6a4-116">The number of [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) interfaces that are actually retrieved.</span></span> <span data-ttu-id="fd6a4-117">Wenn keine **iportabledeviceconnector** -Schnittstellen abgerufen werden und der Rückgabewert **S \_ false** ist, sind keine weiteren **iportabledeviceconnector** -Schnittstellen für die Enumeration vorhanden.</span><span class="sxs-lookup"><span data-stu-id="fd6a4-117">If no **IPortableDeviceConnector** interfaces are retrieved and the return value is **S\_FALSE**, there are no more **IPortableDeviceConnector** interfaces to enumerate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd6a4-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fd6a4-118">Return value</span></span>

<span data-ttu-id="fd6a4-119">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="fd6a4-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="fd6a4-120">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="fd6a4-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="fd6a4-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="fd6a4-121">Return code</span></span>                                                                             | <span data-ttu-id="fd6a4-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fd6a4-122">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="fd6a4-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fd6a4-123"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="fd6a4-124">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fd6a4-124">The method succeeded.</span></span><br/>                                 |
| <dl> <span data-ttu-id="fd6a4-125"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="fd6a4-125"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="fd6a4-126">Es sind keine weiteren MTP-Bluetooth-Geräte zur Enumeration vorhanden.</span><span class="sxs-lookup"><span data-stu-id="fd6a4-126">There are no more MTP Bluetooth devices to enumerate.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="fd6a4-127">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd6a4-127">Examples</span></span>

<span data-ttu-id="fd6a4-128">Im folgenden Beispiel wird veranschaulicht, wie diese Methode verwendet wird, um gekoppelte MTP/Bluetooth-Geräte aufzuzählen und eine asynchrone Verbindungsanforderung an jede zu senden.</span><span class="sxs-lookup"><span data-stu-id="fd6a4-128">The following example demonstrates the use of this method to enumerate paired MTP/Bluetooth devices, and to send an asynchronous connection request to each.</span></span>


```C++
IEnumPortableDeviceConnectors* pEnum = NULL;
    HRESULT hrEnum = S_OK;
 HRESULT hr = CoCreateInstance(CLSID_EnumBthMtpConnectors, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pEnum));
    if (SUCCEEDED(hr))
{
  while (S_OK == hrEnum)
    {
       UINT32  uFetched        = 0;
       LPWSTR  wszDevicePnPID  = NULL;
       IPortableDeviceConnector* pDevice = NULL;
       hrEnum = pEnum->Next(1, &spDevice, &uFetched);
       if (hrEnum == S_OK && uFetched == 1)
        {
          // Send an asynchronous connect request.  
          hr = pDevice ->Connect(NULL);
          // Release the device when done
          pDevice->Release();
          pDevice = NULL;
        }
     }  // while S_OK == hrEnum
  // Release the enumerator when done
    if (pEnum)
    {
     pEnum->Release();
     pEnum = NULL;
   }
    }
       
```



## <a name="requirements"></a><span data-ttu-id="fd6a4-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd6a4-129">Requirements</span></span>



| <span data-ttu-id="fd6a4-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd6a4-130">Requirement</span></span> | <span data-ttu-id="fd6a4-131">Wert</span><span class="sxs-lookup"><span data-stu-id="fd6a4-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd6a4-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd6a4-132">Minimum supported client</span></span><br/> | <span data-ttu-id="fd6a4-133">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd6a4-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="fd6a4-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd6a4-134">Minimum supported server</span></span><br/> | <span data-ttu-id="fd6a4-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fd6a4-135">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="fd6a4-136">Header</span><span class="sxs-lookup"><span data-stu-id="fd6a4-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd6a4-137"><dt>Devpkey. h; </dt> <dt>Portablede viceconnectapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd6a4-137"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="fd6a4-138">IDL</span><span class="sxs-lookup"><span data-stu-id="fd6a4-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fd6a4-139"><dt>Portablede viceconnectapi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fd6a4-139"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="fd6a4-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fd6a4-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="fd6a4-141"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd6a4-141"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="fd6a4-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd6a4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd6a4-143">**Ienumportablede viceconnectors**</span><span class="sxs-lookup"><span data-stu-id="fd6a4-143">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




