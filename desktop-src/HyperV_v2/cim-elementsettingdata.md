---
description: Stellt eine Zuordnung zwischen einem verwalteten Element und den zugehörigen Einstellungsdaten dar. Diese Zuordnung beschreibt auch, ob dies eine Standardeinstellung oder eine aktuelle Einstellung ist.
ms.assetid: 0df2b235-76d9-4899-938b-274ec5471324
title: CIM_ElementSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementSettingData
- CIM_ElementSettingData.ManagedElement
- CIM_ElementSettingData.SettingData
- CIM_ElementSettingData.IsDefault
- CIM_ElementSettingData.IsCurrent
- CIM_ElementSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e22dbd221f2e83009e4268cc0de337374e04298a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373076"
---
# <a name="cim_elementsettingdata-class"></a>CIM- \_ elementsettingdata-Klasse

Stellt eine Zuordnung zwischen einem verwalteten Element und den zugehörigen Einstellungsdaten dar. Diese Zuordnung beschreibt auch, ob dies eine Standardeinstellung oder eine aktuelle Einstellung ist.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Abstract, Version("2.19.1"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_ElementSettingData
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
  uint16                 IsDefault;
  uint16                 IsCurrent;
  uint16                 IsNext;
};
```

## <a name="members"></a>Member

Die **CIM \_ elementsettingdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ elementsettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**IsCurrent**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Einstellung, auf die verwiesen wird, zurzeit vom Element verwendet wird.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Is_Current"></span><span id="is_current"></span><span id="IS_CURRENT"></span>

**Ist aktuell** (1)


</dt> <dd></dd> <dt>

<span id="Is_Not_Current"></span><span id="is_not_current"></span><span id="IS_NOT_CURRENT"></span>

**Ist nicht aktuell** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**IsDefault**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Wert, der angibt, ob die Einstellung eine Standardeinstellung für das Element ist.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Is_Default"></span><span id="is_default"></span><span id="IS_DEFAULT"></span>

**Ist Standard** (1)


</dt> <dd></dd> <dt>

<span id="Is_Not_Default"></span><span id="is_not_default"></span><span id="IS_NOT_DEFAULT"></span>

**Ist nicht Standard** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**IsNext**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Flag, das angibt, wann und wie oft die Einstellung angewendet werden soll.

Die Einstellung kann z. b. auf eine neuinitialisierungs-, Zurücksetzungs-und Neukonfigurations Anforderung angewendet werden. Dies könnte eine permanente Einstellung oder eine Einstellung sein, die nur ein Mal verwendet wird, wie durch das-Flag angegeben. Wenn es sich um eine permanente Einstellung handelt, wird die Einstellung jedes Mal angewendet, wenn das verwaltete Element erneut initialisiert wird, bis dieses Flag manuell zurückgesetzt wird. Wenn es sich jedoch um eine einzelne Verwendung handelt, wird das Flag nach dem Anwenden der Einstellungen automatisch gelöscht. Wenn dieses Flag außerdem auf einen anderen Wert als 0 (unbekannt) festgelegt ist, hat dies Vorrang vor einer **SettingData** -Eigenschaft, die auf "Default" festgelegt ist.

Wenn das verwaltete Element ein Computersystem ist und der Wert dieses Flags "is Next" lautet, wird die Einstellung beim nächsten Zurücksetzen des Systems wirksam. Und wenn dieses Flag nicht geändert wird, wird es für nachfolgende System zurück Stellungen beibehalten. Wenn dieses Flag jedoch auf "Next for Single Use" festgelegt ist, wird diese Einstellung nur einmal verwendet, und das Flag würde danach auf 2 zurückgesetzt (nicht weiter). Im obigen Beispiel wird die Einstellung beim zweiten Neustart nicht verwendet, wenn das System in einer schnell Folge neu gestartet wird.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Is_Next"></span><span id="is_next"></span><span id="IS_NEXT"></span>

**Ist Next** (1)


</dt> <dd></dd> <dt>

<span id="Is_Not_Next"></span><span id="is_not_next"></span><span id="IS_NOT_NEXT"></span>

**Nicht weiter** (2)


</dt> <dd></dd> <dt>

<span id="Is_Next_For_Single_Use"></span><span id="is_next_for_single_use"></span><span id="IS_NEXT_FOR_SINGLE_USE"></span>

**Nächste Verwendung** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**"Managedelement"**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ managedelta**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Das verwaltete Element.

</dd> <dt>

**SettingData**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ SettingData**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Die Einstellungsdaten, die dem Element zugeordnet sind.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

