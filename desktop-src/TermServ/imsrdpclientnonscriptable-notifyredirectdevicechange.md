---
title: IMsRdpClientNonScriptable NotifyRedirectDeviceChange-Methode
description: Benachrichtigt das Geräteumleitungsmodul des Remotedesktop ActiveX, dass eine Geräteänderung auf dem System aufgetreten ist. Diese Methode übergibt WM \_ DEVICECHANGE-Benachrichtigungen an das Steuerelement.
ms.assetid: 36323831-06e0-4e47-8a6c-06367119298f
ms.tgt_platform: multiple
keywords:
- NotifyRedirectDeviceChange-Remotedesktopdienste
- NotifyRedirectDeviceChange-Methode Remotedesktopdienste , IMsRdpClientNonScriptable-Schnittstelle
- IMsRdpClientNonScriptable-Schnittstelle Remotedesktopdienste , NotifyRedirectDeviceChange-Methode
- NotifyRedirectDeviceChange-Methode Remotedesktopdienste , IMsRdpClientNonScriptable2-Schnittstelle
- IMsRdpClientNonScriptable2-Schnittstelle Remotedesktopdienste , NotifyRedirectDeviceChange-Methode
- NotifyRedirectDeviceChange-Methode Remotedesktopdienste , IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3-Schnittstelle Remotedesktopdienste , NotifyRedirectDeviceChange-Methode
- NotifyRedirectDeviceChange-Methode Remotedesktopdienste , IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4-Schnittstelle Remotedesktopdienste , NotifyRedirectDeviceChange-Methode
- NotifyRedirectDeviceChange-Remotedesktopdienste , IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5-Schnittstelle Remotedesktopdienste , NotifyRedirectDeviceChange-Methode
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
ms.openlocfilehash: 37986a218f672f5ace6d81b6496b958547e70a95f8ddea91bf6a130eb05b1ed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130077"
---
# <a name="imsrdpclientnonscriptablenotifyredirectdevicechange-method"></a>IMsRdpClientNonScriptable::NotifyRedirectDeviceChange-Methode

Benachrichtigt das Geräteumleitungsmodul des Remotedesktop ActiveX, dass eine Geräteänderung auf dem System aufgetreten ist. Diese Methode übergibt [**WM \_ DEVICECHANGE-Benachrichtigungen**](/windows/desktop/DevIO/wm-devicechange) an das Steuerelement.

## <a name="syntax"></a>Syntax


```C++
HRESULT NotifyRedirectDeviceChange(
  [in] WPARAM wParam,
  [in] LPARAM lParam
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Gibt das Geräteereignis an. Dieser Parameter kann einen der folgenden Werte annehmen.

<dt>

<span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>

<span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>**DBT \_ CONFIGCHANGECANCELED**


</dt> <dd>

Eine Anforderung zum Ändern der aktuellen Konfiguration (Dock oder Abdocken) wurde abgebrochen.

</dd> <dt>

<span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>

<span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>**DBT \_ CONFIGCHANGED**


</dt> <dd>

Die aktuelle Konfiguration wurde aufgrund eines Andocks oder Abdockens geändert.

</dd> <dt>

<span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>

<span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>**DBT \_ CUSTOMEVENT**


</dt> <dd>

Ein benutzerdefiniertes Ereignis ist aufgetreten.

</dd> <dt>

<span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>

<span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>**DBT \_ DEVICEARRARRARR**


</dt> <dd>

Ein Gerät wurde eingefügt und ist jetzt verfügbar.

</dd> <dt>

<span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>

<span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>**DBT \_ DEVICEQUERYREMOVE**


</dt> <dd>

Die Berechtigung zum Entfernen eines Geräts wird angefordert. Jede Anwendung kann diese Anforderung verweigern und die Entfernung abbrechen.

</dd> <dt>

<span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>

<span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>**DBT \_ DEVICEQUERYREMOVEFAILED**


</dt> <dd>

Eine Anforderung zum Entfernen eines Geräts wurde abgebrochen.

</dd> <dt>

<span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>

<span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>**DBT \_ DEVICEREMOVECOMPLETE**


</dt> <dd>

Ein Gerät wurde entfernt.

</dd> <dt>

<span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>

<span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>**DBT \_ DEVICEREMOVEPENDING**


</dt> <dd>

Ein Gerät wird entfernt. Das Entfernen kann nicht verweigert werden.

</dd> <dt>

<span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>

<span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>**DBT \_ DEVICETYPESPECIFIC**


</dt> <dd>

Ein gerätespezifisches Ereignis ist aufgetreten.

</dd> <dt>

<span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>

<span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>**DBT \_ DEVNODES \_ GEÄNDERT**


</dt> <dd>

Ein Gerät wurde dem System hinzugefügt oder daraus entfernt.

</dd> <dt>

<span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>

<span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>**DBT \_ QUERYCHANGECONFIG**


</dt> <dd>

Die Berechtigung zum Ändern der aktuellen Konfiguration (Dock oder Abdocken) wird angefordert.

</dd> <dt>

<span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>

<span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>**DBT \_ USERDEFINED**


</dt> <dd>

Die Bedeutung dieser Nachricht ist benutzerdefiniert.

</dd> </dl> </dd> <dt>

*lParam* \[ In\]
</dt> <dd>

Zeiger auf eine -Struktur, die ereignisspezifische Daten enthält. Das Format hängt vom Wert des *wParam-Parameters* ab. Weitere Informationen finden Sie in der Dokumentation zu jedem Ereignis. Weitere Informationen finden Sie unter [Geräteereignistypen.](/windows/desktop/DevIO/device-event-types)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Geben Sie **S \_ OK zurück,** wenn erfolgreich.

## <a name="remarks"></a>Hinweise

Eine Containeranwendung, die das dynamische Addition oder Entfernen von Geräten zulässt, sollte die [**WM \_ DEVICECHANGE-Nachricht**](/windows/desktop/DevIO/wm-devicechange) im Fenster der obersten Ebene verarbeiten und die Nachricht mithilfe der **NotifyRedirectDeviceChange-Methode** an das Steuerelement weiterleiten. Ein Beispiel für eine dynamische Geräteänderung ist, wenn ein umgeleitetes Laufwerk hinzugefügt oder entfernt wird, während das System ausgeführt wird.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                               |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable ist als 2f079c4c-87b2-4afd-97ab-20cdb43038ae definiert.<br/> |



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

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> </dl>

 

