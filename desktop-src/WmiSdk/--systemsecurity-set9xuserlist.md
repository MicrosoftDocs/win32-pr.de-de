---
description: Legt die Remotezugriffsrechte für eine Liste einzelner Benutzer auf Computern fest, auf denen veraltete Versionen von Windows ausgeführt werden, wobei die Zugriffssteuerung über Windows Sicherheitsbeschreibungen nicht verfügbar ist.
ms.assetid: f6da65d3-86dd-4fc8-b4c0-f7ddc8536d4e
ms.tgt_platform: multiple
title: __SystemSecurity::Set9XUserList-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.Set9XUserList
api_type:
- COM
api_location:
- all
ms.openlocfilehash: d1185fa91d9d12e240f592d458b975b650947cf5b8cd1b289a7e016b455556a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118109961"
---
# <a name="__systemsecurityset9xuserlist-method"></a>\_\_SystemSecurity::Set9XUserList-Methode

Die **\_ \_ SystemSecurity::Set9XUserList-Methode** legt die Remotezugriffsrechte für eine Liste einzelner Benutzer auf Computern fest, auf denen veraltete Versionen von Windows ausgeführt werden, auf denen die Zugriffssteuerung über Windows-Sicherheitsdeskriptoren nicht verfügbar ist.

Die Liste wird als Array eingebetteter Objekte angegeben, wobei jedes Objekt eine Instanz der [**\_ \_ NTLMUser9X-Klasse**](--ntlmuser9x.md) ist. Diese Funktion ähnelt der Sicherheitsbeschreibung, ist jedoch eingeschränkter. Gruppen werden nicht unterstützt, und es gibt keine Kontrolle über den lokalen Zugriff, da der lokale Benutzer immer Vollzugriff hat. Zugriffssteuerungseinträge (ACE) werden sowohl verweigert als auch zugelassen. Aus diesem Grund ist die ACE-Reihenfolge in der DACL (Discretionary Access Control List) wichtig. Weitere Informationen finden Sie unter [Reihenfolge der ACEs in einer DACL.](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl)

## <a name="syntax"></a>Syntax


```C++
HRESULT Set9XUserList(
  [in] __NTLMUser9X ul[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ul* \[ In\]
</dt> <dd>

Array von Benutzern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **HRESULT zurück,** das den Status des Methodenaufrufs angibt. In der folgenden Liste sind die Rückgabewerte aufgeführt, die für **Set9XUserList von Bedeutung sind.** Für Skripts und Visual Basic können Sie das Ergebnis aus [OutParameters.ReturnValue erhalten.](parsing-outparameters-objects.md) Weitere Informationen finden Sie unter [Constructing InParameters Objects (Erstellen von InParameters-Objekten) und Parsing OutParameters Objects (Analyse von OutParameters-Objekten).](constructing-inparameters-objects-and-parsing-outparameters-objects.md)

<dl> <dt>

**WBEM \_ \_ E-METHODE \_ DEAKTIVIERT**
</dt> <dd>

Diese Methode wird nicht unterstützt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Weitere Informationen

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

[WMI-Sicherheitskonst constants](wmi-security-constants.md)
</dt> </dl>

 

