---
description: Eine abstrakte Klasse für Unterklassen, die eine Auflistung von CIM \_ ManagedSystemElement-Objekten darstellen. Diese Sammlungen ermöglichen es, verwaltete Systemelemente zu Identifikationszwecken zu gruppieren und die Zuordnung von Einstellungen und Konfigurationen zu vereinfachen.
ms.assetid: f47bf1d6-6d89-4d9f-82d1-99a7343481bc
title: CIM_CollectionOfMSEs -Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfMSEs
- CIM_CollectionOfMSEs.CollectionID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8598b8208b9291ec9dabc405f1b1c8d18513ff111e22ec8caa6c8bf32fb946f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813323"
---
# <a name="cim_collectionofmses-class-hyper-v-management"></a>CIM_CollectionOfMSEs -Klasse (Hyper-V-Verwaltung)

Eine abstrakte Klasse für Unterklassen, die eine Auflistung von [**CIM \_ ManagedSystemElement-Objekten**](cim-managedsystemelement.md) darstellen. Diese Sammlungen ermöglichen es, verwaltete Systemelemente zu Identifikationszwecken zu gruppieren und die Zuordnung von Einstellungen und Konfigurationen zu vereinfachen.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_CollectionOfMSEs : CIM_Collection
{
  string CollectionID;
};
```

## <a name="members"></a>Member

Die **CIM \_ CollectionOfMSEs-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ CollectionOfMSEs-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**CollectionID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Die Identifikation des Auflistungsobjekts. Bei Unterklassen kann die **CollectionID-Eigenschaft** als Schlüsseleigenschaft überschrieben werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CIM-Sammlung**](cim-collection.md)
</dt> </dl>

 

