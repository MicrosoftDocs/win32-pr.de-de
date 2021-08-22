---
description: Stellt Konfigurations- und Betriebsparameter für CIM \_ ManagedElement-Instanzen dar.
ms.assetid: a9ee0eb6-dc48-43f2-bdb5-f84fe7bbc1f2
title: CIM_SettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingData
- CIM_SettingData.InstanceID
- CIM_SettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 19c62496b7980c265ff20ae0b1cdb050e311e4c5e09fd981b49b562eed14596b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118647321"
---
# <a name="cim_settingdata-class"></a>CIM \_ SettingData-Klasse

Stellt Konfigurations- und Betriebsparameter für [**CIM \_ ManagedElement-Instanzen**](cim-managedelement.md) dar.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_SettingData : CIM_ManagedElement
{
  string InstanceID;
  string ElementName;
};
```

## <a name="members"></a>Member

Die **CIM \_ SettingData-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ SettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Erforderlich,**](/windows/desktop/WmiSdk/standard-qualifiers) [**Überschreibung**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")
</dt> </dl>

Der benutzerfreundliche Name für eine Instanz dieser Klasse. Darüber hinaus kann der benutzerfreundliche Name als Index für eine Suche oder Abfrage verwendet werden. Der Name muss innerhalb eines Namespaces nicht eindeutig sein.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**Überschreibung**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig innerhalb des Bereichs des enthaltenden Namespace.

> [!IMPORTANT]
>
> Um die Eindeutigkeit innerhalb des Namespace sicherzustellen, sollte der Wert der **InstanceID-Eigenschaft** im folgenden Muster erstellt werden: *OrgID*:*LocalID*
>
> -   *OrgID* muss einen urheberrechtlich geschützten, markengebundenen oder anderweitig eindeutigen Namen enthalten, der im Besitz der Geschäftsentität ist, die die **InstanceID-Eigenschaft** definiert, oder eine registrierte ID sein, die von einer erkannten globalen Autorität zugewiesen wird.
> -   *OrgID* darf keinen Doppelpunkt enthalten. Der erste Doppelpunkt in **InstanceID** muss zwischen *OrgID* und *LocalID liegen.*
> -   *LocalID* wird von der Geschäftsentität ausgewählt und sollte nicht erneut verwendet werden, um verschiedene zugrunde liegende reale Elemente zu identifizieren.
> -   Wenn das oben genannte Muster nicht verwendet wird, muss die definierende Entität sicherstellen, dass der resultierende **InstanceID-Wert** nicht für **InstanceID-Eigenschaften** erneut verwendet wird, die von diesem Anbieter oder anderen Anbietern für diesen Namespace erstellt werden.
> -   Für DMTF-definierte Instanzen muss das Muster verwendet werden, und die *OrgID* muss auf "CIM" festgelegt sein.

 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ ManagedElement**](cim-managedelement.md)
</dt> </dl>

 

