---
title: Remotecontrol-Methode der Win32_TSRemoteControlSetting-Klasse
description: Die Methode "levelofcontrol" wird von der remotecontrol-Methode festgelegt.
ms.assetid: 341f4f8d-17be-4482-834a-b771e041cfec
ms.tgt_platform: multiple
keywords:
- Remotecontrol-Methode Remotedesktopdienste
- Remotecontrol-Methode Remotedesktopdienste, Win32_TSRemoteControlSetting-Klasse
- Win32_TSRemoteControlSetting-Klasse Remotedesktopdienste, remotecontrol-Methode
topic_type:
- apiref
api_name:
- Win32_TSRemoteControlSetting.RemoteControl
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9476269c2f619b7ea46bc6546f106d7ccd2a486e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340628"
---
# <a name="remotecontrol-method-of-the-win32_tsremotecontrolsetting-class"></a>Remotecontrol-Methode der Win32- \_ Klasse "zremotecontrolsetting"

Die Methode " **levelofcontrol** " wird von der **remotecontrol** -Methode festgelegt.

## <a name="syntax"></a>Syntax


```mof
uint32 RemoteControl(
  [in] uint32 LevelOfControl
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Levelofcontrol* \[ in\]
</dt> <dd>

Neuer Wert für die **levelofcontrol** -Eigenschaft, die angibt, ob die Sitzung nur vom Remote Benutzer angezeigt wird oder über Tastatur und Maus angezeigt und gesteuert wird. Weitere Informationen finden Sie im Abschnitt "Hinweise". Die folgenden Werte werden unterstützt.

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Deaktivieren** (0)


</dt> <dd>

Die Remote Steuerung ist deaktiviert.

</dd> <dt>

<span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>

<span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**EnableInputNotify** (1)


</dt> <dd>

Der Benutzer der Remote Steuerung hat die vollständige Kontrolle über die Sitzung des Benutzers mit der Berechtigung des Benutzers.

</dd> <dt>

<span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>

<span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**EnableInputNoNotify** (2)


</dt> <dd>

Der Benutzer der Remote Steuerung hat die vollständige Kontrolle über die Sitzung des Benutzers. die Berechtigung des Benutzers ist nicht erforderlich.

</dd> <dt>

<span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>

<span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**EnableNoInputNotify** (3)


</dt> <dd>

Der Benutzer der Remote Steuerung kann die Sitzung Remote mit der Berechtigung des Benutzers anzeigen. der Remote Benutzer kann die Sitzung nicht aktiv steuern.

</dd> <dt>

<span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>

<span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**EnableNoInputNoNotify** (4)


</dt> <dd>

Der Benutzer der Remote Steuerung kann die Sitzung Remote anzeigen, aber die Sitzung nicht aktiv steuern. die Berechtigung des Benutzers ist nicht erforderlich.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) . Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.

## <a name="remarks"></a>Bemerkungen

Vollständige Kontrolle über eine Sitzung bedeutet, dass der Remote Benutzer die Sitzung des Benutzers mit Tastatur und Maus aktiv steuern kann.

Wenn ein Benutzer versucht, eine Remote Steuerungs Verbindung herzustellen, zeigt das System eine Meldung an den Remote Client an und fordert die Berechtigung an, die Remote Sitzung entweder in der Remote Sitzung anzuzeigen oder aktiv zu nehmen.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32-"t- \_ remotecontrolsetting"**](win32-tsremotecontrolsetting.md)
</dt> </dl>

 

