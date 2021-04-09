---
description: Beschreibt die Funktionen des zugeordneten MSVM \_ externalethernetport.
ms.assetid: 63731b62-b1c7-4dd9-b906-03225bbc3154
title: Msvm_ExternalEthernetPortCapabilities-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ExternalEthernetPortCapabilities
- Msvm_ExternalEthernetPortCapabilities.InstanceID
- Msvm_ExternalEthernetPortCapabilities.Caption
- Msvm_ExternalEthernetPortCapabilities.Description
- Msvm_ExternalEthernetPortCapabilities.ElementName
- Msvm_ExternalEthernetPortCapabilities.IOVSupport
- Msvm_ExternalEthernetPortCapabilities.IOVSupportReasons
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 748b207151fb1d11b013af7c736de52bbe5bec8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862944"
---
# <a name="msvm_externalethernetportcapabilities-class"></a>MSVM \_ externalethernetportfunktionalitäten-Klasse

Beschreibt die Funktionen des zugeordneten [**MSVM \_ externalethernetport**](msvm-externalethernetport.md).

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ExternalEthernetPortCapabilities : CIM_Capabilities
{
  string  InstanceID;
  string  Caption = "Ethernet Port Capabilities";
  string  Description = "Describes the capabilities of the Microsoft External Ethernet Port";
  string  ElementName = "Ethernet Port Capabilities";
  boolean IOVSupport;
  string  IOVSupportReasons[];
};
```

## <a name="members"></a>Member

Die **MSVM \_ externalethernetportfunktionsklasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ externalethernetportfunktionalitäten** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des-Objekts. Diese Eigenschaft wird vom [**CIM \_ managedelta-Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet-Port Funktionen" festgelegt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "beschreibt die Funktionen des Microsoft-externen Ethernet-Ports" festgelegt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeige Name für das-Objekt. Diese Eigenschaft wird vom [**CIM \_ managedelta-Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet-Port Funktionen" festgelegt.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**IOVSupport**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein boolescher Wert, der angibt, ob die e/a-Virtualisierung (IOV) vom Netzwerkadapter unterstützt wird. Wenn der Wert **true** ist, wird IOV vom Netzwerkadapter unterstützt, und die **iovsupporwerons** -Eigenschaft ist leer. Andernfalls gibt die **iovsuppor-** Eigenschaft die Gründe dafür, warum IOV nicht unterstützt werden kann.

</dd> <dt>

**IOVSupportReasons**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von Zeichen folgen, das die möglichen Gründe angibt, warum IOV nicht unterstützt wird. Wenn der Wert von **iovsupport** den Wert **true** hat, ist dieses Array leer.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

