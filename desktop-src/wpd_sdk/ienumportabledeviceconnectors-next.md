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
# <a name="ienumportabledeviceconnectorsnext-method"></a>Ienumportabledeviceconnectors:: Next-Methode

Die **Next** -Methode ruft das nächste oder mehrere [**iportabledeviceconnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) -Objekte in der enumerationssequenz ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT Next(
  [in]      UINT32                   cRequested,
  [out]     IPortableDeviceConnector **pConnectors,
  [in, out] UINT32                   *pcFetched
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

durch *forwalte* \[ in\]
</dt> <dd>

Die Anzahl der angeforderten Geräte. Dieser Wert gibt auch die Anzahl der Elemente im vom Aufrufer zugeordneten Array an, das durch den *pconnectors* -Parameter angegeben wird.

</dd> <dt>

*pconnectors* \[ vorgenommen\]
</dt> <dd>

Ein Array von [**iportablede viceconnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) -Zeigern, das jeweils ein gekoppeltes MTP-Bluetooth-Gerät angibt. Der Aufrufer muss ein Array von **iportablede viceconnector** -Zeigern zuordnen, wobei die Array Länge durch den *erstellten Parameter angegeben* wird. Bei erfolgreicher Rückgabe muss der Aufrufer sowohl das Array als auch den zurückgegebenen Zeiger freigeben. Die **iportabledeviceconnector** -Schnittstellen werden durch Aufrufen der **IUnknown:: Release** -Methode freigegeben.

</dd> <dt>

*pcfetch* \[ in, out\]
</dt> <dd>

Die Anzahl von [**iportabledeviceconnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) -Schnittstellen, die tatsächlich abgerufen werden. Wenn keine **iportabledeviceconnector** -Schnittstellen abgerufen werden und der Rückgabewert **S \_ false** ist, sind keine weiteren **iportabledeviceconnector** -Schnittstellen für die Enumeration vorhanden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                             | Beschreibung                                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | Die Methode wurde erfolgreich ausgeführt.<br/>                                 |
| <dl> <dt>**S \_ false**</dt> </dl> | Es sind keine weiteren MTP-Bluetooth-Geräte zur Enumeration vorhanden.<br/> |



 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird veranschaulicht, wie diese Methode verwendet wird, um gekoppelte MTP/Bluetooth-Geräte aufzuzählen und eine asynchrone Verbindungsanforderung an jede zu senden.


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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                                                                                             |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                                                                              |
| Header<br/>                   | <dl> <dt>Devpkey. h; </dt> <dt>Portablede viceconnectapi. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Portablede viceconnectapi. idl</dt> </dl>                                                                |
| Bibliothek<br/>                  | <dl> <dt>Portabledeviceguids. lib</dt> </dl>                                                                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ienumportablede viceconnectors**](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




