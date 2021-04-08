---
description: Eine abstrakte Klasse für Unterklassen, die eine Auflistung von CIM \_ ManagedSystemElement-Objekten darstellen. Mithilfe dieser Sammlungen können verwaltete Systemelemente zu Identifikationszwecken gruppiert und die Zuordnung von Einstellungen und Konfigurationen vereinfacht werden.
ms.assetid: f47bf1d6-6d89-4d9f-82d1-99a7343481bc
title: CIM_CollectionOfMSEs-Klasse (Hyper-V-Verwaltung)
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
ms.openlocfilehash: 7e467e775c78364718f25cc732d6689d9fb2b9da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864123"
---
# <a name="cim_collectionofmses-class-hyper-v-management"></a>CIM_CollectionOfMSEs-Klasse (Hyper-V-Verwaltung)

Eine abstrakte Klasse für Unterklassen, die eine Auflistung von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) -Objekten darstellen. Mithilfe dieser Sammlungen können verwaltete Systemelemente zu Identifikationszwecken gruppiert und die Zuordnung von Einstellungen und Konfigurationen vereinfacht werden.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_CollectionOfMSEs : CIM_Collection
{
  string CollectionID;
};
```

## <a name="members"></a>Member

Die **CIM \_ CollectionOfMSEs** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ CollectionOfMSEs** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Sammlungs**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Die Identifizierung des Auflistungs Objekts. Bei einer Unterklasse kann die **CollectionId** -Eigenschaft als Schlüsseleigenschaft überschrieben werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ -Auflistung**](cim-collection.md)
</dt> </dl>

 

