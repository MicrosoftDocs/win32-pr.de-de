---
title: Iwmdrmdeviceapp-synchronizelicenses-Methode (wmdrmdeviceapp. h)
description: Die synchronizelicenses-Methode aktualisiert Lizenzen auf einem Gerät, wenn Sie fast abgelaufen sind.
ms.assetid: 352378c1-7432-476c-98e9-d811165c020e
keywords:
- Synchronizelicenses-Methode Windows Media Device Manager
- Synchronizelicenses-Methode, Windows Media Device Manager, iwmdrmdeviceapp-Schnittstelle
- Iwmdrmdeviceapp-Schnittstelle Windows Media Device Manager, synchronizelicenses-Methode
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.SynchronizeLicenses
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b08f3457fec55a0eb519419feddf4594a2cbfac0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372112"
---
# <a name="iwmdrmdeviceappsynchronizelicenses-method"></a>Iwmdrmdeviceapp:: synchronizelicenses-Methode

Die **synchronizelicenses** -Methode aktualisiert Lizenzen auf einem Gerät, wenn Sie fast abgelaufen sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT SynchronizeLicenses(
  [in] IWMDMDevice    *pDevice,
  [in] IWMDMProgress3 *pProgressCallback,
  [in] DWORD          cMinCountThreshold,
  [in] DWORD          cMinHoursThreshold
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdevice* \[ in\]
</dt> <dd>

Zeiger auf ein [**iwmdmdevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) -Objekt.

</dd> <dt>

*pprogresscallback* \[ in\]
</dt> <dd>

Status Rückruf, der den Fortschritt von eventuell auszuführenden Schritten empfängt. Der Schritt wird durch den *EventID-* Parameter der [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) -Methode identifiziert, die aufgerufen wird.

</dd> <dt>

*cminzählthreshold* \[ in\]
</dt> <dd>

Optionale minimale Anzahl von verbleibenden spielen für eine Geräte Lizenz.

</dd> <dt>

*cminhoursthreshold* \[ in\]
</dt> <dd>

Die optionalen minimalen verbleibenden Stunden für eine Geräte Lizenz.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                         | Beschreibung                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                | Die Methode wurde erfolgreich ausgeführt.<br/>                                                                                                                            |
| <dl> <dt>**DRM \_ E \_ invalidArg**</dt> </dl>                   | Mindestens ein Argument ist ungültig.<br/>                                                                                                             |
| <dl> <dt>**DRM \_ E \_ invalidxmltag**</dt> </dl>                | XML ist nicht ordnungsgemäß formatiert.<br/>                                                                                                                        |
| <dl> <dt>**DRM \_ E \_ notimpl**</dt> </dl>                      | Diese Funktion ist zurzeit nicht implementiert. (Synclicenses w/ *pdevice* = null)<br/>                                                               |
| <dl> <dt>**DRM \_ E \_ noxmlclosetag**</dt> </dl>                | Die Lizenz-XML-Datei wurde nicht ordnungsgemäß formatiert.<br/>                                                                                                           |
| <dl> <dt>**DRM \_ E \_ noxmlopentag**</dt> </dl>                 | Die Lizenz-XML-Datei wurde nicht ordnungsgemäß formatiert.<br/>                                                                                                           |
| <dl> <dt>**DRM- \_ E- \_ outo-Speicher**</dt> </dl>                  | Nicht genügend Arbeitsspeicher.<br/>                                                                                                                                   |
| <dl> <dt>**DRM \_ E \_ xmlnotfound**</dt> </dl>                  | Fehler beim Suchen eines erforderlichen XML-Tags in der Lizenz.<br/>                                                                                                |
| <dl> <dt>**NS \_ E \_ Gerät \_ nicht \_ WMDRM- \_ Gerät**</dt> </dl>    | Das angegebene Gerät ist kein Windows Media DRM-kompatibles Gerät.<br/>                                                                               |
| <dl> <dt>**NS \_ E \_ DRM \_ benötigt \_ Individualisierung**</dt> </dl> | Das DRM erfordert ein individualisiertes schwarzes Kästchen, um diese Funktion auszuführen. Anders ausgedrückt: für das Windows Media-Format-SDK ist ein Sicherheits Upgrade erforderlich.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Dieser Rückruf kann nur auf einem Gerät erfolgen, das Windows Media DRM 10 für tragbare Geräte unterstützt. Sie müssen mindestens einen Schwellenwert Parameter angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmdeviceapp. h (erfordert auch wmdrmdeviceapp \_ i. c, erstellt von wmdrmdeviceapp. idl)</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>Mssachlp. lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Behandeln geschützter Inhalte in der Anwendung**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**IWMDMProgress3-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)
</dt> <dt>

[**Iwmdrmdeviceapp-Schnittstelle**](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





