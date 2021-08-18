---
title: RemoteControl-Methode der Win32_TSRemoteControlSetting Klasse
description: Die RemoteControl-Methode legt die LevelOfControl-Eigenschaft fest.
ms.assetid: 341f4f8d-17be-4482-834a-b771e041cfec
ms.tgt_platform: multiple
keywords:
- RemoteControl-Remotedesktopdienste
- RemoteControl-Remotedesktopdienste , Win32_TSRemoteControlSetting-Klasse
- Win32_TSRemoteControlSetting klasse Remotedesktopdienste , RemoteControl-Methode
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
ms.openlocfilehash: 73de3f92171f688a9c0dc611552a061a3f2de7bf573fa41dab8606395eafe228
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769420"
---
# <a name="remotecontrol-method-of-the-win32_tsremotecontrolsetting-class"></a>RemoteControl-Methode der Win32 \_ TSRemoteControlSetting-Klasse

Die **RemoteControl-Methode** legt die **LevelOfControl-Eigenschaft** fest.

## <a name="syntax"></a>Syntax


```mof
uint32 RemoteControl(
  [in] uint32 LevelOfControl
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*LevelOfControl* \[ In\]
</dt> <dd>

Neuer Wert für die **LevelOfControl-Eigenschaft,** der angibt, ob die Sitzung nur vom Remotebenutzer angezeigt oder per Tastatur und Maus angezeigt und gesteuert wird. Weitere Informationen finden Sie im Abschnitt "Hinweise". Die folgenden Werte werden unterstützt.

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Deaktivieren** (0)


</dt> <dd>

Die Remotesteuerung ist deaktiviert.

</dd> <dt>

<span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>

<span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**EnableInputNotify** (1)


</dt> <dd>

Der Benutzer der Remotesteuerung hat mit der Berechtigung des Benutzers die vollständige Kontrolle über die Sitzung des Benutzers.

</dd> <dt>

<span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>

<span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**EnableInputNoNotify** (2)


</dt> <dd>

Der Benutzer der Remotesteuerung hat die vollständige Kontrolle über die Sitzung des Benutzers. Die Berechtigung des Benutzers ist nicht erforderlich.

</dd> <dt>

<span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>

<span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**EnableNoInputNotify** (3)


</dt> <dd>

Der Benutzer der Remotesteuerung kann die Sitzung mit der Berechtigung des Benutzers remote anzeigen. der Remotebenutzer kann die Sitzung nicht aktiv steuern.

</dd> <dt>

<span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>

<span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**EnableNoInputNoNotify** (4)


</dt> <dd>

Der Benutzer der Remotesteuerung kann die Sitzung remote anzeigen, aber nicht aktiv steuern. Die Berechtigung des Benutzers ist nicht erforderlich.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Remotedesktopdienste finden Sie unter [Fehlercodes](terminal-services-wmi-provider-error-codes.md) für WMI-Anbieter. Die -Methode gibt einen Fehler zurück, wenn sich die Einstellung unter der Gruppenrichtliniensteuerung befindet.

## <a name="remarks"></a>Hinweise

Die vollständige Kontrolle über eine Sitzung bedeutet, dass der Remotebenutzer die Sitzung des Benutzers aktiv mit einer Tastatur und Maus steuern kann.

Wenn ein Benutzer versucht, eine Remotesteuerungsverbindung herzustellen, zeigt das System eine Nachricht an den Remoteclient an und fordert die Berechtigung an, die Remotesitzung entweder anzeigen oder aktiv daran teilnehmen zu können.

Managed Object Format (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSRemoteControlSetting**](win32-tsremotecontrolsetting.md)
</dt> </dl>

 

