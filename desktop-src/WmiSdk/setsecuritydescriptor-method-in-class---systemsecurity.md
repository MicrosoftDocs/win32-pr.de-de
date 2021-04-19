---
description: Schreibt eine aktualisierte Version der Sicherheits Beschreibung, die den Zugriff auf den WMI-Namespace steuert, mit dem Sie verbunden sind. Die Sicherheits Beschreibung wird durch eine Instanz von \_ \_ securityDescriptor dargestellt.
ms.assetid: e92430fd-61b1-4986-88dc-b85f502f62e6
ms.tgt_platform: multiple
title: SETSECURITYDESCRIPTOR-Methode der __SystemSecurity-Klasse
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
ms.openlocfilehash: fcdc192801b839451cee256f57090780818d2046
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364053"
---
# <a name="setsecuritydescriptor-method-of-the-__systemsecurity-class"></a>SETSECURITYDESCRIPTOR-Methode der \_ \_ System Security-Klasse

Die [**SETSECURITYDESCRIPTOR**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-printer) -Methode schreibt eine aktualisierte Version der Sicherheits Beschreibung, die den Zugriff auf den WMI-Namespace steuert, mit dem Sie verbunden sind. Die Sicherheits Beschreibung wird durch eine Instanz von [**\_ \_ securityDescriptor**](--securitydescriptor.md)dargestellt. Weitere Informationen finden Sie unter [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md).

## <a name="syntax"></a>Syntax


```mof
uint32 SetSecurityDescriptor(
  [in] __SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Deskriptor* \[ in\]
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

Die [**Win32- \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Instanz stellt einen Datentyp für die [**Sicherheits \_ \_ deskriptorsteuerung**](/windows/desktop/SecAuthZ/security-descriptor-control) dar und enthält eine freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) und eine [*System Access Control Liste*](/windows/desktop/SecGloss/a-gly) (SACL). Weitere Informationen finden Sie unter [Access Control Listen](/windows/desktop/SecAuthZ/access-control-lists).

Wenn **SeSecurityPrivilege** beim erhalten einer Sicherheits Beschreibung nicht gewährt oder aktiviert ist, wird nur die DACL in der zurückgegebenen Sicherheits Beschreibung zurückgegeben. Weitere Informationen finden Sie unter [**Berechtigungs Konstanten**](privilege-constants.md) und [Ausführen privilegierter Vorgänge](executing-privileged-operations.md).

Wenn Sie diese Methode aufrufen, können Sie sowohl die DACL als auch die SACL in der [**Win32- \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Instanz aktualisieren, aber Sie können auch nur die DACL oder nur die SACL aktualisieren.

Die folgenden Werte im [**Sicherheits \_ \_ deskriptorsteuerelement**](/windows/desktop/SecAuthZ/security-descriptor-control) bestimmen, ob die DACL oder die SACL oder beides aktualisiert wird.

-   **SE \_ DACL \_ vorhanden**

    Gibt an, dass die DACL aktualisiert werden soll. Wenn dies nicht festgelegt ist, behält WMI den ursprünglichen Wert der DACL bei.

-   **SE \_ SACL \_ vorhanden**

    Gibt an, dass die SACL aktualisiert werden soll. Wenn dies nicht festgelegt ist, behält WMI den ursprünglichen Wert der SACL bei. Zum Aktualisieren der SACL muss für das Konto die Berechtigung " **SeSecurityPrivilege** " aktiviert sein. Bei der Skripterstellung lautet der Berechtigungs Name " **SeSecurityPrivilege**". Weitere Informationen finden Sie unter [**Berechtigungs Konstanten**](privilege-constants.md).

Wenn die Eigenschaften des Gruppen Vertrauens nehmers und des Besitzer Treuhänders nicht **null** sind, werden Sie aktualisiert. Andernfalls behält WMI die ursprünglichen Werte bei. Weitere Informationen finden Sie unter [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md).

Wenn eine neue SACL in einem Aufruf dieser Methode **null** ist, bleibt die SACL der Sicherheits Beschreibung für das Sicherungs fähige Zielobjekt unverändert.

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

 

