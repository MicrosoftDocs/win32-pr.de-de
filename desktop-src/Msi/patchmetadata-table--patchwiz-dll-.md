---
description: Die PatchMetadata-Tabelle enthält Informationen zu einem Windows Installer-Patch, der zum Entfernen eines Patches erforderlich ist und von Software zum Hinzufügen/Entfernen verwendet wird.
ms.assetid: 09a06de4-0713-4e92-ab29-f34f6c94b677
title: PatchMetadata-Tabelle (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af760fbe286cf37cdb3aefe389ee8d09d7a759d3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475446"
---
# <a name="patchmetadata-table-patchwizdll"></a>PatchMetadata-Tabelle (PATCHWIZ.DLL)

Die PatchMetadata-Tabelle enthält Informationen zu einem Windows Installer-Patch, der zum Entfernen eines Patches erforderlich ist und von Software zum Hinzufügen/Entfernen verwendet wird. Alle Eigenschaften in der PatchMetadata-Tabelle werden der [MsiPatchMetadata-Tabelle](msipatchmetadata-table.md) der MSP-Datei für einen Patch hinzugefügt.

Die PatchMetadata-Tabelle ist in Eigenschaftendateien für die Patcherstellung (PCP-Dateien) erforderlich, deren MinimumRequiredMsiVersion in der [Properties-Tabelle](properties-table-patchwiz-dll-.md)gleich 300 ist. Die Tabelle ist optional, wenn MinimumRequiredMsiVersion nicht gleich 300 ist.

Die PatchMetadata-Tabelle enthält die folgenden Spalten.



| Spalte   | Typ | Schlüssel | Nullwerte zulässig |
|----------|------|-----|----------|
| Company  | text | J   | J        |
| Eigenschaft | text | J   | N        |
| Wert    | text |     | J        |



 

### <a name="columns"></a>Spalten

<dl> <dt>

<span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Unternehmen
</dt> <dd>

Der Name des Unternehmens. Ein leeres Feld (ein NULL-Wert) gibt an, dass diese Zeile eine der Standardmetadateneigenschaften enthält. Ein Unternehmen kann den Eigenschaftensatz erweitern, indem er der Tabelle eine Zeile hinzufügung und einen Firmennamen in dieses Feld ein gibt.

</dd> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Eigenschaft
</dt> <dd>

Der Name einer Metadateneigenschaft. Die Eigenschaften AllowRemoval, ManufacturerName, TargetProductName, MoreInfoURL, DisplayName, Description und Classification sind in der PatchMetadata-Tabelle erforderlich. Dieses Feld muss eine der folgenden Standardmetadateneigenschaften enthalten, wenn das Feld Company leer ist (ein NULL-Wert).




| Eigenschaft | BESCHREIBUNG | 
|----------|-------------|
| AllowRemoval | Ein ganzzahliger Wert, der angibt, ob der Patch ein <a href="uninstallable-patches.md">deinstallationsfähiges Patch ist.</a> Wenn das Feld Wert den Wert 0 (null) enthält, kann der Patch nicht entfernt werden. Wenn das Feld Wert 1 (eins) enthält, ist der Patch ein deinstallationsfähiger Patch. Diese Eigenschaft ist erforderlich. Diese Eigenschaft wird registriert, und ihr Wert kann mithilfe der <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx-Funktion erhalten</strong></a> werden.<br /> | 
| ManufacturerName | Ein Zeichenfolgenwert, der den Namen des Herstellers der Anwendung enthält. Diese Eigenschaft ist erforderlich. | 
| MinorUpdateTargetRTM | Gibt an, dass der Patch auf die RTM-Version des Produkts oder den letzten größeren Upgradepatch zielt. Erstellen Sie diese optionale Eigenschaft in kleineren Upgradepatches, die Sequenzierungsinformationen enthalten, um anzugeben, dass der Patch alle Patches bis zur RTM-Version des Produkts oder bis zum letzten größeren Upgradepatch entfernt. Diese Eigenschaft ist ab Windows Installer 3.1 verfügbar.<blockquote>[!Note]<br />Legen Sie die MinimumRequiredMsiVersion-Eigenschaft in der <a href="properties-table-patchwiz-dll-.md">Eigenschaftentabelle</a> der PCP-Datei auf 310 fest, um die Installation von Windows Installer 3.1 zum Anwenden des Patches zu verlangen.</blockquote><br /><br /> | 
| TargetProductName | Ein Zeichenfolgenwert, der den Namen der Anwendung oder Zielanwendungssammlung enthält. Diese Eigenschaft ist erforderlich. | 
| MoreInfoURL | Ein Zeichenfolgenwert, der eine URL enthält, die auf Informationen für diesen Patch verweisen. Diese erforderliche Eigenschaft wird registriert, und ihr Wert kann mithilfe der <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx-Funktion ermittelt</strong></a> werden. Ab Windows XP mit Service Pack 2 (SP2) kann dieser Wert der Supportlink für den Patch sein, der unter Programme hinzufügen/entfernen angezeigt wird.<br /> | 
| CreationTimeUTC | Ein Zeichenfolgenwert, der die Erstellungszeit der MSP-Datei in der Form mm-tt-yy HH:MM (Monat-Tag-Jahr Stunde:Minute) enthält. Diese Eigenschaft ist optional. | 
| DisplayName | Ein Zeichenfolgenwert, der den Titel für den Patch enthält, der für die öffentliche Anzeige geeignet ist. Diese Eigenschaft ist erforderlich. Diese Eigenschaft wird registriert, und ihr Wert kann mithilfe der <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx-Funktion erhalten</strong></a> werden. Ab Windows XP mit SP2 ist dieser Wert der Name des Patches, der in Programme hinzufügen/entfernen angezeigt wird, beginnend mit Windows XP mit SP2.<br /> | 
| BESCHREIBUNG | Ein Zeichenfolgenwert, der eine kurze Beschreibung des Patches enthält. Diese Eigenschaft ist erforderlich. | 
| Klassifizierung | Ein Zeichenfolgenwert, der die beliebige Kategorie von Updates enthält, wie vom Autor des Patches definiert. Patchautoren können beispielsweise angeben, dass jeder Patch als Hotfix, Sicherheitsrollup, kritisches Update, Update, Service Pack oder Updaterollup klassifiziert wird. Diese Eigenschaft ist erforderlich. | 
| OptimizedInstallMode | Wenn diese Eigenschaft in allen Patches, die in einer Transaktion angewendet werden sollen, auf 1 (eins) festgelegt ist, wird die Anwendung des Patches nach Möglichkeit optimiert. Weitere Informationen finden Sie unter <a href="patch-optimization.md">Patchoptimierung.</a> Verfügbar ab Windows Installer 3.1. | 




 

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Der Wert der Metadateneigenschaft. Dies darf nie NULL oder eine leere Zeichenfolge sein. Dieser Wert kann lokalisiert werden.

</dd> </dl>

### <a name="remarks"></a>Hinweise

Verfügbar ab Windows Installer 3.0.

Alle Eigenschaften, die in der PatchMetadata-Tabelle erstellt wurden, werden der MsiPatchMetadata-Tabelle der MSP-Datei hinzugefügt. Die Eigenschaften AllowRemoval, MoreInfoURL und DisplayName werden registriert und sind über [**msiGetPatchInfoEx zugänglich.**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)

 

 




