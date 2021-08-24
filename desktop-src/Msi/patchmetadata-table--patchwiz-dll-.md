---
description: Die PatchMetadata-Tabelle enthält Informationen zu einem Windows Installer-Patch, der zum Entfernen eines Patches erforderlich ist und von Add/Remove Programs verwendet wird.
ms.assetid: 09a06de4-0713-4e92-ab29-f34f6c94b677
title: PatchMetadata-Tabelle (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5845bc279094a4a0280aa1e5e46d161c2d82b4e4037903f502230f6c6d54dca9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926150"
---
# <a name="patchmetadata-table-patchwizdll"></a>PatchMetadata-Tabelle (PATCHWIZ.DLL)

Die PatchMetadata-Tabelle enthält Informationen zu einem Windows Installer-Patch, der zum Entfernen eines Patches erforderlich ist und von Add/Remove Programs verwendet wird. Alle Eigenschaften in der PatchMetadata-Tabelle werden der [MsiPatchMetadata-Tabelle](msipatchmetadata-table.md) der MSP-Datei für einen Patch hinzugefügt.

Die PatchMetadata-Tabelle ist in Dateien mit Patcherstellungseigenschaften (PCP-Dateien) erforderlich, die in der Eigenschaftentabelle über eine MinimumRequiredMsiVersion gleich 300 [verfügen.](properties-table-patchwiz-dll-.md) Die Tabelle ist optional, wenn MinimumRequiredMsiVersion ungleich 300 ist.

Die PatchMetadata-Tabelle enthält die folgenden Spalten.



| Spalte   | Typ | Key | Nullwerte zulässig |
|----------|------|-----|----------|
| Company  | text | J   | J        |
| Eigenschaft | text | J   | N        |
| Wert    | text |     | J        |



 

### <a name="columns"></a>Spalten

<dl> <dt>

<span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Unternehmen
</dt> <dd>

Der Name des Unternehmens. Ein leeres Feld (ein NULL-Wert) gibt an, dass diese Zeile eine der Standardmetadateneigenschaften enthält. Ein Unternehmen kann den Eigenschaftensatz erweitern, indem es der Tabelle eine Zeile hinzufügt und einen Firmennamen in dieses Feld eingibt.

</dd> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Eigenschaft
</dt> <dd>

Der Name einer Metadateneigenschaft. Die Eigenschaften AllowRemoval, ManufacturerName, TargetProductName, MoreInfoURL, DisplayName, Description und Classification sind in der PatchMetadata-Tabelle erforderlich. Dieses Feld muss eine der folgenden Standardmetadateneigenschaften enthalten, wenn das Feld Company leer ist (ein NULL-Wert).



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
<td>AllowRemoval</td>
<td>Ein ganzzahliger Wert, der angibt, ob der Patch ein <a href="uninstallable-patches.md">Deinstallationsfähiger Patch</a>ist. Wenn das Feld Wert den Wert 0 (null) enthält, kann der Patch nicht entfernt werden. Wenn das Feld Wert 1 (eins) enthält, ist der Patch ein deinstallationsfähiger Patch. Diese Eigenschaft ist erforderlich. Diese Eigenschaft wird registriert, und ihr Wert kann mithilfe der <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx-Funktion</strong></a> ermittelt werden.<br/></td>
</tr>
<tr class="even">
<td>ManufacturerName</td>
<td>Ein Zeichenfolgenwert, der den Namen des Herstellers der Anwendung enthält. Diese Eigenschaft ist erforderlich.</td>
</tr>
<tr class="odd">
<td>MinorUpdateTargetRTM</td>
<td>Gibt an, dass der Patch auf die RTM-Version des Produkts oder den letzten größeren Upgradepatch ausgerichtet ist. Erstellen Sie diese optionale Eigenschaft in kleineren Upgradepatches, die Sequenzinformationen enthalten, um anzugeben, dass der Patch alle Patches bis zur RTM-Version des Produkts oder bis zum letzten Hauptupgradepatch entfernt. Diese Eigenschaft ist ab Windows Installer 3.1 verfügbar.
<blockquote>
[!Note]<br />
Damit Windows Installer 3.1 installiert werden muss, um den Patch anzuwenden, legen Sie die MinimumRequiredMsiVersion-Eigenschaft in der <a href="properties-table-patchwiz-dll-.md">Eigenschaftentabelle</a> der PCP-Datei auf 310 fest.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>TargetProductName</td>
<td>Ein Zeichenfolgenwert, der den Namen der Anwendung oder Zielanwendungssammlung enthält. Diese Eigenschaft ist erforderlich.</td>
</tr>
<tr class="odd">
<td>MoreInfoURL</td>
<td>Ein Zeichenfolgenwert, der eine URL enthält, die auf Informationen für diesen Patch verweist. Diese erforderliche Eigenschaft wird registriert, und ihr Wert kann mithilfe der <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx-Funktion</strong></a> abgerufen werden. Ab Windows XP mit Service Pack 2 (SP2) kann dieser Wert der Supportlink für den Patch sein, der unter Software angezeigt wird.<br/></td>
</tr>
<tr class="even">
<td>CreationTimeUTC</td>
<td>Ein Zeichenfolgenwert, der die Erstellungszeit der MSP-Datei im Format mm-dd-yyy HH:MM (Month-Day-Year Hour:Minute) enthält. Diese Eigenschaft ist optional.</td>
</tr>
<tr class="odd">
<td>DisplayName</td>
<td>Ein Zeichenfolgenwert, der den Titel für den Patch enthält, der für die öffentliche Anzeige geeignet ist. Diese Eigenschaft ist erforderlich. Diese Eigenschaft wird registriert, und ihr Wert kann mithilfe der <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx-Funktion</strong></a> ermittelt werden. Ab Windows XP mit SP2 ist dieser Wert der Name des Patches, der in Software ab Windows XP mit SP2 angezeigt wird.<br/></td>
</tr>
<tr class="even">
<td>BESCHREIBUNG</td>
<td>Ein Zeichenfolgenwert, der eine kurze Beschreibung des Patches enthält. Diese Eigenschaft ist erforderlich.</td>
</tr>
<tr class="odd">
<td>Klassifizierung</td>
<td>Ein Zeichenfolgenwert, der die beliebige Kategorie von Updates enthält, wie vom Autor des Patches definiert. Patchautoren können beispielsweise angeben, dass jeder Patch als Hotfix, Sicherheitsrollup, Kritisches Update, Update, Service Pack oder Updaterollup klassifiziert werden soll. Diese Eigenschaft ist erforderlich.</td>
</tr>
<tr class="even">
<td>OptimizedInstallMode</td>
<td>Wenn diese Eigenschaft in allen Patches, die in einer Transaktion angewendet werden sollen, auf 1 (eins) festgelegt ist, wird die Anwendung des Patches nach Möglichkeit optimiert. Weitere Informationen finden Sie unter <a href="patch-optimization.md">Patchoptimierung.</a> Verfügbar ab Windows Installer 3.1.</td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Wert der Metadateneigenschaft. Dies darf nie NULL oder eine leere Zeichenfolge sein. Dieser Wert kann lokalisiert werden.

</dd> </dl>

### <a name="remarks"></a>Hinweise

Verfügbar ab Windows Installer 3.0.

Alle eigenschaften, die in der PatchMetadata-Tabelle erstellt wurden, werden der MsiPatchMetadata-Tabelle der MSP-Datei hinzugefügt. Die Eigenschaften AllowRemoval, MoreInfoURL und DisplayName sind registriert und über [**msiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)zugänglich.

 

 




