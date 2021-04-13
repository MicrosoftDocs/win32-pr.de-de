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
# <a name="freeportabledevicepnpids-function"></a>Freportabledebug Item-Funktion

Die Hilfsfunktion " **freportabledevicepnpids** " gibt die Plug & Play (PNP)-IDs frei, die von der [**iportabledevicemanager:: GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) -Methode oder der [**iportabledeviceservicemanager:: getdeviceservices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) -Methode abgerufen werden.

## <a name="syntax"></a>Syntax


```C++
void FreePortableDevicePnPIDs(
   LPWSTR *pPnPIDs,
   DWORD  cPnPIDs
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppnpids* 
</dt> <dd>

Das Array von Plug & Play-Bezeichner (PNP), das freigegeben werden soll.

</dd> <dt>

*cpnpids* 
</dt> <dd>

Die Anzahl der Bezeichner im Array, das vom *ppnpids* -Parameter angegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Anwendung ist dafür verantwortlich, das Array von Zeigern freizugeben, das Sie zuweist.

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
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                   |
| Header<br/>                   | <dl> <dt>Portabledevice. h</dt> </dl> |



 

 




