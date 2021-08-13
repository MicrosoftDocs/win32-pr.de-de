---
description: Ruft das nächste oder mehrere IPortableDeviceConnector-Objekte in der Enumerationssequenz ab.
ms.assetid: 5aed563a-5ecc-49c0-8a0c-622405453896
title: IEnumPortableDeviceConnectors::Next-Methode (Devpkey.h)
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
ms.openlocfilehash: 868f13f220dbd5d5867e5ee2bbb54c1ef946e267d87e9ea0aa625108b945d537
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697295"
---
# <a name="ienumportabledeviceconnectorsnext-method"></a>IEnumPortableDeviceConnectors::Next-Methode

Die **Next-Methode** ruft das nächste oder mehrere [**IPortableDeviceConnector-Objekte**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) in der Enumerationssequenz ab.

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

*cRequested* \[ In\]
</dt> <dd>

Die Anzahl der angeforderten Geräte. Dieser Wert gibt auch die Anzahl der Elemente im vom Aufrufer zugewiesenen Array an, die durch den *pConnectors-Parameter* angegeben werden.

</dd> <dt>

*pConnectors* \[ out\]
</dt> <dd>

Ein Array von [**IPortableDeviceConnector-Zeigern,**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) die jeweils ein gekoppeltes MTP-Bluetooth Gerät angeben. Der Aufrufer muss ein Array von **IPortableDeviceConnector-Zeigern** mit der vom *cRequested-Parameter angegebenen* Arraylänge zuordnen. Bei erfolgreicher Rückgabe muss der Aufrufer sowohl das Array als auch die zurückgegebenen Zeiger freigeben. Die **IPortableDeviceConnector-Schnittstellen** werden durch Aufrufen der **IUnknown::Release-Methode** freigegeben.

</dd> <dt>

*pcFetched* \[ in, out\]
</dt> <dd>

Die Anzahl der [**IPortableDeviceConnector-Schnittstellen,**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) die tatsächlich abgerufen werden. Wenn keine **IPortableDeviceConnector-Schnittstellen** abgerufen werden und der Rückgabewert **S \_ FALSE** lautet, müssen keine **IPortableDeviceConnector-Schnittstellen** mehr aufzählen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                             | Beschreibung                                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | Die Methode wurde erfolgreich ausgeführt.<br/>                                 |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Es sind keine MTP-Bluetooth geräte mehr aufzuzählen.<br/> |



 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung dieser Methode veranschaulicht, um gekoppelte MTP-/Bluetooth-Geräte aufzuzählen und jeweils eine asynchrone Verbindungsanforderung zu senden.


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
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                                                                                             |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                                                                              |
| Header<br/>                   | <dl> <dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Portabledeviceconnectapi.idl</dt> </dl>                                                                |
| Bibliothek<br/>                  | <dl> <dt>PortableDeviceGuids.lib</dt> </dl>                                                                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




