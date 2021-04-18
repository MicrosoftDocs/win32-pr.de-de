---
description: Beschreibt die Einschränkungen für die Eigenschaften eines zugeordneten CIM \_ enabledlogicalelement-Objekts.
ms.assetid: debce40c-9a0e-43a7-88fa-9336afd52e17
title: CIM_EnabledLogicalElementCapabilities-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EnabledLogicalElementCapabilities
- CIM_EnabledLogicalElementCapabilities.ElementNameEditSupported
- CIM_EnabledLogicalElementCapabilities.MaxElementNameLen
- CIM_EnabledLogicalElementCapabilities.RequestedStatesSupported
- CIM_EnabledLogicalElementCapabilities.ElementNameMask
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 35f400643e01821667c999342603fd402a3ae419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359083"
---
# <a name="cim_enabledlogicalelementcapabilities-class"></a>CIM \_ enabledlogicalelementfunktionalitäten-Klasse

Beschreibt die Einschränkungen für die Eigenschaften eines zugeordneten [**CIM \_ enabledlogicalelement**](cim-enabledlogicalelement.md) -Objekts.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_EnabledLogicalElementCapabilities : CIM_Capabilities
{
  boolean ElementNameEditSupported;
  uint16  MaxElementNameLen;
  uint16  RequestedStatesSupported[];
  string  ElementNameMask;
};
```

## <a name="members"></a>Member

Die **CIM \_ enabledlogicalelementfunktionsklasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ enabledlogicalelementfunktionalitäten** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Elementnameeditsupported**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-Swap. "INCITS-T11 \| \_ \_ \_ \_ \| ", "", "", "", [](/windows/desktop/WmiSdk/standard-qualifiers) "", "", "", "", "[**CIM \_ managedelta**](cim-managedelement.md)".**Elementname**")
</dt> </dl>

**true** , wenn die **ElementName** -Eigenschaft des aktivierten logischen Elements geändert werden kann. andernfalls **false**.

</dd> <dt>

**Elementnamemask**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ enabledlogicalelementutilities**".**Maxelementnamelen**")
</dt> </dl>

Ein regulärer Ausdruck, der die Einschränkungen für die Element **Name** -Eigenschaft des logischen Elements enable angibt. Die zulässige Syntax finden Sie unter *DMTF Standard ABNF mit dem Verwendungs Handbuch zur Verwaltungs Profil Spezifikation*(Anhang C).

> [!Note]  
> Wenn diese Eigenschaft und die **elementnamemask** -Eigenschaft des logischen Elements enable die maximale Länge von Element **Name** beschreiben, wird der kleinere Wert verwendet.

 

</dd> <dt>

**Maxelementnamelen**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-Swap-API. INCITS-T11-- \| \_ Einheiten config-Einheiten \_ config \_ \_ T \| maxnamechars "), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ fcswitchfunktionalitäten. elementnameeditsupported ","**CIM \_ enabledlogicalelementutilities**".**Elementnamemask**")
</dt> </dl>

Die maximal unterstützte Länge der **ElementName** -Eigenschaft des aktivierten logischen Elements.

</dd> <dt>

**Requestedstaatunter stützt**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ enabledlogicalelement**](cim-enabledlogicalelement.md)".**RequestStateChange**")
</dt> </dl>

Die möglichen Zustände, die von der [**requestStateChange**](cim-enabledlogicalelement-requeststatechange.md) -Methode auf dem aktivierten logischen Element angefordert werden können.

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Aktiviert** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deaktiviert** (3)


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

**Herunter** fahren (4)


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

**Offline** (6)


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

**Test** (7)


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

Zurück **stellen (8** )


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

Still **legung (9** )


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

**Neustart** (10)


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

**Zurücksetzen** (11)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Funktionen**](cim-capabilities.md)
</dt> </dl>

 

