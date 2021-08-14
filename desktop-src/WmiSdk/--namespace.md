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
ms.openlocfilehash: 4640570dd834b42652d04262b70ec84fac106d99f463ca22144e28ad388a0937
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320768"
---
# <a name="__namespace-class"></a>\_\_Namespace-Klasse

Die **\_ \_ Namespace-Systemklasse** stellt einen WMI-Namespace dar.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
class __Namespace : __SystemClass
{
  string Name;
};
```

## <a name="members"></a>Member

Die **\_ \_ Namespace-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ Namespace-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **Schlüssel**](standard-qualifiers.md)
</dt> </dl>

Namespacename.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\_ \_ Namespace-Klasse** wird von [**\_ \_ SystemClass**](--systemclass.md)abgeleitet, die keine Eigenschaften aufweist.

Sie können **\_ \_ Namespace** verwenden, um untergeordnete Namespaces innerhalb des aktuellen funktionierenden Namespace zu identifizieren, zu erstellen und zu löschen, für den Sie über ein [**IWbemServices-Objekt**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) verfügen. Beim Erstellen einer neuen Instanz von **\_ \_ Namespace** innerhalb eines funktionierenden Namespaces wird ein untergeordneter Namespace innerhalb des funktionierenden Namespaces erstellt. Umgekehrt entfernt das Löschen einer Instanz von **\_ \_ Namespace** den untergeordneten Namespace aus dem funktionierenden Namespace. Beachten Sie, dass beim Löschen eines untergeordneten Namespace auch alle zugehörigen Klassen und Instanzen gelöscht werden.

Durch das Aufzählen von Instanzen dieser Klasse innerhalb eines funktionierenden Namespaces werden die verfügbaren untergeordneten Namespaces bereitgestellt.

Im Stammnamespace befinden sich beispielsweise \\ zwei Instanzen von **\_ \_ Namespace**. Bei einer ist die **Name-Eigenschaft** auf "Default" festgelegt, während der andere **name** auf "Cimv2" festgelegt ist. Diese Instanzen stellen den \\ \\ Stammstandard bzw. die \\ \\ cimv2-Stammnamespaces dar.

## <a name="examples"></a>Beispiele

Im VBScript-Beispiel [List All WMI Namespaces](https://Gallery.TechNet.Microsoft.Com/4a8e84f1-4b52-452c-ae4f-e4e00e266257) im TechNet Gallery wird ein rekursiver Aufruf verwendet, um alle Instanzen der \_ \_ Namespace-Klasse auf einem System aufzulisten.

Im folgenden Codebeispiel werden alle Namespaces in PowerShell abgerufen.


```PowerShell
get-wmiobject __namespace -namespace 'root' -list -recurse | format-table __namespace
```



Das folgende Codebeispiel verbessert das vorherige Beispiel und fügt zusätzliche Informationen hinzu.


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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_\_SystemClass**](--systemclass.md)
</dt> <dt>

[WMI-Systemklassen](wmi-system-classes.md)
</dt> </dl>

 

 




