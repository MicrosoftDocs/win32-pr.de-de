---
description: Windows-Verwaltungsinstrumentation (WMI) definiert eine Gruppe von Systemeigenschaften, die allen Klassen und Klassen Instanzen zugeordnet sind.
ms.assetid: e812c0cb-3e08-4cac-8d05-2cd7abc922d1
ms.tgt_platform: multiple
title: WMI-System Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ee541d9de0d37c9aa1eae4ded07d3cb70ff1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215441"
---
# <a name="wmi-system-properties"></a>WMI-System Eigenschaften

Windows-Verwaltungsinstrumentation (WMI) definiert eine Gruppe von Systemeigenschaften, die allen Klassen und Klassen Instanzen zugeordnet sind. Wie bei System Klassen beginnen System Eigenschaftsnamen mit einem doppelten Unterstrich und unterscheiden sich von Eigenschaften, die von Anwendungen oder Anbietern erstellt werden, die nicht mit einem einzelnen oder einem doppelten Unterstrich beginnen dürfen. Eine andere Möglichkeit, eine System Eigenschaft zu identifizieren, ist die Verwendung der [**IWbemClassObject:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) -Methode.

System Eigenschaften sind jederzeit verfügbar, Werte sind jedoch möglicherweise **null**. **Null** gibt an, dass eine Eigenschaft nicht für ein bestimmtes Objekt gilt. Systemeigenschaften sind jedoch möglicherweise nicht immer für alle Klassen oder Instanzen verfügbar.

## <a name="system-properties"></a>Systemeigenschaften

In der folgenden Liste werden die WMI-Systemeigenschaften beschrieben. Die angegebenen Beispiele stammen aus den Systemeigenschaften der [**Win32 \_ optionalfeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) -Klasse, die unten in diesem Thema beschrieben wird.

<dl> <dt>

<span id="__Class"></span><span id="__class"></span><span id="__CLASS"></span>**\_\_Klassi**
</dt> <dd>

Datentyp: **CIM- \_ Zeichenfolge**

Zugriffstyp: schreibgeschützt für Instanzen; Lese-/Schreibzugriff für Klassen

Der Name der Klasse.

Beispiel: Win32 \_ optionalfeature

</dd> <dt>

<span id="__Derivation"></span><span id="__derivation"></span><span id="__DERIVATION"></span>**\_\_Ableitung**
</dt> <dd>

Datentyp: **CIM- \_ Zeichen** folgen Array

Zugriffstyp: schreibgeschützt sowohl für Instanzen als auch für Klassen

Klassenhierarchie der aktuellen Klasse oder Instanz. Das erste Element ist die unmittelbar übergeordnete Klasse, das nächste ist das übergeordnete Element, usw. das letzte Element ist die Basisklasse.

Beispiel: {CIM \_ LogicalElement, CIM \_ ManagedSystemElement}

</dd> <dt>

<span id="__Dynasty"></span><span id="__dynasty"></span><span id="__DYNASTY"></span>**\_\_Els**
</dt> <dd>

Datentyp: **CIM- \_ Zeichenfolge**

Zugriffstyp: Schreibgeschützt

Der Name der Klasse der obersten Ebene, von der die Klasse oder Instanz abgeleitet wird. Wenn diese Klasse oder Instanz die Klasse der obersten Ebene ist, sind die Werte von " **\_ \_ Dynastie** " und " **\_ \_ Class** " identisch.

Beispiel: CIM \_ ManagedSystemElement

</dd> <dt>

<span id="__Genus"></span><span id="__genus"></span><span id="__GENUS"></span>**\_\_Umgeleitet**
</dt> <dd>

Datentyp: **CIM \_ SINT32**

Zugriffstyp: Schreibgeschützt

Der Wert, der verwendet wird, um zwischen Klassen und Instanzen zu unterscheiden. Dieser Wert ist die **WBEM- \_ \_ Klasse Class** (1) für Klassen und die **WBEM- \_ \_ Typinstanz** (2) für-Instanzen und-Ereignisse.

Beispiel: 2

</dd> <dt>

<span id="__Namespace"></span><span id="__namespace"></span><span id="__NAMESPACE"></span>[**\_\_Namespace**](--namespace.md)
</dt> <dd>

Datentyp: **CIM- \_ Zeichenfolge**

Zugriffstyp: Schreibgeschützt

Der Name des [*Namespace*](gloss-n.md) der Klasse oder Instanz.

Beispiel: root \\ CIMV2

</dd> <dt>

<span id="__Path"></span><span id="__path"></span><span id="__PATH"></span>**\_\_ADS**
</dt> <dd>

Datentyp: **CIM- \_ Zeichenfolge**

Zugriffstyp: Schreibgeschützt

Vollständiger Pfad zur Klasse oder Instanz – einschließlich Server und Namespace.

Beispiel: \\ \\ myserver \\ root \\ CIMV2: Win32 \_ optionalfeature. Name = "Telnetclient"

</dd> <dt>

<span id="__Property_Count"></span><span id="__property_count"></span><span id="__PROPERTY_COUNT"></span>**\_\_Anzahl von Eigenschaften \_**
</dt> <dd>

Datentyp: **CIM \_ SINT32**

Zugriffstyp: Schreibgeschützt

Anzahl der nicht-Systemeigenschaften, die für die Klasse oder Instanz definiert sind.

Beispiel: 6

</dd> <dt>

<span id="__Relpath"></span><span id="__relpath"></span><span id="__RELPATH"></span>**\_\_RelPath**
</dt> <dd>

Datentyp: **CIM- \_ Zeichenfolge**

Zugriffstyp: Schreibgeschützt

Relativer Pfad zur-Klasse oder-Instanz.

Beispiel: Win32 \_ optionalfeature. Name = "Telnetclient"

</dd> <dt>

<span id="__Server"></span><span id="__server"></span><span id="__SERVER"></span>**\_\_Servers**
</dt> <dd>

Datentyp: **CIM- \_ Zeichenfolge**

Zugriffstyp: Schreibgeschützt

Der Name des Servers, der die Klasse oder Instanz bereitstellt.

Beispiel: MyServer

</dd> <dt>

<span id="__Superclass"></span><span id="__superclass"></span><span id="__SUPERCLASS"></span>**\_\_Übergeordneten Klasse**
</dt> <dd>

Datentyp: **CIM- \_ Zeichenfolge**

Zugriffstyp: Schreibgeschützt

Der Name der unmittelbaren übergeordneten Klasse der Klasse oder Instanz.

Beispiel: CIM \_ LogicalElement

</dd> </dl>

Mit dem folgenden PowerShell-Code werden die Eigenschaften der [**Win32- \_ Funktion "optionalfeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) " abgerufen, die die Systemeigenschaften enthält.


```PowerShell
Get-WmiObject win32_OptionalFeature | Where-Object {$_.name -eq "TelnetClient"}
```



Im vorherigen Codebeispiel wird Folgendes zurückgegeben:


```PowerShell
__GENUS          : 2
__CLASS          : Win32_OptionalFeature
__SUPERCLASS     : CIM_LogicalElement
__DYNASTY        : CIM_ManagedSystemElement
__RELPATH        : Win32_OptionalFeature.Name="TelnetClient"
__PROPERTY_COUNT : 6
__DERIVATION     : {CIM_LogicalElement, CIM_ManagedSystemElement}
__SERVER         : myServer
__NAMESPACE      : root\cimv2
__PATH           : \\myServer\root\cimv2:Win32_OptionalFeature.Name="TelnetClient"
Caption          : Telnet Client
Description      : 
InstallDate      : 
InstallState     : 2
Name             : TelnetClient
Status           : 
PSComputerName   : myServer
```



 

 
