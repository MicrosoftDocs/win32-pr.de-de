---
description: Die CIM ManagedElement-Klasse ist eine abstrakte Klasse, die eine allgemeine Oberklasse (oder einen oberen Teil der Vererbungsstruktur) für die Nicht-Zuordnungsklassen im \_ CIM-Schema bietet.
ms.assetid: 6655a480-37bd-403c-9673-4eaa3d381201
title: CIM_ManagedElement-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ManagedElement
- CIM_ManagedElement.InstanceID
- CIM_ManagedElement.Caption
- CIM_ManagedElement.Description
- CIM_ManagedElement.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: acce9925f057ab63e0697c2bc12cae4336533068afdf43f46322e4d3718b25c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118648182"
---
# <a name="cim_managedelement-class"></a>CIM \_ ManagedElement-Klasse

Die **CIM \_ ManagedElement-Klasse** ist eine abstrakte Klasse, die eine allgemeine Oberklasse (oder einen oberen Teil der Vererbungsstruktur) für die Nicht-Zuordnungsklassen im CIM-Schema bietet.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ManagedElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a>Member

Die **CIM \_ ManagedElement-Klasse** verfügt über diese Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ ManagedElement-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Eine kurze Textbeschreibung des Objekts.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Textbeschreibung des Objekts.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein benutzerfreundlicher Name für das Objekt. Mit dieser Eigenschaft kann jede Instanz zusätzlich zu ihren Schlüsseleigenschaften, Identitätsdaten und Beschreibungsinformationen einen benutzerfreundlichen Namen definieren.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Identifiziert eine Instanz dieser Klasse innerhalb des Bereichs des enthaltenden Namespace eindeutig und undurchsichtig.

> [!IMPORTANT]
>
> Um die Eindeutigkeit innerhalb des Namespace sicherzustellen, sollte der Wert der **InstanceID-Eigenschaft** im folgenden Muster erstellt werden: *OrgID*:*LocalID*
>
> *OrgID* muss einen urheberrechtlich geschützten, markengebundenen oder anderweitig eindeutigen Namen enthalten, der im Besitz der Geschäftsentität ist, die **die InstanceID** definiert, oder eine registrierte ID sein, die von einer erkannten globalen Autorität zugewiesen wird. Dieses Muster ähnelt der Struktur von Schemaklassennamen. Darüber hinaus muss der erste Doppelpunkt in **InstanceID** zwischen *OrgID* und LocalID liegen, um eindeutig *zu sein.* Daher darf *die OrgID* keinen Doppelpunkt (':') enthalten.
>
> *LocalID* wird von der Geschäftsentität ausgewählt und sollte nicht erneut verwendet werden, um verschiedene zugrunde liegende reale Elemente zu identifizieren.
>
> Wenn das oben genannte Muster nicht verwendet wird, muss die definierende Entität sicherstellen, dass der resultierende **InstanceID-Wert** nicht für **InstanceID-Eigenschaften** erneut verwendet wird, die von diesem Anbieter oder anderen Anbietern für diesen Namespace erstellt werden.
>
> Für dmtf-definierte Instanzen (Distributed Management Task Force) muss das Muster mit der *OrgID* verwendet werden, die auf CIM festgelegt ist.

 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

