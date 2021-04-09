---
title: Imsrdpclientnonscriptable notifyredirectdevicechange-Methode
description: Benachrichtigt das Geräte Umleitungs Modul des Remotedesktop ActiveX-Steuer Elements, dass eine Geräte Änderung auf dem System aufgetreten ist. Diese Methode übergibt WM \_ devicechange-Benachrichtigungen an das-Steuerelement.
ms.assetid: 36323831-06e0-4e47-8a6c-06367119298f
ms.tgt_platform: multiple
keywords:
- Notifyredirectdevicechange-Methode Remotedesktopdienste
- Notifyredirectdevicechange-Methode Remotedesktopdienste, imsrdpclientnonscriptable-Schnittstelle
- Imsrdpclientnonscriptable-Schnittstelle Remotedesktopdienste, notifyredirectdevicechange-Methode
- Notifyredirectdevicechange-Methode Remotedesktopdienste, IMsRdpClientNonScriptable2-Schnittstelle
- IMsRdpClientNonScriptable2-Schnittstelle Remotedesktopdienste, notifyredirectdevicechange-Methode
- Notifyredirectdevicechange-Methode Remotedesktopdienste, IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3-Schnittstelle Remotedesktopdienste, notifyredirectdevicechange-Methode
- Notifyredirectdevicechange-Methode Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4-Schnittstelle Remotedesktopdienste, notifyredirectdevicechange-Methode
- Notifyredirectdevicechange-Methode Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5-Schnittstelle Remotedesktopdienste, notifyredirectdevicechange-Methode
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable2.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable3.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable4.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable5.NotifyRedirectDeviceChange
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7357fcb5e31eeeb0de5791425b8d9fada4365ab8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957131"
---
# <a name="imsrdpclientnonscriptablenotifyredirectdevicechange-method"></a>Imsrdpclientnonscriptable:: notifyredirectdevicechange-Methode

Benachrichtigt das Geräte Umleitungs Modul des Remotedesktop ActiveX-Steuer Elements, dass eine Geräte Änderung auf dem System aufgetreten ist. Diese Methode übergibt [**WM \_ devicechange**](/windows/desktop/DevIO/wm-devicechange) -Benachrichtigungen an das-Steuerelement.

## <a name="syntax"></a>Syntax


```C++
HRESULT NotifyRedirectDeviceChange(
  [in] WPARAM wParam,
  [in] LPARAM lParam
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Gibt das Geräte Ereignis an. Dieser Parameter kann einen der folgenden Werte annehmen.

<dt>

<span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>

<span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>**DBT \_ configchangeabgeb Rochen**


</dt> <dd>

Eine Anforderung zum Ändern der aktuellen Konfiguration (Andocken oder Abdocken) wurde abgebrochen.

</dd> <dt>

<span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>

<span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>**DBT- \_ ConfigChanged**


</dt> <dd>

Die aktuelle Konfiguration wurde aufgrund eines Andocken oder Abdocken geändert.

</dd> <dt>

<span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>

<span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>**DBT \_ CustomEvent**


</dt> <dd>

Ein benutzerdefiniertes Ereignis ist aufgetreten.

</dd> <dt>

<span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>

<span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>**DBT \_ devicearrival**


</dt> <dd>

Ein Gerät wurde eingefügt und ist jetzt verfügbar.

</dd> <dt>

<span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>

<span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>**DBT \_ DeviceQueryRemove**


</dt> <dd>

Die Berechtigung zum Entfernen eines Geräts wird angefordert. Jede Anwendung kann diese Anforderung verweigern und das Entfernen abbrechen.

</dd> <dt>

<span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>

<span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>**DBT \_ devicequeryremovefailed**


</dt> <dd>

Eine Anforderung zum Entfernen eines Geräts wurde abgebrochen.

</dd> <dt>

<span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>

<span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>**DBT \_ deviceremovecomplete**


</dt> <dd>

Ein Gerät wurde entfernt.

</dd> <dt>

<span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>

<span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>**DBT \_ deviceremovepending**


</dt> <dd>

Ein Gerät wird gerade entfernt. Das Entfernen kann nicht verweigert werden.

</dd> <dt>

<span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>

<span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>**DBT-Geräte- \_ /richtlinientypespecific**


</dt> <dd>

Ein Geräte spezifisches Ereignis ist aufgetreten.

</dd> <dt>

<span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>

<span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>**DBT- \_ Devnodes \_ geändert**


</dt> <dd>

Ein Gerät wurde dem System hinzugefügt oder daraus entfernt.

</dd> <dt>

<span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>

<span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>**DBT \_ querychangeconfig**


</dt> <dd>

Die Berechtigung zum Ändern der aktuellen Konfiguration (Andocken oder Abdocken) wird angefordert.

</dd> <dt>

<span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>

<span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>**DBT \_ UserDefined**


</dt> <dd>

Die Bedeutung dieser Meldung ist Benutzer definiert.

</dd> </dl> </dd> <dt>

*LPARAM* \[ in\]
</dt> <dd>

Zeiger auf eine-Struktur, die ereignisspezifische Daten enthält. Das Format hängt vom Wert des *wParam* -Parameters ab. Weitere Informationen finden Sie in der Dokumentation zu den einzelnen Ereignissen. Weitere Informationen finden Sie unter [Geräte Ereignis Typen](/windows/desktop/DevIO/device-event-types).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **\_ OK** zurück, wenn erfolgreich.

## <a name="remarks"></a>Bemerkungen

Eine Containeranwendung, die das dynamische Hinzufügen oder Entfernen von Geräten zulässt, sollte die [**WM \_ devicechange**](/windows/desktop/DevIO/wm-devicechange) -Nachricht im Fenster der obersten Ebene verarbeiten und die Nachricht mithilfe der **notifyredirectdevicechange** -Methode an das Steuerelement weiterleiten. Ein Beispiel für eine dynamische Geräte Änderung ist, wenn ein umgeleitetes Laufwerk hinzugefügt oder entfernt wird, während das System ausgeführt wird.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                               |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| IID<br/>                      | IID \_ imsrdpclientnonscriptable ist als 2f079c4c-87b2-4afd-97ab-20cdb43038ae definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**Imsrdpclientnonscriptable**](imsrdpclientnonscriptable-interface.md)
</dt> </dl>

 

