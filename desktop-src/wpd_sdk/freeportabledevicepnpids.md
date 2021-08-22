---
description: Gibt die Plug & Play(PnP)-Bezeichner frei, die von den Methoden IPortableDeviceManager::GetDevices oder IPortableDeviceServiceManager::GetDeviceServices abgerufen werden.
ms.assetid: b86f7733-81a3-4b60-bb7c-840c75f8d03f
title: FreePortableDevicePnPIDs-Funktion (PortableDevice.h)
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
ms.openlocfilehash: 150796912d2796a2697d3c088963c20e1523288f5a1301e9467a6859845db68c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590314"
---
# <a name="freeportabledevicepnpids-function"></a>FreePortableDevicePnPIDs-Funktion

The **FreePortableDevicePnPIDs** helper function frees the Plug and Play (PnP) identifiers that are retrieved by the [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) or [**IPortableDeviceServiceManager::GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) methods.

## <a name="syntax"></a>Syntax


```C++
void FreePortableDevicePnPIDs(
   LPWSTR *pPnPIDs,
   DWORD  cPnPIDs
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pPnPIDs* 
</dt> <dd>

Das Array der Plug & Play (PnP), die frei werden sollen.

</dd> <dt>

*cPnPIDs* 
</dt> <dd>

Die Anzahl der Bezeichner im Array, die durch den *pPnPIDs-Parameter angegeben* werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die Anwendung ist dafür verantwortlich, das Array von Zeigern frei zu geben, die sie zuteilen.

## <a name="examples"></a>Beispiele


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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                   |
| Header<br/>                   | <dl> <dt>PortableDevice.h</dt> </dl> |



 

 




