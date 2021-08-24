---
title: IWMDRMDeviceApp SynchronizeLicenses-Methode (WMDRMDeviceApp.h)
description: Die SynchronizeLicenses-Methode aktualisiert Lizenzen auf einem Gerät, wenn sie demnächst ablaufen.
ms.assetid: 352378c1-7432-476c-98e9-d811165c020e
keywords:
- SynchronizeLicenses-Methodenfenster Media Geräte-Manager
- SynchronizeLicenses-Methodenfenster Media Geräte-Manager , IWMDRMDeviceApp-Schnittstelle
- IWMDRMDeviceApp-Schnittstelle windows Media Geräte-Manager , SynchronizeLicenses-Methode
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
ms.openlocfilehash: 91ec48743bf52d990c64ce1aecf30897a7ee2f51664e88695a181f9d4f758140
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031740"
---
# <a name="iwmdrmdeviceappsynchronizelicenses-method"></a>IWMDRMDeviceApp::SynchronizeLicenses-Methode

Die **SynchronizeLicenses-Methode** aktualisiert Lizenzen auf einem Gerät, wenn sie demnächst ablaufen.

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

*pDevice* \[ In\]
</dt> <dd>

Zeiger auf ein [**IWMDMDevice-Objekt.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)

</dd> <dt>

*pProgressCallback* \[ In\]
</dt> <dd>

Statusrückruf, der den Fortschritt aller Schritte empfängt, die ggf. ausgeführt werden müssen. Der Schritt wird durch den *EventId-Parameter* der aufgerufenen [**IWMDMProgress3-Methode**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) identifiziert.

</dd> <dt>

*cMinCountThreshold* \[ In\]
</dt> <dd>

Optionale Mindestanzahl verbleibender Wiedergaben für eine Gerätelizenz.

</dd> <dt>

*cMinHoursThreshold* \[ In\]
</dt> <dd>

Optionale verbleibende Mindeststunden für eine Gerätelizenz.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                         | Beschreibung                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                | Die Methode wurde erfolgreich ausgeführt.<br/>                                                                                                                            |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                   | Mindestens ein Argument ist ungültig.<br/>                                                                                                             |
| <dl> <dt>**DRM \_ E \_ INVALIDXMLTAG**</dt> </dl>                | XML ist nicht ordnungsgemäß formatiert.<br/>                                                                                                                        |
| <dl> <dt>**DRM \_ E \_ NOTIMPL**</dt> </dl>                      | Diese Funktionalität ist derzeit nicht implementiert. (SyncLicenses w/ *pDevice* =NULL)<br/>                                                               |
| <dl> <dt>**DRM \_ E \_ NOXMLCLOSETAG**</dt> </dl>                | Die Lizenz-XML wurde nicht ordnungsgemäß formatiert.<br/>                                                                                                           |
| <dl> <dt>**DRM \_ E \_ NOXMLOPENTAG**</dt> </dl>                 | Die Lizenz-XML wurde nicht ordnungsgemäß formatiert.<br/>                                                                                                           |
| <dl> <dt>**DRM \_ E \_ OUTOFMEMORY**</dt> </dl>                  | Nicht genügend Arbeitsspeicher.<br/>                                                                                                                                   |
| <dl> <dt>**DRM \_ E \_ XMLNOTFOUND**</dt> </dl>                  | Fehler beim Suchen eines erforderlichen XML-Tags in der Lizenz.<br/>                                                                                                |
| <dl> <dt>**NS \_ E \_ DEVICE \_ NOT \_ WMDRM \_ DEVICE**</dt> </dl>    | Das angegebene Gerät ist kein Windows Medien-DRM-kompatibles Gerät.<br/>                                                                               |
| <dl> <dt>**NS \_ E \_ DRM ERFORDERT \_ \_ INDIVIDUALISIERUNG**</dt> </dl> | Das DRM erfordert eine individualisierte Blackbox, um diese Funktion auszuführen. Anders ausgedrückt: Das Windows Media Format SDK erfordert ein Sicherheitsupgrade.<br/> |



 

## <a name="remarks"></a>Hinweise

Dieser Aufruf kann nur auf einem Gerät erfolgen, das Windows Media DRM 10 für portable Geräte unterstützt. Sie müssen mindestens einen Schwellenwertparameter angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>WMDRMDeviceApp.h (erfordert auch Wmdrmdeviceapp \_ i.c, erstellt aus WMDRMDeviceApp.idl)</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>Mssachlp.lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Behandeln von geschützten Inhalten in der Anwendung**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**IWMDMProgress3-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)
</dt> <dt>

[**IWMDRMDeviceApp-Schnittstelle**](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





