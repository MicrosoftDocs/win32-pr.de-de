---
description: Die MsiPatchMetadata-Tabelle enthält Informationen zu einem Windows Installer Patch, der erforderlich ist, um den Patch zu entfernen, und der von "Software" verwendet wird.
ms.assetid: b1c30e16-6c91-451a-8b75-7ddbcefcc092
title: MsiPatchMetadata-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2642661a8f9dc067086926f8e993fc32c95a4a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350159"
---
# <a name="msipatchmetadata-table"></a>MsiPatchMetadata-Tabelle

Die MsiPatchMetadata-Tabelle enthält Informationen zu einem Windows Installer Patch, der erforderlich ist, um den Patch zu entfernen, und **der von "** Software" verwendet wird.

Patches, die ohne diese Tabelle in der Patchdatenbank (MSP-Datei) installiert werden, können nicht entfernt werden, und es fehlen **Informationen von Software**. Die Tabelle muss sich in der Datenbank der Patchdatei befinden und nicht in einer Transformation im Patch.

Die MsiPatchMetadata-Tabelle weist die folgenden Spalten auf.



| Spalte   | Typ                         | Schlüssel | Nullwerte zulässig |
|----------|------------------------------|-----|----------|
| Company  | [Bezeichner](identifier.md) | J   | J        |
| Eigenschaft | [Bezeichner](identifier.md) | J   | N        |
| Wert    | [Text](text.md)             | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Geschäfts
</dt> <dd>

Der Name des Unternehmens. Ein leeres Feld (ein NULL-Wert) gibt an, dass die Zeile eine der standardmetadateneigenschaften der Windows Installer enthält. Weitere Informationen finden Sie im Abschnitt "Hinweise" in diesem Thema.

Wenn Sie der Tabelle eine Zeile hinzufügen und einen Firmennamen in dieses Feld eingeben, können Sie ein beliebiges Unternehmen hinzufügen, um den Eigenschaften Satz zu erweitern.

</dd> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property
</dt> <dd>

Der Name einer Metadateneigenschaft.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Der Wert der Metadateneigenschaft. Dies kann niemals NULL oder eine leere Zeichenfolge sein.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Verfügbar in Windows Installer 3,0 und höher.

Zeilen in der MsiPatchMetadata-Tabelle, die einen NULL-Wert im Feld "Unternehmenname" enthalten, verweisen auf eine der folgenden Standard-Windows Installer Metadateneigenschaften.



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
<td>Gibt an, ob der Patch ein <a href="uninstallable-patches.md">nicht installier barer Patch</a>ist. Wenn das Wertfeld 0 (null) enthält, kann der Patch nicht entfernt werden. Wenn das Wertfeld eins (1) enthält, ist der Patch ein nicht installier barer Patch. diese Eigenschaft wird registriert, und ihr Wert kann mithilfe der Funktion " <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>msigetpatchinfoex</strong></a> " abgerufen werden. <br/></td>
</tr>
<tr class="even">
<td>ManufacturerName</td>
<td>Der Name des Herstellers der Anwendung.</td>
</tr>
<tr class="odd">
<td>Minorupdatetargetrtm</td>
<td>Gibt an, dass der Patch die RTM-Version des Produkts oder den neuesten wichtigen Upgradepatch als Ziel hat. Erstellen Sie diese optionale Eigenschaft in hilfsupgradepatches, die Sequenz Informationen enthalten, um anzugeben, dass der Patch alle Patches bis zur RTM-Version des Produkts entfernt hat, oder bis zum neuesten wichtigen Upgradepatch. Diese Eigenschaft ist in Windows Installer 3,1 und höher verfügbar. <br/></td>
</tr>
<tr class="even">
<td>Targetproductname</td>
<td>Der Name der Anwendungs-oder Ziel Anwendungssuite.</td>
</tr>
<tr class="odd">
<td>MoreInfoUrl</td>
<td>Eine URL, die für diesen Patch spezifische Informationen bereitstellt. Diese Eigenschaft ist registriert, und ihr Wert kann mithilfe der Funktion " <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>msigetpatchinfoex</strong></a> " abgerufen werden. Ab Windows XP mit Service Pack 2 (SP2) kann dieser Wert der Support-Link für <strong>den in Software</strong>angezeigte Patch sein.<br/></td>
</tr>
<tr class="even">
<td>"Kreationtimeutc"</td>
<td>Erstellungszeit der MSP-Datei im Format mm-dd-yy HH: mm (month-day-year Hour: Minute).</td>
</tr>
<tr class="odd">
<td>DisplayName</td>
<td>Ein Titel für den Patch, der für die öffentliche Anzeige geeignet ist. Diese Eigenschaft ist registriert, und ihr Wert kann mithilfe der Funktion " <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>msigetpatchinfoex</strong></a> " abgerufen werden. Ab Windows XP mit SP2 ist dieser Wert der Name des Patches, der unter "Software" angezeigt <strong>wird.</strong><br/></td>
</tr>
<tr class="even">
<td>BESCHREIBUNG</td>
<td>Kurze Beschreibung des Patches.</td>
</tr>
<tr class="odd">
<td>Klassifizierung</td>
<td>Ein Zeichen folgen Wert, der die beliebige Kategorie von Updates enthält, wie vom Autor des Patches definiert. Beispielsweise können patchautoren angeben, dass jeder Patch als Hotfix, Sicherheitsrollup, wichtiges Update, Update, Service Pack oder Updaterollup klassifiziert werden soll. Diese Eigenschaft ist obligatorisch.</td>
</tr>
<tr class="even">
<td>Optimizeca</td>
<td>Gibt an, ob die Windows Installer beim Anwenden des Patches benutzerdefinierte Aktionen überspringen soll. Dadurch kann die Zeit, die zum Anwenden des Patches erforderlich ist, reduziert werden. Die optimizeca-Eigenschaft kann einen der folgenden Werte aufweisen:<br/>
<ul>
<li>0-keine benutzerdefinierten Aktionen überspringen.</li>
<li>1-überspringen Sie benutzerdefinierte Aktionen für die Eigenschaft und Verzeichnis Zuweisung. Der benutzerdefinierte <a href="custom-action-type-35.md">Aktionstyp 35</a> und der <a href="custom-action-type-51.md">benutzerdefinierte Aktionstyp 51</a> können benutzerdefinierte Aktionen der Eigenschaft und Verzeichnis Zuweisung sein.</li>
<li>2: überspringen Sie unmittelbare benutzerdefinierte Aktionen, die nicht in die Eigenschaften-oder Verzeichnis Zuweisungen fallen. Die benutzerdefinierten Aktionen enthalten in der Type-Spalte der <a href="customaction-table.md">CustomAction-Tabelle</a>nicht die msidbcustomaction typeinscript-Option.</li>
<li>4: überspringen Sie benutzerdefinierte Aktionen, die im Skript ausgeführt werden.</li>
</ul>
Der Wert von optimizeca muss für alle Patches, die installiert werden, identisch sein, oder es werden keine benutzerdefinierten Aktionen übersprungen. Wenn beispielsweise zwei Patches installiert werden und optimizeca auf die Werte 1 und 2 festgelegt ist, werden keine benutzerdefinierten Aktionen übersprungen. <br/> Die Werte von optimizeca können kombiniert werden, wenn mehrere neue Patches verarbeitet werden. Wenn alle Patches über eine (eins) in den Werten verfügen, werden alle benutzerdefinierten Aktionen der Eigenschaft und Verzeichnis Zuweisung übersprungen. Wenn ein Patch den Wert 3 (drei) für die-Eigenschaft aufweist und ein Patch den Wert 1 (eins) für die-Eigenschaft aufweist, werden die benutzerdefinierten Eigenschaften und Verzeichnis Zuweisungs Aktionen übersprungen. Die anderen unmittelbaren benutzerdefinierten Aktionen werden jedoch ausgeführt, da nicht alle angeforderten Patches übersprungen werden. <br/></td>
</tr>
<tr class="odd">
<td>OptimizedInstallMode</td>
<td>Wenn diese Eigenschaft in allen Patches, die in einer Transaktion angewendet werden sollen, auf 1 (eins) festgelegt ist, wird nach Möglichkeit eine Anwendung des Patches optimiert. Weitere Informationen finden Sie unter <a href="patch-optimization.md">Patch Optimization</a>. Verfügbar ab Windows Installer 3,1.</td>
</tr>
</tbody>
</table>



 

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




