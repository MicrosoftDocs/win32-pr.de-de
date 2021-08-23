---
description: Ruft den Sicherheitsdeskriptor ab, der steuert, wer eine DCOM-Anwendung starten darf.
ms.assetid: ba02807f-aa2a-4b1c-9692-2803d93cd2ee
ms.tgt_platform: multiple
title: GetLaunchSecurityDescriptor-Methode der Win32_DCOMApplicationSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting.GetLaunchSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b76a37db5b1edbc230c4cc4aed712ef4eee9dd4221cc4cb85fb8f205db69d35
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878950"
---
# <a name="getlaunchsecuritydescriptor-method-of-the-win32_dcomapplicationsetting-class"></a>GetLaunchSecurityDescriptor-Methode der Win32 \_ DCOMApplicationSetting-Klasse

Die WMI-Methode **GetLaunchSecurityDescriptor** ruft den Sicherheitsdeskriptor ab, der steuert, wer eine DCOM-Anwendung starten darf. Der Sicherheitsdeskriptor ist eine Instanz der [**Win32 \_ SecurityDescriptor-Klasse.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) Das Konto, unter dem das Skript oder die Anwendung ausgeführt wird, das diese Methode aufruft, muss über die Berechtigungen **SeSecurityPrivilege** und **SeRestorePrivilege** verfügen. Weitere Informationen finden Sie unter Changing Access Security on Securable Objects (Ändern [der Zugriffssicherheit für sicherungsfähige Objekte).](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)

## <a name="syntax"></a>Syntax


```mof
uint32 GetLaunchSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Deskriptor* \[ out\]
</dt> <dd>

Der Sicherheitsdeskriptor, mit dem festgelegt wird, wer die DCOM-Anwendung starten kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben. Weitere Informationen finden Sie unter [WMI-Rückgabecodes](/windows/desktop/WmiSdk/wmi-return-codes) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

<dl> <dt>

**Erfolgreich**
</dt> <dd>

0

Erfolgreicher Abschluss.

</dd> <dt>

**2**
</dt> <dd>

Der Benutzer hat keinen Zugriff auf die angeforderten Informationen.

</dd> <dt>

**8**
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**9**
</dt> <dd>

Der Benutzer verfügt nicht über die erforderlichen Berechtigungen zum Ausführen der -Methode.

</dd> <dt>

**21**
</dt> <dd>

Ein im Methodenaufruf angegebener Parameter ist ungültig.

</dd> <dt>

**Andere**
</dt> <dd>

1 4294967295

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die [**Win32 \_ SecurityDescriptor-Instanz**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) stellt einen [**SECURITY \_ DESCRIPTOR \_ CONTROL-Datentyp**](/windows/desktop/SecAuthZ/security-descriptor-control) dar und enthält eine DACL (Discretionary [*Access Control List)*](/windows/desktop/SecGloss/d-gly) und eine Systemzugriffssteuerungsliste (SACL). [](/windows/desktop/SecGloss/s-gly) Weitere Informationen finden Sie unter [Access Control Listen.](/windows/desktop/SecAuthZ/access-control-lists)

Wenn **seSecurityPrivilege** beim Abrufen eines Sicherheitsdeskriptors nicht gewährt oder aktiviert wird, wird nur die DACL in der zurückgegebenen Sicherheitsbeschreibung zurückgegeben. Weitere Informationen finden Sie unter [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) und [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ DCOMApplicationSetting**](win32-dcomapplicationsetting.md)
</dt> <dt>

[**Berechtigungskonst constants**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[WMI-Sicherheitsdeskriptorobjekte](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Ändern der Zugriffssicherheit für sicherungsfähige Objekte](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

