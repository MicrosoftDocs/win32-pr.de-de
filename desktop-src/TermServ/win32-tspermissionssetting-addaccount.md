---
title: AddAccount-Methode der Win32_TSPermissionsSetting -Klasse (Faxcomex.h)
description: Die AddAccount-Methode bereitet das Hinzufügen eines Kontos zum Terminal mit dem angegebenen Berechtigungssatz vor. Sie können Benutzer, Gruppen oder Computer hinzufügen.
ms.assetid: da4d8f5b-7aa2-4b55-bf0f-b3e98b70a06b
ms.tgt_platform: multiple
keywords:
- AddAccount-Remotedesktopdienste
- AddAccount-Methode Remotedesktopdienste , Win32_TSPermissionsSetting-Klasse
- Win32_TSPermissionsSetting klasse Remotedesktopdienste , AddAccount-Methode
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
ms.openlocfilehash: c3bd1862dfde955d782527ca60fc0fb43ca31431ccb307574e875fe84a640655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118348555"
---
# <a name="addaccount-method-of-the-win32_tspermissionssetting-class"></a>AddAccount-Methode der Win32 \_ TSPermissionsSetting-Klasse

Die **AddAccount-Methode** bereitet das Hinzufügen eines Kontos zum Terminal mit dem angegebenen Berechtigungssatz vor. Sie können Benutzer, Gruppen oder Computer hinzufügen.

## <a name="syntax"></a>Syntax


```mof
uint32 AddAccount(
  [in] string AccountName,
  [in] uint32 PermissionPreSet
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AccountName* \[ In\]
</dt> <dd>

Der Name des Kontos, das dem Terminal hinzugefügt werden soll.

</dd> <dt>

*PermissionPreSet* \[ In\]
</dt> <dd>

Der Berechtigungssatz, der dem angegebenen Konto zugeordnet werden soll. Dieser Parameter kann einen oder alle der folgenden Werte sein. Weitere Informationen finden Sie unter [Remotedesktopdienste Berechtigungen.](terminal-services-permissions.md)

<dt>

<span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>

<span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>**WINSTATION \_ \_GASTZUGRIFF** (0)


</dt> <dd>

Das Konto verfügt über die Anmeldeberechtigung.

</dd> <dt>

<span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>

<span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>**WINSTATION \_ \_BENUTZERZUGRIFF** (1)


</dt> <dd>

Das Konto verfügt über die folgenden Berechtigungen: Anmeldung, Abfrageinformationen, Nachricht senden und Verbinden.

</dd> <dt>

<span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>

<span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>**WINSTATION \_ ALLE \_ ZUGRIFFE** (2)


</dt> <dd>

Das Konto verfügt über alle Remotedesktopdienste Berechtigungen.

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
| Header<br/>                   | <dl> <dt>Faxcomex.h</dt> </dl>   |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSPermissionsSetting**](win32-tspermissionssetting.md)
</dt> </dl>

 

