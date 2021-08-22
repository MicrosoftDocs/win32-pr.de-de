---
description: Ruft den Sicherheitsdeskriptor ab, der den Zugriff auf den WMI-Namespace steuert, mit dem Sie verbunden sind. Der Sicherheitsdeskriptor wird als Instanz von \_ \_ SecurityDescriptor zurückgegeben.
ms.assetid: b031af45-9237-434d-91db-69222306c615
ms.tgt_platform: multiple
title: GetSecurityDescriptor-Methode der __SystemSecurity Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetSecurityDescriptor
api_type:
- COM
api_location:
- All
ms.openlocfilehash: 77053174878db77409c525510acb54740ac8ad5c5c0505af5bf6ff8421cdf737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050858"
---
# <a name="getsecuritydescriptor-method-of-the-__systemsecurity-class"></a>GetSecurityDescriptor-Methode der \_ \_ SystemSecurity-Klasse

Die **GetSecurityDescriptor-Methode** ruft den Sicherheitsdeskriptor ab, der den Zugriff auf den WMI-Namespace steuert, mit dem Sie verbunden sind. Der Sicherheitsdeskriptor wird als Instanz von [**\_ \_ SecurityDescriptor zurückgegeben.**](--securitydescriptor.md) Weitere Informationen finden Sie unter Changing Access Security on Securable Objects (Ändern [der Zugriffssicherheit für sicherungsfähige Objekte).](changing-access-security-on-securable-objects.md)

## <a name="syntax"></a>Syntax


```mof
uint32 GetSecurityDescriptor(
  [out] __SystemSecurity Descriptor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Deskriptor* \[ out\]
</dt> <dd>

Der dem WMI-Namespace zugeordnete Sicherheitsdeskriptor.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben. Weitere Informationen finden Sie unter [WMI-Rückgabecodes](wmi-return-codes.md) oder [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).

<dl> <dt>

**0**
</dt> <dd>

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

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die [**Win32 \_ SecurityDescriptor-Instanz**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) stellt einen [**SECURITY \_ DESCRIPTOR \_ CONTROL-Datentyp**](/windows/desktop/SecAuthZ/security-descriptor-control) dar und enthält eine DACL (Discretionary [*Access Control List)*](/windows/desktop/SecGloss/d-gly) und eine Systemzugriffssteuerungsliste (SACL). [](/windows/desktop/SecGloss/s-gly) Weitere Informationen finden Sie unter [Access Control Listen.](/windows/desktop/SecAuthZ/access-control-lists)

Wenn **seSecurityPrivilege** beim Abrufen eines Sicherheitsdeskriptors nicht gewährt oder aktiviert wird, wird nur die DACL in der zurückgegebenen Sicherheitsbeschreibung zurückgegeben. Weitere Informationen finden Sie unter [**Privilege Constants**](privilege-constants.md) und [Executing Privileged Operations](executing-privileged-operations.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> <dt>

[Festlegen von Namepace-Sicherheitsdeskriptoren](setting-namespace-security-descriptors.md)
</dt> </dl>

 

