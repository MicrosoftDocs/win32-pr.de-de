---
description: Die MsiPatchMetadata-Tabelle enthält Informationen zu einem Windows Installer-Patch, der zum Entfernen des Patches erforderlich ist und von Add/Remove Programs verwendet wird.
ms.assetid: b1c30e16-6c91-451a-8b75-7ddbcefcc092
title: MsiPatchMetadata-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7094e644ff02caa1cbf4b3e53e5761740ff9a5492c92ca746404b1d243e09285
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012898"
---
# <a name="msipatchmetadata-table"></a>MsiPatchMetadata-Tabelle

Die MsiPatchMetadata-Tabelle enthält Informationen zu einem Windows Installer-Patch, der zum Entfernen des Patches erforderlich ist und von **Add/Remove Programs** verwendet wird.

Patches, die ohne diese Tabelle in der Patchdatenbank (MSP-Datei) installiert wurden, können nicht entfernt werden, und es fehlen einige Informationen unter **Software .** Die Tabelle muss sich in der Datenbank der Patchdatei und nicht in einer Transformation im Patch befinden.

Die MsiPatchMetadata-Tabelle weist die folgenden Spalten auf.



| Spalte   | Typ                         | Key | Nullwerte zulässig |
|----------|------------------------------|-----|----------|
| Company  | [Identifier](identifier.md) | J   | J        |
| Eigenschaft | [Identifier](identifier.md) | J   | N        |
| Wert    | [Text](text.md)             | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Unternehmen
</dt> <dd>

Der Name des Unternehmens. Ein leeres Feld (ein NULL-Wert) gibt an, dass die Zeile eine der Standardmetadateneigenschaften des Windows Installers enthält. Weitere Informationen finden Sie im Abschnitt "Hinweise" dieses Themas.

Indem Sie der Tabelle eine Zeile hinzufügen und einen Firmennamen in dieses Feld eingeben, können Sie ein beliebiges Unternehmen hinzufügen, um den Eigenschaftensatz zu erweitern.

</dd> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Eigenschaft
</dt> <dd>

Der Name einer Metadateneigenschaft.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Der Wert der Metadateneigenschaft. Dies darf nie NULL oder eine leere Zeichenfolge sein.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Verfügbar in Windows Installer 3.0 und höher.

Zeilen in der MsiPatchMetadata-Tabelle, die einen NULL-Wert im Feld CompanyName enthalten, verweisen auf eine der folgenden Standardeigenschaften Windows Installer-Metadaten.



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
<td>Gibt an, ob der Patch ein <a href="uninstallable-patches.md">deinstallationsfähiger Patch</a>ist oder nicht. Wenn das Wertfeld 0 (null) enthält, kann der Patch nicht entfernt werden. Wenn das Wertfeld eins (1) enthält, ist der Patch ein Deinstallationsfähiger Patch. Diese Eigenschaft ist registriert, und ihr Wert kann mithilfe der <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx-Funktion</strong></a> ermittelt werden. <br/></td>
</tr>
<tr class="even">
<td>ManufacturerName</td>
<td>Name des Herstellers der Anwendung.</td>
</tr>
<tr class="odd">
<td>MinorUpdateTargetRTM</td>
<td>Gibt an, dass der Patch auf die RTM-Version des Produkts oder den letzten größeren Upgradepatch ausgerichtet ist. Erstellen Sie diese optionale Eigenschaft in kleineren Upgradepatches, die Sequenzinformationen enthalten, um anzugeben, dass der Patch alle Patches bis zur RTM-Version des Produkts oder bis zum letzten Hauptupgradepatch entfernt. Diese Eigenschaft ist in Windows Installer 3.1 und höher verfügbar. <br/></td>
</tr>
<tr class="even">
<td>TargetProductName</td>
<td>Name der Anwendung oder Zielanwendungssammlung.</td>
</tr>
<tr class="odd">
<td>MoreInfoURL</td>
<td>Eine URL, die spezifische Informationen zu diesem Patch bereitstellt. Diese Eigenschaft wird registriert, und ihr Wert kann mithilfe der <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx-Funktion</strong></a> abgerufen werden. Ab Windows XP mit Service Pack 2 (SP2) kann dieser Wert der Supportlink für den Patch sein, der unter <strong>Software hinzufügen/entfernen</strong>angezeigt wird.<br/></td>
</tr>
<tr class="even">
<td>CreationTimeUTC</td>
<td>Erstellungszeit der MSP-Datei in Form von mm-dd-yyy HH:MM (Monat-Tag-Jahr Stunde:Minute).</td>
</tr>
<tr class="odd">
<td>DisplayName</td>
<td>Ein Titel für den Patch, der für die öffentliche Anzeige geeignet ist. Diese Eigenschaft ist registriert, und ihr Wert kann mithilfe der <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx-Funktion</strong></a> abgerufen werden. Ab Windows XP mit SP2 ist dieser Wert der Name des Patches, der unter <strong>Add/Remove Programs (Software hinzufügen/entfernen)</strong>angezeigt wird.<br/></td>
</tr>
<tr class="even">
<td>BESCHREIBUNG</td>
<td>Kurze Beschreibung des Patches.</td>
</tr>
<tr class="odd">
<td>Klassifizierung</td>
<td>Ein Zeichenfolgenwert, der die beliebige Kategorie von Updates enthält, wie vom Autor des Patches definiert. Patchautoren können beispielsweise angeben, dass jeder Patch als Hotfix, Sicherheitsrollup, Kritisches Update, Update, Service Pack oder Updaterollup klassifiziert werden soll. Diese Eigenschaft ist erforderlich.</td>
</tr>
<tr class="even">
<td>OptimizeCA</td>
<td>Gibt an, ob der Windows Installer beim Anwenden des Patches benutzerdefinierte Aktionen überspringen soll. Dies kann die Zeit verkürzen, die zum Anwenden des Patches erforderlich ist. Die OptimizeCA-Eigenschaft kann einen der folgenden Werte aufweisen:<br/>
<ul>
<li>0 : Überspringen Sie keine benutzerdefinierten Aktionen.</li>
<li>1: Überspringt benutzerdefinierte Aktionen zur Eigenschaften- und Verzeichniszuweisung. <a href="custom-action-type-35.md">Benutzerdefinierter Aktionstyp 35</a> und <a href="custom-action-type-51.md">benutzerdefinierter Aktionstyp 51</a> können benutzerdefinierte Aktionen für Eigenschaften- und Verzeichniszuweisungen sein.</li>
<li>2: Überspringen Sie sofortige benutzerdefinierte Aktionen, die nicht in die Eigenschaften- oder Verzeichniszuweisungen fallen. Die unmittelbaren benutzerdefinierten Aktionen enthalten keine msidbCustomActionTypeInScript-Option in der Spalte Type der <a href="customaction-table.md">CustomAction-Tabelle.</a></li>
<li>4: Überspringen sie benutzerdefinierte Aktionen, die im Skript ausgeführt werden.</li>
</ul>
Der Wert von OptimizeCA muss für alle installierten Patches identisch sein, oder es werden keine benutzerdefinierten Aktionen übersprungen. Wenn beispielsweise zwei Patches installiert werden und OptimizeCA auf die Werte 1 bzw. 2 festgelegt ist, werden keine benutzerdefinierten Aktionen übersprungen. <br/> Die Werte von OptimizeCA können kombiniert werden, wenn mehrere neue Patches verarbeitet werden. Wenn alle Patches eine 1 (eins) in den Werten enthalten, werden alle benutzerdefinierten Aktionen zur Eigenschaften- und Verzeichniszuweisung übersprungen. Wenn ein Patch den Wert 3 (drei) für die Eigenschaft und ein Patch den Wert 1 (eins) für die Eigenschaft hat, werden die benutzerdefinierten Aktionen für die Eigenschaft und verzeichniszuweisung übersprungen. Die anderen unmittelbaren benutzerdefinierten Aktionen werden jedoch ausgeführt, da nicht alle angeforderten Patches übersprungen werden. <br/></td>
</tr>
<tr class="odd">
<td>OptimizedInstallMode</td>
<td>Wenn diese Eigenschaft in allen Patches, die in einer Transaktion angewendet werden sollen, auf 1 (eins) festgelegt ist, wird eine Anwendung des Patches nach Möglichkeit optimiert. Weitere Informationen finden Sie unter <a href="patch-optimization.md">Patchoptimierung.</a> Verfügbar ab Windows Installer 3.1.</td>
</tr>
</tbody>
</table>



 

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




