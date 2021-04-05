---
title: Modifyauditberechtigungs-Methode der Win32_TSAccount-Klasse
description: Bereitet das Festlegen eines präziseteren Satzes von Überwachungs Berechtigungen für das angegebene Konto vor.
ms.assetid: 7df44a37-257d-49c6-8193-f1e1c5ebbb57
ms.tgt_platform: multiple
keywords:
- Modifyauditberechtigungs-Methode Remotedesktopdienste
- Modifyauditberechtigungs-Methode Remotedesktopdienste, Win32_TSAccount-Klasse
- Win32_TSAccount-Klasse Remotedesktopdienste, modifyauditberechtigungs-Methode
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
ms.openlocfilehash: f19337cc6110a15b206fc437fb6ec594ded60640
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859214"
---
# <a name="modifyauditpermissions-method-of-the-win32_tsaccount-class"></a>Modifyauditberechtigungs-Methode der Win32- \_ Klasse "zaccount"

Die **modifyauditberechtigungs** -Methode bereitet das Festlegen eines präziseteren Satzes von Überwachungs Berechtigungen für das angegebene Konto vor.

## <a name="syntax"></a>Syntax


```mof
uint32 ModifyAuditPermissions(
  [in] uint32  PermissionMask,
  [in] boolean Success
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PermissionMask* \[ in\]
</dt> <dd>

Der Satz von [Remotedesktop-Sitzungshost Berechtigungen](terminal-services-permissions.md) , die dem angegebenen Konto zugeordnet werden sollen. Der Wert dieses Parameters ist eine Bitmap, und jeder oder alle der folgenden Werte können ausgewählt werden.

<dt>

<span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>

<span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>**WinStation \_ Abfrage** (0)


</dt> <dd>

Berechtigung zum Abfragen von Informationen über eine Sitzung.

</dd> <dt>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WinStation \_ Set** (1)


</dt> <dd>

Berechtigung zum Ändern von Verbindungsparametern.

</dd> <dt>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WinStation \_ Zurücksetzen** (6)


</dt> <dd>

Berechtigung zum Zurücksetzen oder Beenden einer Sitzung oder einer Verbindung.

</dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WinStation \_ \| \_ \_ Erforderliche virtuelle Standard Rechte** (3)


</dt> <dd>

Berechtigung zum Verwenden von virtuellen Kanälen. Virtuelle Kanäle ermöglichen den Zugriff von einem Serverprogramm auf Client Geräte.

</dd> <dt>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WinStation \_ Schatten** (4)


</dt> <dd>

Berechtigung, um die Sitzung eines anderen Benutzers zu überschatten oder Remote zu steuern.

</dd> <dt>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WinStation \_ Anmelden** (5)


</dt> <dd>

Berechtigung zum Anmelden bei einer Sitzung auf dem Server.

</dd> <dt>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WinStation \_ Abmeldung (2** )


</dt> <dd>

Berechtigung zum Abmelden eines Benutzers von einer Sitzung.

</dd> <dt>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WinStation \_ Meldung (7** )


</dt> <dd>

Die Berechtigung zum Senden einer Nachricht an die Sitzung eines anderen Benutzers.

</dd> <dt>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WinStation \_ Verbinden** (8)


</dt> <dd>

Berechtigung zum Herstellen einer Verbindung mit einer anderen Sitzung.

</dd> <dt>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WinStation \_ Trennen** (9)


</dt> <dd>

Berechtigung zum Trennen einer Sitzung.

</dd> </dl> </dd> <dt>

*Erfolg* \[ in\]
</dt> <dd>

Gibt an, ob der Berechtigungs Satz, der durch den Wert des *PermissionMask* -Parameters angegeben wird, zugelassen oder verweigert wird.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Der angegebene Berechtigungs Satz ist zulässig.

</dd> <dt>

<span id="0"></span>

<span id="0"></span>**1,0**


</dt> <dd>

Der angegebene Berechtigungs Satz wird verweigert.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Bemerkungen

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

[**Win32- \_ Konto**](win32-tsaccount.md)
</dt> </dl>

 

