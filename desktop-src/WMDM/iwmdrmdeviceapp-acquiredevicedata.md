---
title: IWMDRMDeviceApp AcquireDeviceData-Methode (WMDRMDeviceApp.h)
description: Die AcquireDeviceData-Methode initialisiert oder setzt eine sichere Geräteuhr zurück.
ms.assetid: 2f1cfdb9-0f07-4bee-94aa-b33b039453d0
keywords:
- AcquireDeviceData-Methode windows Media Geräte-Manager
- AcquireDeviceData-Methode windows Media Geräte-Manager , IWMDRMDeviceApp-Schnittstelle
- IWMDRMDeviceApp-Schnittstelle Windows Media Geräte-Manager , AcquireDeviceData-Methode
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.AcquireDeviceData
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9280a358c7124a3f16e3d303026f36506610b6dc6fe0453fdf3e7b2432682719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055643"
---
# <a name="iwmdrmdeviceappacquiredevicedata-method"></a>IWMDRMDeviceApp::AcquireDeviceData-Methode

Die **AcquireDeviceData-Methode** initialisiert oder setzt eine sichere Geräteuhr zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT AcquireDeviceData(
  [in]  IWMDMDevice    *pDevice,
  [in]  IWMDMProgress3 *pProgressCallback,
  [in]  DWORD          dwFlags,
  [out] DWORD          *pdwStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevice* \[ In\]
</dt> <dd>

Zeiger auf eine [**IWMDMDevice-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) für das Gerät, das Messungsdaten melden soll.

</dd> <dt>

*pProgressCallback* \[ In\]
</dt> <dd>

Statusrückruf, über den die Anwendung den Fortschritt des Ereignisses nachverfolgen oder das Ereignis abbrechen kann. Der Fortschritt wird durch den *EventId-Parameter* der [**IWMDMProgress3-Methoden**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) identifiziert.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Ein **logisches OR** eines oder beider der folgenden Flags, die angeben, welche Aktion sie ausführen soll. Dieser Wert wird aus dem *pdwStatus-Parameter* von [**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) oder [**IWMDRMDeviceApp2::QueryDeviceStatus2 abgerufen.**](iwmdrmdeviceapp2-querydevicestatus2.md) Sie können das *pdwStatus-Flag* direkt verwenden.



| Flag                        | Beschreibung                                   |
|-----------------------------|-----------------------------------------------|
| WMDRM \_ DEVICE \_ NEEDCLOCK    | Erwerben sie eine Uhr von einem sicheren Uhrserver.   |
| \_ \_ WMDRM-GERÄTEAKTUALISIERUNGCLOCK | Aktualisieren Sie die Uhr von einem sicheren Uhrserver. |



 

</dd> <dt>

*pdwStatus* \[ out\]
</dt> <dd>

Einer der folgenden **DWORD-Werte,** die den vom Gerät zurückgegebenen Status angeben.



| Status | Beschreibung                                                     |
|--------|-----------------------------------------------------------------|
| 0      | Die Aktion wird nicht unterstützt.                                    |
| 1      | Die sichere Uhr des Geräts konnte nicht vom Dienst erworben werden. |
| 2      | Die sichere Uhr des Geräts konnte nicht festgelegt werden.                     |
| 3      | Die sichere Uhr des Geräts wurde festgelegt.                              |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                                             | Beschreibung                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                                    | Die Methode wurde erfolgreich ausgeführt.<br/>                                                                                                    |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                                       | Mindestens ein Argument ist ungültig.<br/>                                                                                     |
| <dl> <dt>**NS \_ E GERÄT NICHT \_ \_ \_ WMDRM-GERÄT \_**</dt> </dl>                        | Das angegebene Gerät ist kein Windows Media DRM-kompatibles Gerät.<br/>                                                       |
| <dl> <dt>**NS \_ E \_ DRM KANN KEINE SICHERE \_ UHR \_ \_ \_ \_ ERHALTEN**</dt> </dl>               | Fehler beim Abrufen einer sicheren Uhr-Challenge vom Gerät oder beim Abrufen der URL der sicheren Uhr aus der Herausforderung.<br/> |
| <dl> <dt>**NS \_ E \_ DRM KANN KEINE SICHERE UHR VOM \_ \_ SERVER \_ \_ \_ \_ \_ ERHALTEN**</dt> </dl> | Fehler beim Abrufen der sicheren Uhrantwort vom sicheren Uhrserver.<br/>                                               |
| <dl> <dt>**NS \_ E \_ DRM KANN DIE SICHERE UHR \_ NICHT \_ \_ \_ \_ FESTLEGEN**</dt> </dl>               | Fehler beim Senden der sicherheitssicheren Uhr-Challenge an das Gerät, oder das Gerät konnte die Uhr nicht festlegen.<br/>                          |



 

## <a name="remarks"></a>Hinweise

Dies ist eine asynchrone Methode. Das Gerät muss auf den [**IWMDMProgress::End-Rückruf**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-end) für diesen Vorgang warten, bevor versucht wird, lizenzierte Inhalte wiederzuspielen.

Eine Anwendung kann durch Aufrufen von [**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) oder [**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md)erfahren, ob die Uhr des Geräts zurückgesetzt oder aktualisiert werden muss.

Ihre Anwendung muss über eine Internetverbindung verfügen, damit sie eine sichere Uhr erhalten oder zurücksetzen kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>WMDRMDeviceApp.h (erfordert auch Wmdrmdeviceapp \_ i.c, erstellt aus WMDRMDeviceApp.idl)</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>Mssachlp.lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Behandeln geschützter Inhalte in der Anwendung**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**IWMDMDevice-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[**IWMDMProgress3-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)
</dt> <dt>

[**IWMDRMDeviceApp-Schnittstelle**](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





