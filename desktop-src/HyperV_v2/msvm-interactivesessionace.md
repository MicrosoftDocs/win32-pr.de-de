---
description: Stellt einen Zugriffssteuerungseintrag (ACE) dar, der den Zugriff auf die interaktive Sitzung eines virtuellen Computers bestimmt.
ms.assetid: dfec83d6-8033-47b5-aa6f-fc7447a29f43
title: Msvm_InteractiveSessionACE-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InteractiveSessionACE
- Msvm_InteractiveSessionACE.Trustee
- Msvm_InteractiveSessionACE.AccessType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ed7dd4c4a3742f43a3de8e919ae2200e76cacc03ba1f7da066f48bac018f0a17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148383"
---
# <a name="msvm_interactivesessionace-class"></a>Msvm \_ InteractiveSessionACE-Klasse

Stellt einen *Zugriffssteuerungseintrag (ACE)* dar, der den Zugriff auf die interaktive Sitzung eines virtuellen Computers bestimmt.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_InteractiveSessionACE
{
  string Trustee;
  uint16 AccessType;
};
```

## <a name="members"></a>Member

Die **Msvm \_ InteractiveSessionACE-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ InteractiveSessionACE-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AccessType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der ACE dem Vertrauensnehmer Zugriff gewährt oder verweigert.

<dt>

<span id="Access_Allowed"></span><span id="access_allowed"></span><span id="ACCESS_ALLOWED"></span>

**Zugriff zulässig** (0)


</dt> <dd></dd> <dt>

<span id="Access_Denied"></span><span id="access_denied"></span><span id="ACCESS_DENIED"></span>

**Zugriff verweigert** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**Treuhänder**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Identifiziert den Sicherheitsprinzipal, auf den der ACE Zugriff gewährt oder verweigert. Gültige Formate für diese Eigenschaft sind das Windows SAM-kompatiblen Benutzernamenformat und das Windows SID-Zeichenfolgenformat.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**GetInteractiveSessionACL**](getinteractivesessionacl-msvm-terminalservice.md)
</dt> </dl>

 

 




