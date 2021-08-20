---
title: ModifyAuditPermissions-Methode der Win32_TSAccount-Klasse
description: Bereitet das Festlegen eines präziseren Satzes von Überwachungsberechtigungen für das angegebene Konto vor.
ms.assetid: 7df44a37-257d-49c6-8193-f1e1c5ebbb57
ms.tgt_platform: multiple
keywords:
- ModifyAuditPermissions-Methode Remotedesktopdienste
- ModifyAuditPermissions-Methode Remotedesktopdienste , Win32_TSAccount-Klasse
- Win32_TSAccount Klasse Remotedesktopdienste , ModifyAuditPermissions-Methode
topic_type:
- apiref
api_name:
- Win32_TSAccount.ModifyAuditPermissions
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 460cbc3ffc16e2b08401c754b3eb7d0def82daf69163a437fc94da331940e402
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117940280"
---
# <a name="modifyauditpermissions-method-of-the-win32_tsaccount-class"></a>ModifyAuditPermissions-Methode der Win32 \_ TSAccount-Klasse

Die **ModifyAuditPermissions-Methode** bereitet vor, einen präziseren Satz von Überwachungsberechtigungen für das angegebene Konto festzulegen.

## <a name="syntax"></a>Syntax


```mof
uint32 ModifyAuditPermissions(
  [in] uint32  PermissionMask,
  [in] boolean Success
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PermissionMask* \[ In\]
</dt> <dd>

Der Satz von [Remotedesktop-Sitzungshost Berechtigungen,](terminal-services-permissions.md) die dem angegebenen Konto zugeordnet werden sollen. Der Wert dieses Parameters ist eine Bitmap, und alle der folgenden Werte können ausgewählt werden.

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

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION \_ VIRTUELLE \| \_ STANDARDRECHTE \_ ERFORDERLICH** (3)


</dt> <dd>

Berechtigung zum Verwenden virtueller Kanäle. Virtuelle Kanäle ermöglichen den Zugriff von einem Serverprogramm auf Clientgeräte.

</dd> <dt>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION \_ SHADOW** (4)


</dt> <dd>

Berechtigung zum Shadowing oder remoten Steuern der Sitzung eines anderen Benutzers.

</dd> <dt>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION \_ ANMELDUNG** (5)


</dt> <dd>

Berechtigung zum Anmelden bei einer Sitzung auf dem Server.

</dd> <dt>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION \_ LOGOFF** (2)


</dt> <dd>

Berechtigung zum Abmelden eines Benutzers aus einer Sitzung.

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

*Erfolgreich* \[ In\]
</dt> <dd>

Gibt an, ob der durch den Wert des *PermissionMask-Parameters* angegebene Berechtigungssatz zulässig oder verweigert wird.

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

Gibt bei Erfolg 0 zurück, andernfalls einen WMI-Fehlercode. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSAccount**](win32-tsaccount.md)
</dt> </dl>

 

