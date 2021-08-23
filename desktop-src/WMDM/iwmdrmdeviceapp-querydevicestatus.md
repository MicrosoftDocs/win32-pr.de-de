---
title: IWMDRMDeviceApp QueryDeviceStatus-Methode (WMDRMDeviceApp.h)
description: Die QueryDeviceStatus-Methode fragt ein Gerät nach seinem aktuellen DRM-Status und seinen Funktionen ab.
ms.assetid: cd5a75d5-d7f8-4077-a9fc-6e7ddd7c796b
keywords:
- QueryDeviceStatus-Methode windows Media Geräte-Manager
- QueryDeviceStatus-Methode windows Media Geräte-Manager , IWMDRMDeviceApp-Schnittstelle
- IWMDRMDeviceApp-Schnittstelle windows Media Geräte-Manager , QueryDeviceStatus-Methode
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
ms.openlocfilehash: b169412104a5e22ae973542457d08bead328ea4ded5a34691499ea8dbfd8b7b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055642"
---
# <a name="iwmdrmdeviceappquerydevicestatus-method"></a>IWMDRMDeviceApp::QueryDeviceStatus-Methode

Die **QueryDeviceStatus-Methode** fragt ein Gerät nach seinem aktuellen DRM-Status und seinen Funktionen ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT QueryDeviceStatus(
  [in]  IWMDMDevice *pDevice,
  [out] DWORD       *pdwStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevice* \[ In\]
</dt> <dd>

Zeiger auf ein [**IWMDMDevice-Objekt.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)

</dd> <dt>

*pdwStatus* \[ out\]
</dt> <dd>

Null oder mehr der folgenden **DWORD-Werte,** die die DRM-Aspekte des Geräts beschreiben, kombiniert mit einem bitweisen **OR.** Siehe Hinweise.



| Status                      | Beschreibung                                  |
|-----------------------------|----------------------------------------------|
| WMDRM \_ DEVICE \_ ISWMDRM      | Das Gerät unterstützt Windows Medien-DRM.       |
| WMDRM \_ DEVICE \_ NEEDCLOCK    | Das Gerät verfügt nicht über eine sichere Uhr.     |
| \_WMDRM-GERÄT \_ WIDERRUFEN      | Das Gerät wurde widerrufen.                 |
| \_WMDRM-CLIENT \_ NEEDINDIV    | Die DRM-Sicherheit muss individualisiert werden. |
| WMDRM \_ DEVICE \_ REFRESHCLOCK | Die Uhr muss aktualisiert werden.             |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                              | Beschreibung                                                               |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                     | Die Methode wurde erfolgreich ausgeführt.<br/>                                          |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                        | Das Eingabeargument ist ungültig.<br/>                               |
| <dl> <dt>**UNGÜLTIGES \_ \_ NS E-DRM-ZERTIFIKAT \_ \_**</dt> </dl>          | Das vom Gerät abgerufene Gerätezertifikat ist ungültig.<br/> |
| <dl> <dt>**NS \_ E \_ DRM KANN \_ \_ \_ \_ \_ GERÄTEZERTIFIKAT NICHT ABRUFEN**</dt> </dl> | Fehler beim Abrufen des Gerätezertifikats vom Gerät.<br/>     |



 

## <a name="remarks"></a>Hinweise

Diese Methode sollte aufgerufen werden, bevor Sie eingeschränkte Aktionen für DRM-Inhalte ausführen, z. B. das Übertragen von DRM-Inhalten auf das Gerät oder das Abrufen von Messungsinformationen. Wenn die von *pdwStatus* abgerufenen Werte angeben, dass eine Aktion ausgeführt werden muss (z. B. Individualisierung für den Desktop oder Abrufen einer Uhr für das Gerät), sollte die Anwendung [**AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) aufrufen und den abgerufenen *pdwStatus-Wert* von dieser Funktion an den *dwFlags-Parameter* in **AcquireDeviceData** übergeben. Wenn 0 (null) zurückgegeben wird, unterstützt das Gerät Windows Media DRM 10 für portable Geräte nicht, und es müssen keine Aktionen ausgeführt werden. Weitere Informationen finden Sie [unter Behandeln von geschützten Inhalten in der Anwendung.](handling-protected-content-in-the-application.md)

## <a name="examples"></a>Beispiele

Im folgenden C++-Codebeispiel wird ein **WMDRMDeviceApp-Objekt** erstellt, überprüft, ob es sich bei dem Gerät um ein Windows Media DRM 10-Gerät handelt, ob seine Uhr korrekt ist, und fordert dann die Messdaten an.


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
| Header<br/>  | <dl> <dt>WMDRMDeviceApp.h (erfordert auch Wmdrmdeviceapp \_ i.c, erstellt aus WMDRMDeviceApp.idl)</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>Mssachlp.lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Behandeln von geschützten Inhalten in der Anwendung**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**IWMDRMDeviceApp-Schnittstelle**](iwmdrmdeviceapp.md)
</dt> <dt>

[**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md)
</dt> </dl>

 

 





