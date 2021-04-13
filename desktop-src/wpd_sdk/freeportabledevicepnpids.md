---
description: 'Gibt die Plug & Play (PNP)-IDs frei, die von den Methoden iportabledevicemanager:: GetDevices oder iportabledeviceservicemanager:: getdeviceservices abgerufen werden.'
ms.assetid: b86f7733-81a3-4b60-bb7c-840c75f8d03f
title: Freportabledebug-Funktion (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreePortableDevicePnPIDs
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 58bb5fa33007ed0e167226edf7078d08c2e5c3de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217199"
---
# <a name="freeportabledevicepnpids-function"></a><span data-ttu-id="73e77-103">Freportabledebug Item-Funktion</span><span class="sxs-lookup"><span data-stu-id="73e77-103">FreePortableDevicePnPIDs function</span></span>

<span data-ttu-id="73e77-104">Die Hilfsfunktion " **freportabledevicepnpids** " gibt die Plug & Play (PNP)-IDs frei, die von der [**iportabledevicemanager:: GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) -Methode oder der [**iportabledeviceservicemanager:: getdeviceservices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) -Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="73e77-104">The **FreePortableDevicePnPIDs** helper function frees the Plug and Play (PnP) identifiers that are retrieved by the [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) or [**IPortableDeviceServiceManager::GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="73e77-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="73e77-105">Syntax</span></span>


```C++
void FreePortableDevicePnPIDs(
   LPWSTR *pPnPIDs,
   DWORD  cPnPIDs
);
```



## <a name="parameters"></a><span data-ttu-id="73e77-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="73e77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73e77-107">*ppnpids*</span><span class="sxs-lookup"><span data-stu-id="73e77-107">*pPnPIDs*</span></span> 
</dt> <dd>

<span data-ttu-id="73e77-108">Das Array von Plug & Play-Bezeichner (PNP), das freigegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="73e77-108">The array of Plug and Play (PnP) identifiers to be freed.</span></span>

</dd> <dt>

<span data-ttu-id="73e77-109">*cpnpids*</span><span class="sxs-lookup"><span data-stu-id="73e77-109">*cPnPIDs*</span></span> 
</dt> <dd>

<span data-ttu-id="73e77-110">Die Anzahl der Bezeichner im Array, das vom *ppnpids* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="73e77-110">The number of identifiers in the array specified by the *pPnPIDs* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73e77-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="73e77-111">Return value</span></span>

<span data-ttu-id="73e77-112">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="73e77-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="73e77-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73e77-113">Remarks</span></span>

<span data-ttu-id="73e77-114">Die Anwendung ist dafür verantwortlich, das Array von Zeigern freizugeben, das Sie zuweist.</span><span class="sxs-lookup"><span data-stu-id="73e77-114">The application is responsible for freeing the array of pointers that it allocates.</span></span>

## <a name="examples"></a><span data-ttu-id="73e77-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="73e77-115">Examples</span></span>


```C++
// Allocate an array of LPWSTR pointers.
    LPWSTR* pPnpDeviceIDs = new LPWSTR[cPnpDeviceIDs];
if (pPnpDeviceIDs != NULL)
{
    hr = pPortableDeviceManager->;GetDevices(pPnpDeviceIDs, &cPnpDeviceIDs);
    if (SUCCEEDED(hr))
    {
        // Free all returned PnPDeviceID strings allocated by IPortableDeviceManager::GetDevices.
     FreePortableDevicePnPIDs(pPnpDeviceIDs, cPnpDeviceIDs);
     // Application is responsible for deleting the array of LPWSTR pointers.
     delete [] pPnpDeviceIDs;
     pPnpDeviceIDs = NULL;      
 }
} 
```



## <a name="requirements"></a><span data-ttu-id="73e77-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73e77-116">Requirements</span></span>



| <span data-ttu-id="73e77-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73e77-117">Requirement</span></span> | <span data-ttu-id="73e77-118">Wert</span><span class="sxs-lookup"><span data-stu-id="73e77-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="73e77-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="73e77-119">Minimum supported client</span></span><br/> | <span data-ttu-id="73e77-120">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="73e77-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                           |
| <span data-ttu-id="73e77-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="73e77-121">Minimum supported server</span></span><br/> | <span data-ttu-id="73e77-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="73e77-122">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="73e77-123">Header</span><span class="sxs-lookup"><span data-stu-id="73e77-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="73e77-124"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="73e77-124"><dt>PortableDevice.h</dt></span></span> </dl> |



 

 




