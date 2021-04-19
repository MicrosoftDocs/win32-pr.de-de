---
title: Iwmdrmdeviceapp generatemeterchallenge-Methode (wmdrmdeviceapp. h)
description: Mit der generatemeterchallenge-Methode werden Messungs Daten von einem Gerät angefordert.
ms.assetid: 2457cab7-bd45-49a7-ba69-74ae022207ce
keywords:
- Generatemeterchallenge-Methode, Windows Media Device Manager
- Generatemeterchallenge-Methode Windows Media Device Manager, iwmdrmdeviceapp-Schnittstelle
- Iwmdrmdeviceapp-Schnittstelle Windows Media Device Manager, generatemeterchallenge-Methode
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.GenerateMeterChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06a71f04a5837f09575a2f4bccf4b17e34e30d63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354161"
---
# <a name="iwmdrmdeviceappgeneratemeterchallenge-method"></a>Iwmdrmdeviceapp:: generatemeterchallenge-Methode

Mit der **generatemeterchallenge** -Methode werden Messungs Daten von einem Gerät angefordert.

## <a name="syntax"></a>Syntax


```C++
HRESULT GenerateMeterChallenge(
  [in]  IWMDMDevice *pDevice,
  [in]  BSTR        bstrMeterCert,
  [out] BSTR        *pbstrMeterURL,
  [out] BSTR        *pbstrMeterData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdevice* \[ in\]
</dt> <dd>

Zeiger auf eine [**iwmdmdevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) -Schnittstelle. Wenn die Anwendung in **null** übergeht, werden Messungs Informationen, die auf dem Computer gespeichert sind, anstelle von Messungs Informationen eines verbundenen Geräts verwendet.

</dd> <dt>

*bstrinmetercert* \[ in\]
</dt> <dd>

Das Messungs Zertifikat der Anwendung als **BSTR**. Dies ist ein von Microsoft empfangenes signiertes Zertifikat.

</dd> <dt>

*pbstrinmeterurl* \[ vorgenommen\]
</dt> <dd>

Die URL, an die Messungs Daten gesendet werden sollen. Diese wird von Windows Media Device Manager zugeordnet und muss vom Aufrufer mit **SysFreeString** freigegeben werden.

</dd> <dt>

*pbstrinmeterdaten* \[ vorgenommen\]
</dt> <dd>

Messungs Daten, die an den Messungs Dienst gesendet werden sollen. Diese wird von Windows Media Device Manager zugeordnet und muss vom Aufrufer mit **SysFreeString** freigegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                      | Beschreibung                                                                   |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                             | Die Methode wurde erfolgreich ausgeführt.<br/>                                              |
| <dl> <dt>**DRM \_ E \_ invalidArg**</dt> </dl>                | Mindestens ein Argument ist ungültig.<br/>                               |
| <dl> <dt>**DRM \_ E \_ invalidxmltag**</dt> </dl>             | XML ist nicht ordnungsgemäß formatiert.<br/>                                          |
| <dl> <dt>**DRM \_ E \_ noxmlclosetag**</dt> </dl>             | XML ist nicht ordnungsgemäß formatiert.<br/>                                          |
| <dl> <dt>**DRM \_ E \_ noxmlopentag**</dt> </dl>              | XML ist nicht ordnungsgemäß formatiert.<br/>                                          |
| <dl> <dt>**DRM \_ E \_ xmlnotfound**</dt> </dl>               | Fehler beim Suchen eines erforderlichen XML-Tags.<br/>                                 |
| <dl> <dt>**Fehler des Geräts**</dt> </dl>            | Eine beliebige Anzahl von Gerätefehlern.<br/>                                  |
| <dl> <dt>**Fehler vom DRM-Client**</dt> </dl>        | Eine beliebige Anzahl interner DRM-Client Fehler.<br/>                     |
| <dl> <dt>**NS \_ E \_ Gerät \_ nicht \_ WMDRM- \_ Gerät**</dt> </dl> | Das angegebene Gerät ist kein Windows Media DRM-kompatibles Gerät.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Vor dem Aufrufen dieser Methode sollte die Anwendung [**iwmdrmdeviceapp:: querydevicestatus**](iwmdrmdeviceapp-querydevicestatus.md) oder [**IWMDRMDeviceApp2:: QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) aufrufen, um zu überprüfen, ob alle DRM-Komponenten des Geräts auf dem neuesten Stand sind. Diese Methode kann nur auf einem Gerät aufgerufen werden, das Windows Media DRM 10 für tragbare Geräte unterstützt.

Die abgerufenen Daten *pbstrinmeterdata* sollten an die durch *pbstraumeterurl* angegebene URL gesendet werden. Stellen Sie sicher, dass die abgerufenen Daten URL-codiert werden, damit Sie während der Übertragung nicht geändert werden.

Weitere Informationen finden Sie [unter behandeln geschützter Inhalte in der Anwendung](handling-protected-content-in-the-application.md) .

## <a name="examples"></a>Beispiele

Im folgenden C++-Codebeispiel wird ein **wmdrmdeviceapp** -Objekt erstellt, und es wird überprüft, ob das Gerät ein Windows Media DRM 10-Gerät ist, dass seine Uhr genau ist, und dann die Messungs Daten anfordert.


```C++
HRESULT hr = S_OK;
// Create the WMDRMDeviceApp object.
CComPtr<IWMDRMDeviceApp> pDRM;
hr = pDRM.CoCreateInstance(CLSID_WMDRMDeviceApp, 0, CLSCTX_ALL);

// Find out first if the device is a WMDRM 10 device, and if it requires
// any clock updates.
DWORD status = 0;
hr = pDRM->QueryDeviceStatus(pDevice, &status);

if (!(WMDRM_DEVICE_ISWMDRM & status)) // Device is not WMDRM 10. Nothing can be updated,
    return E_FAIL;                   // and metering cannot be performed.
else if (status & WMDRM_DEVICE_REVOKED) // Device is revoked.
    return E_FAIL;
else if (status & WMDRM_DEVICE_NEEDCLOCK || 
    status & WMDRM_CLIENT_NEEDINDIV ||
    status & WMDRM_DEVICE_REFRESHCLOCK)
{
    // Need to update device clock. 
    // Using custom function, which is synchronous.
    hr = myAcquireDeviceData(pDRM, pDevice, this, status, &result);
    if (hr != S_OK || result != 0)    // Couldn't perform the updates.
        return E_FAIL;    
}

// Any updates have been performed. Now get the metering information from the device.
CComBSTR meterCert(METERCERT);
CComBSTR URL;
CComBSTR rawdata;
CComBSTR data;
hr = pDRM->GenerateMeterChallenge(pDevice, meterCert, &URL, &rawdata);
if (hr == S_OK)
    ..... Send to URL...
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmdeviceapp. h (erfordert auch wmdrmdeviceapp \_ i. c, erstellt von wmdrmdeviceapp. idl)</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>Mssachlp. lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Behandeln geschützter Inhalte in der Anwendung**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Iwmdmdevice-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[**Iwmdrmdeviceapp-Schnittstelle**](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





