---
title: Methode ' iwmdrmdeviceapp acquiredevicedata ' (wmdrmdeviceapp. h)
description: Die acquiredevicedata-Methode initialisiert oder setzt eine sichere Uhr des Geräts zurück.
ms.assetid: 2f1cfdb9-0f07-4bee-94aa-b33b039453d0
keywords:
- Acquiredevicedata-Methode, Windows Media Device Manager
- Acquiredevicedata-Methode Windows Media Device Manager, iwmdrmdeviceapp-Schnittstelle
- Iwmdrmdeviceapp-Schnittstelle Windows Media Device Manager, acquiredevicedata-Methode
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
ms.openlocfilehash: 268572e5dad3dffd0fe15956a0ff145f277fb6db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368522"
---
# <a name="iwmdrmdeviceappacquiredevicedata-method"></a>Iwmdrmdeviceapp:: acquiredevicedata-Methode

Die **acquiredevicedata** -Methode initialisiert oder setzt eine sichere Uhr des Geräts zurück.

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

*pdevice* \[ in\]
</dt> <dd>

Zeiger auf eine [**iwmdmdevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) -Schnittstelle für das Gerät, das Messungs Daten meldet.

</dd> <dt>

*pprogresscallback* \[ in\]
</dt> <dd>

Der Fortschritts Rückruf, über den die Anwendung den Status des Ereignisses verfolgen kann, oder das Ereignis abbrechen. Der Fortschritt wird durch den *EventID-* Parameter der [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) -Methoden identifiziert.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Ein logisches **or** von einem oder beiden der folgenden Flags, das angibt, welche Aktion ausgeführt werden soll. Dieser Wert wird aus dem *pdwstatus* -Parameter von [**iwmdrmdeviceapp:: querydevicestatus**](iwmdrmdeviceapp-querydevicestatus.md) oder [**IWMDRMDeviceApp2:: QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md)abgerufen. Sie können das *pdwstatus* -Flag direkt verwenden.



| Flag                        | Beschreibung                                   |
|-----------------------------|-----------------------------------------------|
| WMDRM- \_ Geräte- \_ needclock    | Erwerben Sie eine Uhr von einem sicheren Uhr-Server.   |
| WMDRM- \_ Geräte \_ Erfrischung | Aktualisieren Sie die Uhr von einem sicheren Uhr-Server. |



 

</dd> <dt>

*pdwstatus* \[ vorgenommen\]
</dt> <dd>

Einer der folgenden **DWORD** -Werte, der den vom Gerät zurückgegebenen Status angibt.



| Status | BESCHREIBUNG                                                     |
|--------|-----------------------------------------------------------------|
| 0      | Die Aktion wird nicht unterstützt.                                    |
| 1      | Die sichere Uhr des Geräts konnte nicht vom Dienst abgerufen werden. |
| 2      | Die sichere Uhr des Geräts konnte nicht festgelegt werden.                     |
| 3      | Die sichere Uhr des Geräts wurde festgelegt.                              |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                                             | Beschreibung                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                                    | Die Methode wurde erfolgreich ausgeführt.<br/>                                                                                                    |
| <dl> <dt>**DRM \_ E \_ invalidArg**</dt> </dl>                                       | Mindestens ein Argument ist ungültig.<br/>                                                                                     |
| <dl> <dt>**NS \_ E \_ Gerät \_ nicht \_ WMDRM- \_ Gerät**</dt> </dl>                        | Das angegebene Gerät ist kein Windows Media DRM-kompatibles Gerät.<br/>                                                       |
| <dl> <dt>**NS \_ E \_ DRM \_ kann \_ keine \_ \_ sichere \_ Uhr erhalten.**</dt> </dl>               | Fehler beim Abrufen der sicherheitstokenaufforderung vom Gerät, oder die URL der sicheren Uhr konnte nicht abgerufen werden.<br/> |
| <dl> <dt>**NS \_ E \_ DRM \_ kann \_ keine \_ \_ sichere \_ Uhr \_ vom \_ Server erhalten.**</dt> </dl> | Fehler beim Abrufen der Antwort auf sichere Uhr vom Sicherheitstokenserver.<br/>                                               |
| <dl> <dt>**NS \_ E \_ DRM \_ kann \_ \_ \_ sichere Uhr nicht \_ festlegen**</dt> </dl>               | Fehler beim Senden der Anforderung für die sichere Uhr an das Gerät, oder das Gerät konnte die Uhr nicht festlegen.<br/>                          |



 

## <a name="remarks"></a>Bemerkungen

Dabei handelt es sich um eine asynchrone Methode. das Gerät muss den [**iwmdmprogress:: End**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-end) -Rückruf für diesen Vorgang abwarten, bevor er versucht, lizenzierte Inhalte wiederzugeben.

Eine Anwendung kann lernen, ob das Gerät durch Aufrufen von [**iwmdrmdeviceapp:: querydevicestatus**](iwmdrmdeviceapp-querydevicestatus.md) oder [**IWMDRMDeviceApp2:: QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md)die Uhr zurücksetzen oder aktualisieren muss.

Die Anwendung muss über eine Internet Verbindung verfügen, damit Sie eine sichere Uhr abrufen oder zurücksetzen kann.

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

[**IWMDMProgress3-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)
</dt> <dt>

[**Iwmdrmdeviceapp-Schnittstelle**](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





