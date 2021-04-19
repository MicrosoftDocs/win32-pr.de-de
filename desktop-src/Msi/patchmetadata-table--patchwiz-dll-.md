---
description: Die Tabelle "patchmetadata" enthält Informationen zu einem Windows Installer Patch, der zum Entfernen eines Patches erforderlich ist und das von "Software" verwendet wird.
ms.assetid: 09a06de4-0713-4e92-ab29-f34f6c94b677
title: Patchmetadata-Tabelle (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e2521684714b91d8d172f8eb56bab984ffea87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366299"
---
# <a name="patchmetadata-table-patchwizdll"></a>Patchmetadata-Tabelle (PATCHWIZ.DLL)

Die Tabelle "patchmetadata" enthält Informationen zu einem Windows Installer Patch, der zum Entfernen eines Patches erforderlich ist und das von "Software" verwendet wird. Alle Eigenschaften in der Tabelle patchmetadata werden der [MsiPatchMetadata-Tabelle](msipatchmetadata-table.md) der MSP-Datei für einen Patch hinzugefügt.

Die patchmetadata-Tabelle ist in den Eigenschaften Dateien der Patcherstellung (PCP-Dateien) erforderlich, deren minimumrequirements dmsiversion 300 in der [Properties-Tabelle](properties-table-patchwiz-dll-.md)entspricht. Die Tabelle ist optional, wenn minimumrequirements dmsiversion nicht gleich 300 ist.

Die patchmetadata-Tabelle weist die folgenden Spalten auf.



| Spalte   | Typ | Schlüssel | Nullwerte zulässig |
|----------|------|-----|----------|
| Company  | text | J   | J        |
| Eigenschaft | text | J   | N        |
| Wert    | text |     | J        |



 

### <a name="columns"></a>Spalten

<dl> <dt>

<span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Geschäfts
</dt> <dd>

Der Name des Unternehmens. Ein leeres Feld (ein NULL-Wert) gibt an, dass diese Zeile eine der standardmetadateneigenschaften enthält. Ein Unternehmen kann den Eigenschaften Satz erweitern, indem er der Tabelle eine Zeile hinzufügt und einen Firmennamen in dieses Feld eingeben.

</dd> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property
</dt> <dd>

Der Name einer Metadateneigenschaft. Die Eigenschaften allowremoval, ManufacturerName, targetproductname, MoreInfoUrl, Display Name, Description und Classification sind in der Tabelle patchmetadata erforderlich. Dieses Feld muss eine der folgenden standardmetadateneigenschaften enthalten, wenn das Feld "Company" leer ist (ein NULL-Wert).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Eigenschaft</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Allowremoval</td>
<td>Ein ganzzahliger Wert, der angibt, ob der Patch ein <a href="uninstallable-patches.md">nicht installier barer Patch</a>ist. Wenn das Wertfeld einen Wert von 0 (null) enthält, kann der Patch nicht entfernt werden. Wenn das Wertfeld 1 (eins) enthält, ist der Patch ein nicht installier barer Patch. Diese Eigenschaft ist erforderlich. Diese Eigenschaft ist registriert, und ihr Wert kann mithilfe der Funktion " <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>msigetpatchinfoex</strong></a> " abgerufen werden.<br/></td>
</tr>
<tr class="even">
<td>ManufacturerName</td>
<td>Ein Zeichen folgen Wert, der den Namen des Herstellers der Anwendung enthält. Diese Eigenschaft ist obligatorisch.</td>
</tr>
<tr class="odd">
<td>Minorupdatetargetrtm</td>
<td>Gibt an, dass der Patch die RTM-Version des Produkts oder den neuesten wichtigen Upgradepatch als Ziel hat. Erstellen Sie diese optionale Eigenschaft in hilfsupgradepatches, die Sequenz Informationen enthalten, um anzugeben, dass der Patch alle Patches bis zur RTM-Version des Produkts entfernt hat, oder bis zum neuesten wichtigen Upgradepatch. Diese Eigenschaft ist ab Windows Installer 3,1 verfügbar.
<blockquote>
[!Note]<br />
Legen Sie die Eigenschaft Minimum Requirements dmsiversion in der <a href="properties-table-patchwiz-dll-.md">Tabelle Properties</a> der PCP-Datei auf 310 fest, damit Windows Installer 3,1 installiert werden muss, damit der Patch angewendet werden kann.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>Targetproductname</td>
<td>Ein Zeichen folgen Wert, der den Namen der Anwendung oder der Ziel Anwendungssuite enthält. Diese Eigenschaft ist obligatorisch.</td>
</tr>
<tr class="odd">
<td>MoreInfoUrl</td>
<td>Ein Zeichen folgen Wert, der eine URL enthält, die auf Informationen für diesen Patch zeigt. Diese erforderliche Eigenschaft ist registriert, und ihr Wert kann mithilfe der Funktion " <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>msigetpatchinfoex</strong></a> " abgerufen werden. Ab Windows XP mit Service Pack 2 (SP2) kann dieser Wert der Support-Link für den in Software angezeigte Patch sein.<br/></td>
</tr>
<tr class="even">
<td>"Kreationtimeutc"</td>
<td>Ein Zeichen folgen Wert, der die Erstellungszeit der MSP-Datei im Format mm-dd-yy HH: mm (month-day-year Hour: Minute) enthält. Diese Eigenschaft ist optional.</td>
</tr>
<tr class="odd">
<td>DisplayName</td>
<td>Ein Zeichen folgen Wert, der den Titel für den Patch enthält, der für die öffentliche Anzeige geeignet ist. Diese Eigenschaft ist obligatorisch. Diese Eigenschaft ist registriert, und ihr Wert kann mithilfe der Funktion " <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>msigetpatchinfoex</strong></a> " abgerufen werden. Ab Windows XP mit SP2 ist dieser Wert der Name des Patches, der ab Windows XP mit SP2 unter "Programme hinzufügen/entfernen" angezeigt wird.<br/></td>
</tr>
<tr class="even">
<td>BESCHREIBUNG</td>
<td>Ein Zeichen folgen Wert, der eine kurze Beschreibung des Patches enthält. Diese Eigenschaft ist obligatorisch.</td>
</tr>
<tr class="odd">
<td>Klassifizierung</td>
<td>Ein Zeichen folgen Wert, der die beliebige Kategorie von Updates enthält, wie vom Autor des Patches definiert. Beispielsweise können patchautoren angeben, dass jeder Patch als Hotfix, Sicherheitsrollup, wichtiges Update, Update, Service Pack oder Updaterollup klassifiziert werden soll. Diese Eigenschaft ist obligatorisch.</td>
</tr>
<tr class="even">
<td>OptimizedInstallMode</td>
<td>Wenn diese Eigenschaft in allen Patches, die in einer Transaktion angewendet werden sollen, auf 1 (eins) festgelegt ist, wird die Anwendung des Patches nach Möglichkeit optimiert. Weitere Informationen finden Sie unter <a href="patch-optimization.md">Patch Optimization</a>. Verfügbar ab Windows Installer 3,1.</td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Der Wert der Metadateneigenschaft. Dies kann niemals NULL oder eine leere Zeichenfolge sein. Dieser Wert kann lokalisiert werden.

</dd> </dl>

### <a name="remarks"></a>Bemerkungen

Verfügbar ab Windows Installer 3,0.

Alle Eigenschaften, die in der Tabelle patchmetadata erstellt wurden, werden der MsiPatchMetadata-Tabelle der MSP-Datei hinzugefügt. Die Eigenschaften "allowremoval", "MoreInfoUrl" und "Display Name" sind registriert und können über " [**msigetpatchinfoex**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)" aufgerufen werden.

 

 




