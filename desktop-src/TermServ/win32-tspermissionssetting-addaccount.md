---
title: Addaccount-Methode der Win32_TSPermissionsSetting-Klasse (faxcomex. h)
description: Die addaccount-Methode bereitet das Hinzufügen eines Kontos zum Terminal mit dem angegebenen Berechtigungs Satz vor. Sie können Benutzer, Gruppen oder Computer hinzufügen.
ms.assetid: da4d8f5b-7aa2-4b55-bf0f-b3e98b70a06b
ms.tgt_platform: multiple
keywords:
- Addaccount-Methode Remotedesktopdienste
- Addaccount-Methode Remotedesktopdienste, Win32_TSPermissionsSetting-Klasse
- Win32_TSPermissionsSetting-Klasse Remotedesktopdienste, addaccount-Methode
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting.AddAccount
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de89c34bd7aab20fbfbcbdedfd9d2f91bba866bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477697"
---
# <a name="addaccount-method-of-the-win32_tspermissionssetting-class"></a>Addaccount-Methode der Win32 \_ tspermissionssetting-Klasse

Die **addaccount** -Methode bereitet das Hinzufügen eines Kontos zum Terminal mit dem angegebenen Berechtigungs Satz vor. Sie können Benutzer, Gruppen oder Computer hinzufügen.

## <a name="syntax"></a>Syntax


```mof
uint32 AddAccount(
  [in] string AccountName,
  [in] uint32 PermissionPreSet
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Accountname* \[ in\]
</dt> <dd>

Der Name des Kontos, das dem Terminal hinzugefügt werden soll.

</dd> <dt>

*Permissionvoreinstellung* \[ in\]
</dt> <dd>

Der Satz von Berechtigungen, die dem angegebenen Konto zugeordnet werden sollen. Dieser Parameter kann einen oder alle der folgenden Werte aufweisen. Weitere Informationen finden Sie unter [Remotedesktopdienste Berechtigungen](terminal-services-permissions.md).

<dt>

<span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>

<span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>**WinStation \_ Gast \_ Zugriff** (0)


</dt> <dd>

Das Konto verfügt über die Berechtigung "Anmelden".

</dd> <dt>

<span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>

<span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>**WinStation \_ Benutzer \_ Zugriff** (1)


</dt> <dd>

Das Konto verfügt über die folgenden Berechtigungen: Anmeldung, Abfrage Informationen, Nachricht senden und verbinden.

</dd> <dt>

<span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>

<span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>**WinStation \_ Alle \_ Zugriffs** Rechte (2)


</dt> <dd>

Das Konto verfügt über alle Remotedesktopdienste Berechtigungen.

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
| Header<br/>                   | <dl> <dt>Faxcomex. h</dt> </dl>   |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ tspermissionssetting**](win32-tspermissionssetting.md)
</dt> </dl>

 

