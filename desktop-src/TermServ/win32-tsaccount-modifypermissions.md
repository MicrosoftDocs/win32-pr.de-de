---
title: ModifyPermissions-Methode der Win32_TSAccount Klasse
description: Legt eine Berechtigung für das angegebene Konto fest.
ms.assetid: cef36f7f-d327-4bb6-9bff-282036c1a5d5
ms.tgt_platform: multiple
keywords:
- ModifyPermissions-Remotedesktopdienste
- ModifyPermissions-Methode Remotedesktopdienste , Win32_TSAccount Klasse
- Win32_TSAccount klasse Remotedesktopdienste , ModifyPermissions-Methode
topic_type:
- apiref
api_name:
- Win32_TSAccount.ModifyPermissions
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6265290fa3604c426609f51d0518f1f6762ea02718757d86ff9ed69b10bd018
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119421670"
---
# <a name="modifypermissions-method-of-the-win32_tsaccount-class"></a>ModifyPermissions-Methode der Win32 \_ TSAccount-Klasse

Legt eine Berechtigung für das angegebene Konto fest.

## <a name="syntax"></a>Syntax


```mof
uint32 ModifyPermissions(
  [in] uint32  PermissionMask,
  [in] boolean Allow
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PermissionMask* \[ In\]
</dt> <dd>

Die [Remotedesktop-Sitzungshost Berechtigung, die](terminal-services-permissions.md) festgelegt werden soll.

Mögliche Werte sind:

<dt>

<span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>

<span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>**WINSTATION \_ QUERY** (0)


</dt> <dd>

Berechtigung zum Abfragen von Informationen zu einer Sitzung.

</dd> <dt>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION \_ SET** (1)


</dt> <dd>

Berechtigung zum Ändern von Verbindungsparametern.

</dd> <dt>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION \_ RESET** (6)


</dt> <dd>

Berechtigung zum Zurücksetzen oder Beenden einer Sitzung oder Verbindung.

</dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION \_ VIRTUELLE \| \_ \_ STANDARDRECHTE ERFORDERLICH** (3)


</dt> <dd>

Berechtigung zum Verwenden virtueller Kanäle. Virtuelle Kanäle ermöglichen den Zugriff von einem Serverprogramm auf Clientgeräte.

</dd> <dt>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION \_ SHADOW** (4)


</dt> <dd>

Berechtigung zum Überschatten oder Remotesteuerung der Sitzung eines anderen Benutzers.

</dd> <dt>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION \_ LOGON** (5)


</dt> <dd>

Berechtigung zum Anmelden bei einer Sitzung auf dem Server.

</dd> <dt>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION \_ LOGOFF** (2)


</dt> <dd>

Berechtigung zum Abmelden eines Benutzers von einer Sitzung.

</dd> <dt>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION \_ MSG** (7)


</dt> <dd>

Berechtigung zum Senden einer Nachricht an die Sitzung eines anderen Benutzers.

</dd> <dt>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION \_ CONNECT** (8)


</dt> <dd>

Berechtigung zum Herstellen einer Verbindung mit einer anderen Sitzung.

</dd> <dt>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION \_ DISCONNECT** (9)


</dt> <dd>

Berechtigung zum Trennen einer Sitzung.

</dd> </dl> </dd> <dt>

*Zulassen* \[ In\]
</dt> <dd>

Gibt an, ob die Berechtigung im *PermissionMask-Parameter* zulässig oder verweigert wird.

Mögliche Werte sind:

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Der angegebene Berechtigungssatz ist zulässig.

</dd> <dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Der angegebene Berechtigungssatz wird verweigert.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Remotedesktopdienste finden Sie unter [Fehlercodes](terminal-services-wmi-provider-error-codes.md) für WMI-Anbieter.

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**Win32 \_ TSAccount**](win32-tsaccount.md)
</dt> </dl>

 

