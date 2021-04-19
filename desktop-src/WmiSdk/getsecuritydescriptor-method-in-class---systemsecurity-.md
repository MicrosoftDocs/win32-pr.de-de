---
description: Ruft die Sicherheits Beschreibung ab, die den Zugriff auf den WMI-Namespace steuert, mit dem Sie verbunden sind. Die Sicherheits Beschreibung wird als Instanz von \_ \_ securityDescriptor zurückgegeben.
ms.assetid: b031af45-9237-434d-91db-69222306c615
ms.tgt_platform: multiple
title: Getsecuritydescriptor-Methode der __SystemSecurity-Klasse
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
ms.openlocfilehash: 7aece0a50678689141de9b9a38a014414578de3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363615"
---
# <a name="getsecuritydescriptor-method-of-the-__systemsecurity-class"></a>Getsecuritydescriptor-Methode der \_ \_ System Security-Klasse

Die **getsecuritydescriptor** -Methode ruft die Sicherheits Beschreibung ab, die den Zugriff auf den WMI-Namespace steuert, mit dem Sie verbunden sind. Die Sicherheits Beschreibung wird als Instanz von [**\_ \_ securityDescriptor**](--securitydescriptor.md)zurückgegeben. Weitere Informationen finden Sie unter [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md).

## <a name="syntax"></a>Syntax


```mof
uint32 GetSecurityDescriptor(
  [out] __SystemSecurity Descriptor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Deskriptor* \[ vorgenommen\]
</dt> <dd>

Die Sicherheits Beschreibung, die dem WMI-Namespace zugeordnet ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der Werte zurück, der in der folgenden Liste aufgeführt ist, oder einen anderen Wert, um einen Fehler anzugeben. Weitere Informationen finden Sie unter [WMI-Rückgabe Codes](wmi-return-codes.md) oder [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).

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

Der Benutzer verfügt nicht über die erforderlichen Berechtigungen, um die Methode auszuführen.

</dd> <dt>

**21**
</dt> <dd>

Ein im Methoden Aufrufwert angegebener Parameter ist ungültig.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die [**Win32- \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Instanz stellt einen Datentyp für die [**Sicherheits \_ \_ deskriptorsteuerung**](/windows/desktop/SecAuthZ/security-descriptor-control) dar und enthält eine freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) und eine [*System Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/s-gly) (SACL). Weitere Informationen finden Sie unter [Access Control Listen](/windows/desktop/SecAuthZ/access-control-lists).

Wenn **SeSecurityPrivilege** beim erhalten einer Sicherheits Beschreibung nicht gewährt oder aktiviert ist, wird nur die DACL in der zurückgegebenen Sicherheits Beschreibung zurückgegeben. Weitere Informationen finden Sie unter [**Berechtigungs Konstanten**](privilege-constants.md) und [Ausführen privilegierter Vorgänge](executing-privileged-operations.md).

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

[Festlegen von namepace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md)
</dt> </dl>

 

