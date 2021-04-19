---
description: Konzeptionell vergleichbar mit einem Uniform Resource Locator (URL) ist ein WMI-Objekt Pfad eine Zeichenfolge, die den Namespace auf einem Server, eine Klasse innerhalb eines Namespace oder Instanzen einer Klasse eindeutig identifiziert.
ms.assetid: 7a390541-609d-4b97-b91c-1a41d21ec17d
ms.tgt_platform: multiple
title: Beschreiben des Speicher Orts eines WMI-Objekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b58b58a6b668955d6eba1e4c51f6f8dccdac890
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345872"
---
# <a name="describing-the-location-of-a-wmi-object"></a>Beschreiben des Speicher Orts eines WMI-Objekts

Konzeptionell vergleichbar mit einem Uniform Resource Locator (URL) ist ein WMI-Objekt Pfad eine Zeichenfolge, die den Namespace auf einem Server, eine Klasse innerhalb eines Namespace oder Instanzen einer Klasse eindeutig identifiziert. Ein Objekt Pfad ist hierarchisch und enthält mehrere Elemente, die den Speicherort des fraglichen Objekts beschreiben. Wie Dateipfade können auch WMI-Objekt Pfade als relativer Pfad beschrieben oder als relativer Pfad angegeben werden.

Der Namespace eines WMI-Objekts wird auf der WMI-Referenzseite aufgeführt. Der Speicherort der meisten Klassen, die von den [cimwin32-WMI-Anbietern](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers) unterstützt werden, befindet sich z \\ . b. im root cimv2- \\ Namespace. Der folgende PowerShell-Code beschreibt einen Rückruf zum Abrufen des [**Win32- \_ Computersystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) -Objekts auf dem lokalen Computer:

`Get-WmiObject -Class Win32_ComputerSystem -Namespace "root\cimv2" -ComputerName "."`

Alternativ kann eine bestimmte Instanz von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) den folgenden Pfad aus der Eigenschaft " [**errbemubject. Path \_**](swbemobject-path-.md) " aufweisen.

`\\Machine1\root\cimv2:Win32_LogicalDisk.DeviceID="C:"`

Das folgende Beispiel zeigt den relativen Pfad zu dieser Instanz, wie durch Anzeigen der [**RelPath**](swbemobjectpath-relpath.md) -Eigenschaft des " [**errbemubjectpath**](swbemobjectpath.md) "-Objekts angezeigt, das durch den Aufrufen von " [**errbemubject. Path \_**](swbemobject-path-.md)" zurückgegeben wird.

`Win32_LogicalDisk.DeviceID="A:"`

Beachten Sie, dass **DeviceID** die Schlüsseleigenschaft der [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse ist.

## <a name="c"></a>C++

In der folgenden Tabelle sind die Objekt Pfad Typen und die zugehörigen Methoden aufgelistet, die Objekt Pfade erfordern.



<table>
<thead>
<tr class="header">
<th>Objekt Pfadtyp</th>
<th>Methode</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="describing-a-wmi-namespace-object-path.md">Namespace</a></td>
<td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-opennamespace"><strong>IWbemServices:: OpenNamespace</strong></a><br />
</dl></td>
</tr>
<tr class="even">
<td><a href="describing-a-class-object-path.md">Klasse</a></td>
<td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod"><strong>IWbemServices:: ExecMethod</strong></a><br />
[<strong>IWbemServices:: ExecMethodAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="describing-a-class-object-path.md">Klasse</a> oder <a href="describing-an-instance-object-path.md">Instanz</a></td>
<td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject"><strong>IWbemServices:: GetObject</strong></a><br />
[<strong>IWbemServices:: GetObjectAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="describing-an-instance-object-path.md">Instanz</a></td>
<td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance"><strong>IWbemServices::D eleteingestance</strong></a><br />
[<strong>IWbemServices::D eleteingestanceasync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="script"></a>Skript

Objekt Pfade können auf verschiedene Arten erstellt werden:

-   Rufen Sie die-Eigenschaft einer Methode ab, die ein Objekt vom Typ" [**errbemjectpath**](swbemobjectpath.md) " zurückgibt.
-   Rufen Sie die Eigenschaft " [**errbemubject. Path \_**](swbemobject-path-.md) " ab.
-   Erstellen Sie eine Zeichen folgen Variable, die den Objekt Pfad enthält.

In der folgenden Tabelle werden die Skript Objekte aufgelistet, die Objekt Pfade erfordern.



<table>
<thead>
<tr class="header">
<th>Skript Objekt</th>
<th>Methode</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="swbemservices.md"><strong>SWbemServices</strong></a></td>
<td><dl><a href="swbemservices-associatorsof.md"><strong>Assoziatorsof</strong></a><br />
[<strong>Associatorsofasync</strong>] (SWbemServices-associatorsofasync.MD)<br />
[<strong>Löschen</strong>] (SWbemServices-DELETE.MD)<br />
[<strong>Deleteasync</strong>] (SWbemServices-deleteasync.MD)<br />
[<strong>ExecMethod</strong>] (SWbemServices-ExecMethod.MD)<br />
[<strong>ExecMethodAsync</strong>] (SWbemServices-ExecMethodAsync.MD)<br />
[<strong>Get</strong>] (SWbemServices-Get.MD)<br />
[<strong>Getasync</strong>] (SWbemServices-getasync.MD)<br />
[<strong>Referencesto</strong>] (SWbemServices-referencesto.MD)<br />
[<strong>Referencestoasync</strong>] (SWbemServices-referencestoasync.MD)<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="swbemobjectset.md"><strong>Austauschen von "errbemubjectset"</strong></a></td>
<td><dl><a href="swbemobjectset-item.md"><strong>Element</strong></a><br />
</dl></td>
</tr>
</tbody>
</table>



 

 

 
