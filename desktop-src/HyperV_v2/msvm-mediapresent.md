---
description: Ordnet ein Speicher Laufwerk den Medien zu, die in das Laufwerk eingefügt werden.
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
ms.openlocfilehash: 57d46fb711ab8d4abcf27966e6ec92ed2287bc3e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869592"
---
# <a name="msvm_mediapresent-class"></a>MSVM \_ mediapresent-Klasse

Ordnet ein Speicher Laufwerk den Medien zu, die in das Laufwerk eingefügt werden. Diese Zuordnung wird für alle Speicher Laufwerk Objekte verwendet.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

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

Die **MSVM \_ mediapresent** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ mediapresent** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Verweis auf das Medien Zugriffsgerät. Diese Eigenschaft wird von [**CIM \_ mediapresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent)geerbt.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Verweis auf den Speicherblock, auf den mit dem Medien Zugriffsgerät zugegriffen wird. Diese Eigenschaft wird von [**CIM \_ mediapresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent)geerbt.

</dd> <dt>

**Fixedmedia**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Speicherplatz, auf den zugegriffen wird, fest ist und nicht aussteht. Der Wert ist für Festplatten **true** und andernfalls **false** . Diese Eigenschaft wird von [**CIM \_ mediapresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent)geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die **MSVM \_ mediapresent** -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ mediapresent**](cim-mediapresent.md)
</dt> <dt>

[**CIM- \_ mediapresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent)
</dt> <dt>

[Speicher Klassen](storage-classes.md)
</dt> </dl>

 

