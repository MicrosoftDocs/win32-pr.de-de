---
description: Eine abstrakte Klasse für Unterklassen, die die Fähigkeiten eines zugeordneten verwalteten Elements und das Potenzial der Fähigkeiten beschreibt.
ms.assetid: f0ffddf5-99d4-49be-ac0a-c2cfd4a92d96
title: CIM_Capabilities-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Capabilities
- CIM_Capabilities.InstanceID
- CIM_Capabilities.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7fc640950b7e943f0e549f41ec216b2832ec9de3b91938ef1aadea1893ac2faa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119561910"
---
# <a name="cim_capabilities-class"></a>CIM \_ Capabilities-Klasse

Eine abstrakte Klasse für Unterklassen, die die Fähigkeiten eines zugeordneten verwalteten Elements und das Potenzial der Fähigkeiten beschreibt.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_Capabilities : CIM_ManagedElement
{
  string InstanceID;
  string ElementName;
};
```

## <a name="members"></a>Member

Die **CIM \_ Capabilities-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ Capabilities-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Erforderlich,**](/windows/desktop/WmiSdk/standard-qualifiers) [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")
</dt> </dl>

Der benutzerfreundliche Name für diese Klasseninstanz. Darüber hinaus kann der benutzerfreundliche Name als Indexeigenschaft für eine Abfrage verwendet werden. Dieser Wert muss innerhalb seines Namespace nicht eindeutig sein.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")
</dt> </dl>

Identifiziert eine Instanz dieser Klasse innerhalb des Bereichs des enthaltenden Namespaces eindeutig und nicht transparent.

> [!IMPORTANT]
>
> Um die Eindeutigkeit innerhalb des Namespace sicherzustellen, sollte der Wert der **InstanceID-Eigenschaft** im folgenden Muster erstellt werden: *OrgID*:*LocalID*
>
> *OrgID* muss einen urheberrechtlich geschützten, markengeschützten oder anderweitig eindeutigen Namen enthalten, der sich im Besitz der Geschäftsentität befindet, die die **Instanz-ID** definiert, oder es muss sich um eine registrierte ID handeln, die von einer anerkannten globalen Autorität zugewiesen wird. Dieses Muster ähnelt der Struktur von Schemaklassennamen. Darüber hinaus muss der erste Doppelpunkt in **InstanceID** zwischen *orgID* und *LocalID* stehen, um eindeutig zu sein. Daher darf die *OrgID* keinen Doppelpunkt (":") enthalten.
>
> *LocalID* wird von der Geschäftsentität ausgewählt und sollte nicht erneut verwendet werden, um verschiedene zugrunde liegende reale Elemente zu identifizieren.
>
> Wenn das obige Muster nicht verwendet wird, muss die definierende Entität sicherstellen, dass der resultierende **InstanceID-Wert** nicht für alle **InstanceID-Eigenschaften** wiederverwendet wird, die von diesem Anbieter oder anderen Anbietern für diesen Namespace erstellt werden.
>
> Für definierte DMTF-Instanzen (Distributed Management Task Force) muss das Muster mit der *OrgID* verwendet werden, die auf CIM festgelegt ist.

 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ ManagedElement**](cim-managedelement.md)
</dt> </dl>

 

