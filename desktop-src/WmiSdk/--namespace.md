---
description: Stellt einen WMI-Namespace dar.
ms.assetid: d5f0abc7-32cf-4d85-b5cd-5d60c991bcbc
ms.tgt_platform: multiple
title: __Namespace-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Namespace
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 9f396b588f372f26a808e97593ffcc30eac9b3ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868136"
---
# <a name="__namespace-class"></a>\_\_Namespace-Klasse

Die **\_ \_ Namespace** -System Klasse stellt einen WMI-Namespace dar.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class __Namespace : __SystemClass
{
  string Name;
};
```

## <a name="members"></a>Member

Die **\_ \_ Namespace** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ Namespace** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **Schlüssel**](standard-qualifiers.md)
</dt> </dl>

Namespacename.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ Namespace** -Klasse wird von [**\_ \_ systemclass**](--systemclass.md)abgeleitet, die keine Eigenschaften hat.

Sie können **\_ \_ Namespace** verwenden, um untergeordnete Namespaces innerhalb des aktuellen funktionierenden Namespaces zu identifizieren, zu erstellen und zu löschen, für den Sie ein [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Objekt haben. Beim Erstellen einer neuen Instanz des **\_ \_ Namespace** in einem funktionierenden Namespace wird ein untergeordneter Namespace innerhalb des funktionierenden Namespaces erstellt. Umgekehrt entfernt das Löschen einer Instanz von **\_ \_ Namespace** den untergeordneten Namespace aus dem funktionierenden Namespace. Beachten Sie, dass beim Löschen eines untergeordneten Namespace auch alle seine Klassen und Instanzen gelöscht werden.

Durch das Auflisten von Instanzen dieser Klasse in einem funktionierenden Namespace werden die verfügbaren untergeordneten Namespaces bereitgestellt.

Im Stamm \\ Namespace sind z. b. zwei Instanzen von **\_ \_ Namespace**. Der **Name** der Eigenschaft ist auf "Default" festgelegt, der andere **Name** ist auf "Cimv2" festgelegt. Diese Instanzen stellen die \\ Stamm \\ -Standard \\ \\ Namespaces bzw. root cimv2-Namespaces dar.

## <a name="examples"></a>Beispiele

Das Beispiel zum [Auflisten aller WMI-Namespaces](https://Gallery.TechNet.Microsoft.Com/4a8e84f1-4b52-452c-ae4f-e4e00e266257) VBScript in der TechNet Gallery verwendet einen rekursiven-Befehl, um alle Instanzen der \_ \_ Namespace Klasse auf einem System aufzulisten.

Das folgende Codebeispiel ruft alle Namespaces in PowerShell ab.


```PowerShell
get-wmiobject __namespace -namespace 'root' -list -recurse | format-table __namespace
```



Im folgenden Codebeispiel wird das vorherige Beispiel verbessert, und es werden zusätzliche Informationen hinzugefügt.


```PowerShell
# Set computer name 
$comp = "." 
 
# Get the name spaces on the local computer, and the local computer name 
$Namespace = get-wmiobject __namespace -namespace 'root' -list -recurse -computer $comp  
$hotsname = hostname 
 
# Display number of and names of the namespaces 
"{0} Namespaces on: {1}" -f $namespace.count, $hostname 
$NameSpace| sort __namespace  | Format-Table @{Expression = "__Namespace"; Label = "Namespace"}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_System Class**](--systemclass.md)
</dt> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> </dl>

 

 




