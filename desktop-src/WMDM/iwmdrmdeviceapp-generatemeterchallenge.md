---
title: IWMDRMDeviceApp GenerateMeterChallenge-Methode (WMDRMDeviceApp.h)
description: Die GenerateMeterChallenge-Methode erfasst Messdaten von einem Gerät.
ms.assetid: 2457cab7-bd45-49a7-ba69-74ae022207ce
keywords:
- GenerateMeterChallenge-Methode windows Media Geräte-Manager
- GenerateMeterChallenge-Methode windows Media Geräte-Manager , IWMDRMDeviceApp-Schnittstelle
- IWMDRMDeviceApp-Schnittstelle windows Media Geräte-Manager , GenerateMeterChallenge-Methode
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
ms.openlocfilehash: e91ac5049740d360ae0c5f53959b3d952188bfa2a569c58a9e7cf86ae0c22577
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584549"
---
# <a name="iwmdrmdeviceappgeneratemeterchallenge-method"></a>IWMDRMDeviceApp::GenerateMeterChallenge-Methode

Die **GenerateMeterChallenge-Methode** erfasst Messdaten von einem Gerät.

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

*pDevice* \[ In\]
</dt> <dd>

Zeiger auf eine [**IWMDMDevice-Schnittstelle.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) Wenn die Anwendung **NULL** übergibt, werden auf dem Computer gespeicherte Messungsinformationen anstelle von Messungsinformationen von einem verbundenen Gerät verwendet.

</dd> <dt>

*bstrMeterCert* \[ In\]
</dt> <dd>

Das Messungszertifikat der Anwendung als **BSTR.** Dies ist ein signiertes Zertifikat, das von Microsoft empfangen wurde.

</dd> <dt>

*pbstrMeterURL* \[ out\]
</dt> <dd>

Die URL, an die Messungsdaten gesendet werden sollen. Dies wird von Windows Media Geräte-Manager zugeordnet und muss vom Aufrufer mit **sysFreeString** kostenlos sein.

</dd> <dt>

*pbstrMeterData* \[ out\]
</dt> <dd>

Messungsdaten, die an den Messungsdienst gesendet werden sollen. Dies wird von Windows Media Geräte-Manager zugeordnet und muss vom Aufrufer mit **sysFreeString** kostenlos sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                      | Beschreibung                                                                   |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                             | Die Methode wurde erfolgreich ausgeführt.<br/>                                              |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                | Mindestens ein Argument ist ungültig.<br/>                               |
| <dl> <dt>**DRM \_ E \_ INVALIDXMLTAG**</dt> </dl>             | XML ist nicht ordnungsgemäß formatiert.<br/>                                          |
| <dl> <dt>**DRM \_ E \_ NOXMLCLOSETAG**</dt> </dl>             | XML ist nicht ordnungsgemäß formatiert.<br/>                                          |
| <dl> <dt>**DRM \_ E \_ NOXMLOPENTAG**</dt> </dl>              | XML ist nicht ordnungsgemäß formatiert.<br/>                                          |
| <dl> <dt>**DRM \_ E \_ XMLNOTFOUND**</dt> </dl>               | Fehler beim Suchen eines erforderlichen XML-Tags.<br/>                                 |
| <dl> <dt>**Fehler vom Gerät**</dt> </dl>            | Eine beliebige Anzahl von Gerätefehlern.<br/>                                  |
| <dl> <dt>**Fehler vom DRM-Client**</dt> </dl>        | Eine beliebige Anzahl interner DRM-Clientfehler.<br/>                     |
| <dl> <dt>**NS \_ E \_ DEVICE \_ NOT \_ WMDRM \_ DEVICE**</dt> </dl> | Das angegebene Gerät ist kein Windows Medien-DRM-kompatibles Gerät.<br/> |



 

## <a name="remarks"></a>Hinweise

Vor dem Aufrufen dieser Methode sollte die Anwendung [**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) oder [**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) aufrufen, um sicherzustellen, dass alle DRM-Komponenten des Geräts auf dem neuesten Stand sind. Diese Methode kann nur auf einem Gerät aufgerufen werden, das Windows Media DRM 10 für portable Geräte unterstützt.

Die abgerufenen Daten *pbstrMeterData* sollten an die url gesendet werden, die von *pbstrMeterURL* angegeben wird. Achten Sie darauf, die abgerufenen Daten url-encode zu codieren, damit sie während der Übertragung nicht geändert werden.

Weitere Informationen finden Sie [unter Behandeln von geschützten Inhalten in der Anwendung.](handling-protected-content-in-the-application.md)

## <a name="examples"></a>Beispiele

Im folgenden C++-Codebeispiel wird ein **WMDRMDeviceApp-Objekt** erstellt, überprüft, ob es sich bei dem Gerät um ein Windows Media DRM 10-Gerät handelt, ob seine Uhr genau ist, und fordert dann die Messungsdaten an.


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
| Header<br/>  | <dl> <dt>WMDRMDeviceApp.h (erfordert auch Wmdrmdeviceapp \_ i.c, erstellt aus WMDRMDeviceApp.idl)</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>Mssachlp.lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Behandeln von geschützten Inhalten in der Anwendung**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**IWMDMDevice-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[**IWMDRMDeviceApp-Schnittstelle**](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





