---
description: Windows Die Verwaltungsinstrumentation (Management Instrumentation, WMI) definiert einen Satz von Systemeigenschaften, die allen Klassen und Instanzen von Klassen zugeordnet sind.
ms.assetid: e812c0cb-3e08-4cac-8d05-2cd7abc922d1
ms.tgt_platform: multiple
title: WMI-Systemeigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3471665e2e818037bb831c8d8ab39bbe0d56e01912afb1a3399b4055d3670a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120660"
---
# <a name="wmi-system-properties"></a>WMI-Systemeigenschaften

Windows Die Verwaltungsinstrumentation (Management Instrumentation, WMI) definiert einen Satz von Systemeigenschaften, die allen Klassen und Instanzen von Klassen zugeordnet sind. Wie bei Systemklassen beginnen Systemeigenschaftennamen mit einem doppelten Unterstrich und unterscheiden sie von Eigenschaften, die von Anwendungen oder Anbietern erstellt wurden, die nicht mit einem einzelnen oder doppelten Unterstrich beginnen dürfen. Eine weitere Möglichkeit zum Identifizieren einer Systemeigenschaft ist die Verwendung der [**IWbemClassObject::Get-Methode.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get)

Systemeigenschaften sind jederzeit verfügbar, werte können jedoch **NULL** sein. **NULL** gibt an, dass eine Eigenschaft nicht für ein bestimmtes Objekt gilt. Systemeigenschaften sind jedoch möglicherweise nicht für alle Klassen oder Instanzen jederzeit verfügbar.

## <a name="system-properties"></a>Systemeigenschaften

In der folgenden Liste werden die WMI-Systemeigenschaften beschrieben. Die angegebenen Beispiele stammen aus den Systemeigenschaften der [**Win32 \_ OptionalFeature-Klasse,**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) die am Ende dieses Themas beschrieben wird.

<dl> <dt>

<span id="__Class"></span><span id="__class"></span><span id="__CLASS"></span>**\_\_Klasse**
</dt> <dd>

Datentyp: **CIM \_ STRING**

Zugriffstyp: Schreibgeschützt für Instanzen; Lesen/Schreiben für Klassen

Der Name der Klasse.

Beispiel: Win32 \_ OptionalFeature

</dd> <dt>

<span id="__Derivation"></span><span id="__derivation"></span><span id="__DERIVATION"></span>**\_\_Ableitung**
</dt> <dd>

Datentyp: **CIM \_ STRING-Array**

Zugriffstyp: Schreibgeschützt für Instanzen und Klassen

Klassenhierarchie der aktuellen Klasse oder Instanz. Das erste Element ist die unmittelbar übergeordnete Klasse, das nächste ist das übergeordnete Element usw. Das letzte Element ist die Basisklasse.

Beispiel: {CIM \_ LogicalElement, CIM \_ ManagedSystemElement}

</dd> <dt>

<span id="__Dynasty"></span><span id="__dynasty"></span><span id="__DYNASTY"></span>**\_\_Dynastie**
</dt> <dd>

Datentyp: **CIM \_ STRING**

Zugriffstyp: Schreibgeschützt

Name der Klasse der obersten Ebene, von der die Klasse oder Instanz abgeleitet wird. Wenn es sich bei dieser Klasse oder Instanz um die Klasse der obersten Ebene handelt, sind die Werte von **\_ \_ Sucht** und **\_ \_ Klasse** identisch.

Beispiel: CIM \_ ManagedSystemElement

</dd> <dt>

<span id="__Genus"></span><span id="__genus"></span><span id="__GENUS"></span>**\_\_Gattung**
</dt> <dd>

Datentyp: **CIM \_ SINT32**

Zugriffstyp: Schreibgeschützt

Wert, der verwendet wird, um zwischen Klassen und Instanzen zu unterscheiden. Dieser Wert ist **WBEM \_ GENUS \_ CLASS** (1) für Klassen und **WBEM \_ GENUS \_ INSTANCE** (2) für Instanzen und Ereignisse.

Beispiel: 2

</dd> <dt>

<span id="__Namespace"></span><span id="__namespace"></span><span id="__NAMESPACE"></span>[**\_\_Namespace**](--namespace.md)
</dt> <dd>

Datentyp: **CIM \_ STRING**

Zugriffstyp: Schreibgeschützt

Name des [*Namespace*](gloss-n.md) der Klasse oder Instanz.

Beispiel: root \\ cimv2

</dd> <dt>

<span id="__Path"></span><span id="__path"></span><span id="__PATH"></span>**\_\_Pfad**
</dt> <dd>

Datentyp: **CIM \_ STRING**

Zugriffstyp: Schreibgeschützt

Vollständiger Pfad zur Klasse oder Instanz, einschließlich Server und Namespace.

Beispiel: \\ \\ MyServer \\ root \\ cimv2:Win32 \_ OptionalFeature.Name="TelnetClient"

</dd> <dt>

<span id="__Property_Count"></span><span id="__property_count"></span><span id="__PROPERTY_COUNT"></span>**\_\_\_Eigenschaftsanzahl**
</dt> <dd>

Datentyp: **CIM \_ SINT32**

Zugriffstyp: Schreibgeschützt

Anzahl der für die Klasse oder Instanz definierten Nichtsystemeigenschaften.

Beispiel: 6

</dd> <dt>

<span id="__Relpath"></span><span id="__relpath"></span><span id="__RELPATH"></span>**\_\_Relpath**
</dt> <dd>

Datentyp: **CIM \_ STRING**

Zugriffstyp: Schreibgeschützt

Relativer Pfad zur Klasse oder Instanz.

Beispiel: Win32 \_ OptionalFeature.Name="TelnetClient"

</dd> <dt>

<span id="__Server"></span><span id="__server"></span><span id="__SERVER"></span>**\_\_Server**
</dt> <dd>

Datentyp: **CIM \_ STRING**

Zugriffstyp: Schreibgeschützt

Name des Servers, der die Klasse oder Instanz an die -Klasse oder -Instanz liefert.

Beispiel: MyServer

</dd> <dt>

<span id="__Superclass"></span><span id="__superclass"></span><span id="__SUPERCLASS"></span>**\_\_Oberklasse**
</dt> <dd>

Datentyp: **CIM \_ STRING**

Zugriffstyp: Schreibgeschützt

Name der unmittelbar übergeordneten Klasse der Klasse oder Instanz.

Beispiel: CIM \_ LogicalElement

</dd> </dl>

Der folgende PowerShell-Code ruft die Eigenschaften der [**Win32 \_ OptionalFeature-Klasse**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) ab, die die Systemeigenschaften enthält.


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



 

 
