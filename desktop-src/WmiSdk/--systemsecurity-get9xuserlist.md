---
description: Ruft die Remotezugriffsrechte für eine Liste einzelner Benutzer auf Computern ab, auf denen veraltete Versionen von Windows ausgeführt werden, wobei die Zugriffssteuerung über Windows Sicherheitsbeschreibungen nicht verfügbar ist.
ms.assetid: 79a596db-5f85-4664-8989-f309286eca0d
ms.tgt_platform: multiple
title: __SystemSecurity::Get9XUserList-Methode
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
ms.openlocfilehash: cfb6f0b9bb503e212e00d5343b55d6a9e20fbc8acfb0a5b534e8848cc6d3d931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110103"
---
# <a name="__systemsecurityget9xuserlist-method"></a>\_\_SystemSecurity::Get9XUserList-Methode

Die [**\_ \_ SystemSecurity::Set9XUserList-Methode**](--systemsecurity-set9xuserlist.md) ruft die Remotezugriffsrechte für eine Liste einzelner Benutzer auf Computern ab, auf denen veraltete Versionen von Windows ausgeführt werden, wobei die Zugriffssteuerung über Windows Sicherheitsbeschreibungen nicht verfügbar ist.

Diese Funktion ähnelt dem Sicherheitsdeskriptor, ist jedoch eingeschränkter. Gruppen werden nicht unterstützt, und es gibt keine Kontrolle über den lokalen Zugriff, da der lokale Benutzer immer über Vollzugriff verfügt. Zugriffssteuerungseinträge (ACE) werden sowohl verweigern als auch zulassen zugelassen. Aus diesem Grund ist die ACE-Reihenfolge in der DACL (Discretionary Access Control List) wichtig. Weitere Informationen finden Sie unter [Reihenfolge der ACEs in einer DACL.](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl)

## <a name="syntax"></a>Syntax


```C++
HRESULT Get9XUserList(
  [out] __NTLMUser9X ul[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ul* \[ out\]
</dt> <dd>

Array von Benutzern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **HRESULT** zurück, das den Status des Methodenaufrufs angibt. In der folgenden Liste sind die Rückgabewerte aufgeführt, die für **Get9XUserList** von Bedeutung sind. Für Skripts und Visual Basic Anwendungen kann [outParameters.ReturnValue](parsing-outparameters-objects.md)als Ergebnis verwendet werden. Weitere Informationen finden Sie unter [Erstellen von InParameters-Objekten und Analysieren von OutParameters-Objekten.](constructing-inparameters-objects-and-parsing-outparameters-objects.md)

<dl> <dt>

**WBEM \_ \_ E-METHODE \_ DEAKTIVIERT**
</dt> <dd>

Diese Methode wird für unterstützte Versionen von Windows nicht unterstützt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WMI-Systemklassen](wmi-system-classes.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> <dt>

[**\_\_SystemSecurity::GetSD**](--systemsecurity-getsd.md)
</dt> <dt>

[**\_\_SystemSecurity::SetSD**](--systemsecurity-setsd.md)
</dt> <dt>

[**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Sichern von WMI-Namespaces](securing-wmi-namespaces.md)
</dt> <dt>

[WMI-Sicherheitskonstanten](wmi-security-constants.md)
</dt> </dl>

 

