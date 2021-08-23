---
description: Ordnet dem in das Laufwerk eingefügten Medium ein Speicherlaufwerk zu.
ms.assetid: C0B2D604-0B55-4EA0-A46E-2450D89A5B22
title: Msvm_MediaPresent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MediaPresent
- Msvm_MediaPresent.Antecedent
- Msvm_MediaPresent.Dependent
- Msvm_MediaPresent.FixedMedia
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7044cfed5a4affd628ea8008c89b4aabeee3499d65f03abf815e68d73d06a773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521720"
---
# <a name="msvm_mediapresent-class"></a>Msvm \_ MediaPresent-Klasse

Ordnet dem in das Laufwerk eingefügten Medium ein Speicherlaufwerk zu. Diese Zuordnung wird für alle Speicherlaufwerkobjekte verwendet.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MediaPresent : CIM_MediaPresent
{
  CIM_MediaAccessDevice REF Antecedent;
  CIM_StorageExtent     REF Dependent;
  boolean                   FixedMedia;
};
```

## <a name="members"></a>Member

Die **Msvm \_ MediaPresent-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ MediaPresent-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Verweis auf das Medienzugriffsgerät. Diese Eigenschaft wird von [**CIM \_ MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent)geerbt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Verweis auf den Speicherbereich, auf den mit dem Medienzugriffsgerät zugegriffen wird. Diese Eigenschaft wird von [**CIM \_ MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent)geerbt.

</dd> <dt>

**FixedMedia**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Speicherumfang, auf den zugegriffen wird, behoben ist und nicht eingefügt werden kann. Der Wert **ist** true für Festplatten, **andernfalls FALSE.** Diese Eigenschaft wird von [**CIM \_ MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent)geerbt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **Msvm \_ MediaPresent-Klasse** kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ MediaPresent**](cim-mediapresent.md)
</dt> <dt>

[**CIM \_ MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent)
</dt> <dt>

[Storage Klassen](storage-classes.md)
</dt> </dl>

 

