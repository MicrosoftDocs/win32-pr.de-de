---
title: Iwmdrmdeviceapp querydevicestatus-Methode (wmdrmdeviceapp. h)
description: Die querydevicestatus-Methode fragt ein Gerät nach dem aktuellen DRM-Status und den zugehörigen Funktionen ab.
ms.assetid: cd5a75d5-d7f8-4077-a9fc-6e7ddd7c796b
keywords:
- Querydevicestatus-Methode, Windows Media Device Manager
- Querydevicestatus-Methode Windows Media Device Manager, iwmdrmdeviceapp-Schnittstelle
- Iwmdrmdeviceapp-Schnittstelle Windows Media Device Manager, querydevicestatus-Methode
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.QueryDeviceStatus
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8e0f4fad5ff9026ce70fc21712506eb4796d76b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369692"
---
# <a name="iwmdrmdeviceappquerydevicestatus-method"></a>Iwmdrmdeviceapp:: querydevicestatus-Methode

Die **querydevicestatus** -Methode fragt ein Gerät nach dem aktuellen DRM-Status und den zugehörigen Funktionen ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT QueryDeviceStatus(
  [in]  IWMDMDevice *pDevice,
  [out] DWORD       *pdwStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdevice* \[ in\]
</dt> <dd>

Zeiger auf ein [**iwmdmdevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) -Objekt.

</dd> <dt>

*pdwstatus* \[ vorgenommen\]
</dt> <dd>

NULL oder mehr der folgenden **DWORD** -Werte, die die DRM-Aspekte des Geräts beschreiben, kombiniert mit einem bitweisen **or**. Siehe Hinweise.



| Status                      | BESCHREIBUNG                                  |
|-----------------------------|----------------------------------------------|
| WMDRM- \_ Gerät \_ iswmdrm      | Das Gerät unterstützt Windows Media DRM.       |
| WMDRM- \_ Geräte- \_ needclock    | Das Gerät hat keine sichere Uhr.     |
| WMDRM- \_ Gerät gesperrt \_      | Das Gerät wurde widerrufen.                 |
| WMDRM- \_ Client- \_ needindiv    | Die DRM-Sicherheit muss individualisiert werden. |
| WMDRM- \_ Geräte \_ Erfrischung | Die Uhr muss aktualisiert werden.             |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                              | Beschreibung                                                               |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                     | Die Methode wurde erfolgreich ausgeführt.<br/>                                          |
| <dl> <dt>**DRM \_ E \_ invalidArg**</dt> </dl>                        | Das Eingabe Argument ist ungültig.<br/>                               |
| <dl> <dt>**\_Ungültiges NS E- \_ DRM- \_ \_ Zertifikat**</dt> </dl>          | Das vom Gerät abgerufene Gerätezertifikat ist ungültig.<br/> |
| <dl> <dt>**NS \_ E \_ DRM \_ kann \_ das \_ \_ Geräte \_ Zertifikat nicht erhalten.**</dt> </dl> | Fehler beim Abrufen des Geräte Zertifikats vom Gerät.<br/>     |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode sollte aufgerufen werden, bevor Eingeschränkte Aktionen für DRM-Inhalte durchgeführt werden, z. b. das Übertragen von DRM-Inhalten auf das Gerät oder das Abrufen von Messungs Informationen. Wenn die von *pdwstatus* abgerufenen Werte angeben, dass eine Aktion ausgeführt werden muss (z. b. die individuelle Bereitstellung des Desktops oder das Abrufen einer Uhr für das Gerät), sollte die Anwendung [**acquiredevicedata**](iwmdrmdeviceapp-acquiredevicedata.md) aufrufen und den abgerufenen *pdwstatus* -Wert aus dieser Funktion an den *dwFlags* -Parameter in **acquiredevicedata** übergeben. Wenn 0 (null) zurückgegeben wird, unterstützt das Gerät Windows Media DRM 10 für tragbare Geräte nicht, und es müssen keine Aktionen durchgeführt werden. Weitere Informationen finden Sie [unter behandeln geschützter Inhalte in der Anwendung](handling-protected-content-in-the-application.md) .

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

[**Iwmdrmdeviceapp-Schnittstelle**](iwmdrmdeviceapp.md)
</dt> <dt>

[**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md)
</dt> </dl>

 

 





