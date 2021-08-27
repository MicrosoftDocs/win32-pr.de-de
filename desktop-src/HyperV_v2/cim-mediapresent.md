---
description: Stellt eine Beziehung dar, in der über ein Medienzugriffsgerät auf einen Speicherbereich zugegriffen werden muss.
ms.assetid: 436a7e2d-2c14-4058-aca0-669373b8004a
title: CIM_MediaPresent-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaPresent
- CIM_MediaPresent.Antecedent
- CIM_MediaPresent.Dependent
- CIM_MediaPresent.FixedMedia
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6694c945594f0ea5008f6b5f574b84accd338f89a45819a8fb02793bc619ea1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046800"
---
# <a name="cim_mediapresent-class-hyper-v-management"></a>CIM_MediaPresent-Klasse (Hyper-V-Verwaltung)

Stellt eine Beziehung dar, in der über ein Medienzugriffsgerät auf einen Speicherbereich zugegriffen werden muss.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageExtents"), MappingStrings("MIF.DMTF|Storage Devices|001.8"), AMENDMENT]
class CIM_MediaPresent : CIM_Dependency
{
  CIM_MediaAccessDevice REF Antecedent;
  CIM_StorageExtent     REF Dependent;
  boolean                   FixedMedia;
};
```

## <a name="members"></a>Member

Die **CIM \_ MediaPresent-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ MediaPresent-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ MediaAccessDevice**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")
</dt> </dl>

Das Medienzugriffsgerät.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ StorageExtent**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Abhängig")
</dt> </dl>

Der Speicherbereich, auf den bei Verwendung des Medienzugriffsgeräts zugegriffen wird.

</dd> <dt>

**FixedMedia**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**TRUE,** wenn der Speicherbereich auf dem Medienzugriffsgerät festgelegt ist und nicht eingefügt werden kann. andernfalls **FALSE.**

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CIM-Abhängigkeit**](cim-dependency.md)
</dt> </dl>

 

