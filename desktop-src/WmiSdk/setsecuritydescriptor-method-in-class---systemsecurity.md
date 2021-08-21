---
description: Schreibt eine aktualisierte Version der Sicherheitsbeschreibung, die den Zugriff auf den WMI-Namespace steuert, mit dem Sie verbunden sind. Der Sicherheitsdeskriptor wird durch eine Instanz von \_ \_ SecurityDescriptor dargestellt.
ms.assetid: e92430fd-61b1-4986-88dc-b85f502f62e6
ms.tgt_platform: multiple
title: SetSecurityDescriptor-Methode der __SystemSecurity-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.SetSecurityDescriptor
api_type:
- COM
api_location:
- All
ms.openlocfilehash: d44322820514fc676c1b3ad304375f5f3ce8966a73217c6505f24659914f7853
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315627"
---
# <a name="setsecuritydescriptor-method-of-the-__systemsecurity-class"></a>SetSecurityDescriptor-Methode der \_ \_ SystemSecurity-Klasse

Die [**SetSecurityDescriptor-Methode**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-printer) schreibt eine aktualisierte Version der Sicherheitsbeschreibung, die den Zugriff auf den WMI-Namespace steuert, mit dem Sie verbunden sind. Der Sicherheitsdeskriptor wird durch eine Instanz von [**\_ \_ SecurityDescriptor**](--securitydescriptor.md)dargestellt. Weitere Informationen finden Sie unter [Ändern der Zugriffssicherheit für sicherungsfähige Objekte.](changing-access-security-on-securable-objects.md)

## <a name="syntax"></a>Syntax


```mof
uint32 SetSecurityDescriptor(
  [in] __SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Deskriptor* \[ In\]
</dt> <dd>

Der dem WMI-Namespace zugeordnete Sicherheitsdeskriptor.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben. Weitere Informationen finden Sie unter [WMI-Rückgabecodes](wmi-return-codes.md) oder [**WbemErrorEnum.**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)

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

Der Benutzer verfügt nicht über ausreichende Berechtigungen zum Ausführen der -Methode.

</dd> <dt>

**21**
</dt> <dd>

Ein im Methodenaufruf angegebener Parameter ist ungültig.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die [**Win32 \_ SecurityDescriptor-Instanz**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) stellt einen [**SECURITY \_ DESCRIPTOR \_ CONTROL-Datentyp**](/windows/desktop/SecAuthZ/security-descriptor-control) dar und enthält eine [*DACL (Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) und eine [*System Access Control List*](/windows/desktop/SecGloss/a-gly) (SACL). Weitere Informationen finden Sie unter [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).

Wenn **seSecurityPrivilege** beim Abrufen eines Sicherheitsdeskriptors nicht gewährt oder aktiviert wird, wird nur die DACL in der zurückgegebenen Sicherheitsbeschreibung zurückgegeben. Weitere Informationen finden Sie unter [**Berechtigungskonstanten**](privilege-constants.md) und [Ausführen privilegierter Vorgänge.](executing-privileged-operations.md)

Sie können sowohl die DACL als auch die SACL in der [**Win32 \_ SecurityDescriptor-Instanz**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) aktualisieren, wenn Sie diese Methode aufrufen. Sie können jedoch auch nur die DACL oder nur die SACL aktualisieren.

Die folgenden Werte in [**SECURITY \_ DESCRIPTOR \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) bestimmen, ob die DACL, die SACL oder beide aktualisiert werden.

-   **\_SE DACL \_ PRESENT**

    Gibt an, dass die DACL aktualisiert werden soll. Wenn dies nicht festgelegt ist, behält WMI den ursprünglichen Wert der DACL bei.

-   **\_SE SACL \_ PRESENT**

    Gibt an, dass die SACL aktualisiert werden soll. Wenn dies nicht festgelegt ist, behält WMI den ursprünglichen Wert der SACL bei. Zum Aktualisieren der SACL muss für das Konto die **SeSecurityPrivilege-Berechtigung** aktiviert sein. Für die Skripterstellung lautet der Berechtigungsname **SeSecurityPrivilege.** Weitere Informationen finden Sie unter [**Berechtigungskonstanten.**](privilege-constants.md)

Wenn die Eigenschaften des Gruppentreuhänders und des Besitzertreuhänders nicht **NULL** sind, werden sie aktualisiert. Andernfalls behält WMI die ursprünglichen Werte bei. Weitere Informationen finden Sie unter [WMI-Sicherheitsdeskriptorobjekte.](wmi-security-descriptor-objects.md)

Wenn eine neue SACL in einem Aufruf dieser Methode **NULL** ist, bleibt die Sicherheitsbeschreibungs-SACL für das sicherungsfähige Zielobjekt unverändert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> <dt>

[Festlegen von Namepace-Sicherheitsbeschreibungen](setting-namespace-security-descriptors.md)
</dt> </dl>

 

