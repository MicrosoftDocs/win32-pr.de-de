---
description: Ruft die Remote Zugriffsrechte für eine Liste einzelner Benutzer auf Computern ab, auf denen veraltete Versionen von Windows ausgeführt werden, bei denen die Zugriffs Steuerung durch Windows-Sicherheits Deskriptoren nicht verfügbar ist.
ms.assetid: 79a596db-5f85-4664-8989-f309286eca0d
ms.tgt_platform: multiple
title: '__SystemSecurity:: Get9XUserList-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.Get9XUserList
api_type:
- COM
api_location:
- all
ms.openlocfilehash: 521f2fe489089d486480c138293ebea39ca6f105
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350804"
---
# <a name="__systemsecurityget9xuserlist-method"></a>\_\_SystemSecurity:: Get9XUserList-Methode

Die [**\_ \_ SystemSecurity:: Set9XUserList**](--systemsecurity-set9xuserlist.md) -Methode ruft die Remote Zugriffsrechte für eine Liste einzelner Benutzer auf Computern ab, auf denen veraltete Versionen von Windows ausgeführt werden, wobei die Zugriffs Steuerung durch Windows-Sicherheits Deskriptoren nicht verfügbar ist.

Diese Funktion ähnelt der Sicherheits Beschreibung, ist aber eingeschränkter. Gruppen werden nicht unterstützt, und es gibt keine Kontrolle über den lokalen Zugriff, da der lokale Benutzer immer über Vollzugriff verfügt. Sowohl Deny-als auch Zulassungs Zugriffs Steuerungs Einträge (ACE) sind zulässig, und aus diesem Grund ist die ACE-Reihenfolge in der freigegebenen Zugriffs Steuerungs Liste (DACL) wichtig. Weitere Informationen finden Sie unter [Reihenfolge von ACEs in einer DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

## <a name="syntax"></a>Syntax


```C++
HRESULT Get9XUserList(
  [out] __NTLMUser9X ul[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*UL* \[ vorgenommen\]
</dt> <dd>

Array von Benutzern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **HRESULT** zurück, das den Status des Methoden Aufrufes angibt. In der folgenden Liste sind die Rückgabewerte aufgelistet, die für **Get9XUserList** von Bedeutung sind. Für Skript-und Visual Basic Anwendungen kann das Ergebnis [OutParameters. returnValue](parsing-outparameters-objects.md)sein. Weitere Informationen finden Sie unter [Erstellen von inparameter-Objekten und Überprüfen von outparameter-Objekten](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

<dl> <dt>

**WBEM \_ E- \_ Methode \_ deaktiviert**
</dt> <dd>

Diese Methode wird auf unterstützten Versionen von Windows nicht unterstützt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> <dt>

[**\_\_SystemSecurity:: getd**](--systemsecurity-getsd.md)
</dt> <dt>

[**\_\_SystemSecurity::-ID**](--systemsecurity-setsd.md)
</dt> <dt>

[**Win32- \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**Win32- \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Sichern von WMI-Namespaces](securing-wmi-namespaces.md)
</dt> <dt>

[WMI-Sicherheits Konstanten](wmi-security-constants.md)
</dt> </dl>

 

