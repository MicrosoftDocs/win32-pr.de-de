---
description: Die MsiPatchMetadata-Tabelle enthält Informationen zu einem Windows Installer-Patch, der zum Entfernen des Patches erforderlich ist und von Software zum Hinzufügen/Entfernen verwendet wird.
ms.assetid: b1c30e16-6c91-451a-8b75-7ddbcefcc092
title: MsiPatchMetadata-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ee71e25bf04a39d8d360c5977fad7ec72a8924b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469167"
---
# <a name="msipatchmetadata-table"></a>MsiPatchMetadata-Tabelle

Die MsiPatchMetadata-Tabelle enthält Informationen zu einem Windows Installer-Patch, der zum Entfernen des Patches erforderlich ist und von **"Software" verwendet wird.**

Patches, die ohne diese Tabelle in der Patchdatenbank (MSP-Datei) installiert sind, können nicht entfernt werden und enthalten einige Informationen unter **Software hinzufügen/entfernen.** Die Tabelle muss sich in der Datenbank der Patchdatei und nicht in einer Transformation im Patch enthalten.

Die MsiPatchMetadata-Tabelle enthält die folgenden Spalten.



| Spalte   | Typ                         | Schlüssel | Nullwerte zulässig |
|----------|------------------------------|-----|----------|
| Company  | [Identifier](identifier.md) | J   | J        |
| Eigenschaft | [Identifier](identifier.md) | J   | N        |
| Wert    | [Text](text.md)             | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Unternehmen
</dt> <dd>

Der Name des Unternehmens. Ein leeres Feld (null-Wert) gibt an, dass die Zeile eine der Standardmetadateneigenschaften des Windows enthält. Weitere Informationen finden Sie im Abschnitt "Hinweise" dieses Themas.

Indem Sie der Tabelle eine Zeile hinzufügen und einen Unternehmensnamen in dieses Feld eingeben, können Sie ein beliebiges Unternehmen hinzufügen, um den Eigenschaftensatz zu erweitern.

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




| Eigenschaft | BESCHREIBUNG | 
|----------|-------------|
| AllowRemoval | Gibt an, ob der Patch ein deinstallationsfähiger <a href="uninstallable-patches.md">Patch ist.</a> Wenn das Wertfeld 0 (null) enthält, kann der Patch nicht entfernt werden. Wenn das Wertfeld eins (1) enthält, ist der Patch ein deinstallationsfähiger Patch. Diese Eigenschaft wird registriert, und ihr Wert kann mithilfe der <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx-Funktion ermittelt</strong></a> werden. <br /> | 
| ManufacturerName | Name des Herstellers der Anwendung. | 
| MinorUpdateTargetRTM | Gibt an, dass der Patch auf die RTM-Version des Produkts oder den letzten größeren Upgradepatch zielt. Erstellen Sie diese optionale Eigenschaft in kleineren Upgradepatches, die Sequenzierungsinformationen enthalten, um anzugeben, dass der Patch alle Patches bis zur RTM-Version des Produkts oder bis zum letzten größeren Upgradepatch entfernt. Diese Eigenschaft ist ab Windows Installer 3.1 verfügbar. <br /> | 
| TargetProductName | Name der Anwendung oder Zielanwendungssammlung. | 
| MoreInfoURL | Eine URL, die spezifische Informationen zu diesem Patch enthält. Diese Eigenschaft wird registriert, und ihr Wert kann mithilfe der <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx-Funktion ermittelt</strong></a> werden. Ab Windows XP mit Service Pack 2 (SP2) kann dieser Wert der Supportlink für den Patch sein, der unter <strong>Programme hinzufügen/entfernen angezeigt wird.</strong><br /> | 
| CreationTimeUTC | Erstellungszeit der MSP-Datei in Form von mm-tt-yy HH:MM (month-day-year hour:minute). | 
| DisplayName | Ein Titel für den Patch, der für die öffentliche Anzeige in Ordnung ist. Diese Eigenschaft wird registriert, und ihr Wert kann mithilfe der <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx-Funktion ermittelt</strong></a> werden. Ab Windows XP mit SP2 ist dieser Wert der Name des Patches, der unter <strong>Programme hinzufügen/entfernen angezeigt wird.</strong><br /> | 
| BESCHREIBUNG | Kurze Beschreibung des Patches. | 
| Klassifizierung | Ein Zeichenfolgenwert, der die beliebige Kategorie von Updates enthält, wie vom Autor des Patches definiert. Patchautoren können beispielsweise angeben, dass jeder Patch als Hotfix, Sicherheitsrollup, kritisches Update, Update, Service Pack oder Updaterollup klassifiziert wird. Diese Eigenschaft ist erforderlich. | 
| OptimizeCA | Gibt an, ob der Windows-Installer beim Anwenden des Patches benutzerdefinierte Aktionen überspringen soll. Dies kann die Zeit reduzieren, die zum Anwenden des Patches erforderlich ist. Die OptimizeCA-Eigenschaft kann einen der folgenden Werte haben:<br /><ul><li>0 – Keine benutzerdefinierten Aktionen überspringen.</li><li>1 : Überspringen benutzerdefinierter Aktionen für die Eigenschaften- und Verzeichniszuweisung. <a href="custom-action-type-35.md">Der benutzerdefinierte Aktionstyp 35</a> und der <a href="custom-action-type-51.md">benutzerdefinierte Aktionstyp 51</a> können benutzerdefinierte Aktionen für Eigenschaften- und Verzeichniszuweisungen sein.</li><li>2: Überspringen Sie sofortige benutzerdefinierte Aktionen, die nicht in die Eigenschaften- oder Verzeichniszuweisungen fallen. Die unmittelbaren benutzerdefinierten Aktionen enthalten nicht die Option msidbCustomActionTypeInScript in der Type -Spalte der <a href="customaction-table.md">CustomAction-Tabelle.</a></li><li>4: Überspringen sie benutzerdefinierte Aktionen, die innerhalb des Skripts ausgeführt werden.</li></ul>Der Wert von OptimizeCA muss für alle Patches, die installiert werden, identisch sein, oder es werden keine benutzerdefinierten Aktionen übersprungen. Wenn beispielsweise zwei Patches installiert werden und OptimizeCA auf die Werte 1 bzw. 2 festgelegt ist, werden keine benutzerdefinierten Aktionen übersprungen. <br /> Die Werte von OptimizeCA können kombiniert werden, wenn mehrere neue Patches verarbeitet werden. Wenn alle Patches eine 1 (eins) in den Werten enthalten, werden alle benutzerdefinierten Aktionen zur Eigenschaften- und Verzeichniszuweisung übersprungen. Wenn ein Patch den Wert 3 (drei) für die Eigenschaft hat und ein Patch den Wert 1 (eins) für die Eigenschaft hat, werden die benutzerdefinierten Aktionen für die Eigenschaften- und Verzeichniszuweisung übersprungen. Die anderen unmittelbaren benutzerdefinierten Aktionen werden jedoch ausgeführt, da nicht alle angeforderten Patches übersprungen werden. <br /> | 
| OptimizedInstallMode | Wenn diese Eigenschaft in allen Patches, die in einer Transaktion angewendet werden sollen, auf 1 (eins) festgelegt ist, wird eine Anwendung des Patches nach Möglichkeit optimiert. Weitere Informationen finden Sie unter <a href="patch-optimization.md">Patchoptimierung.</a> Verfügbar ab Windows Installer 3.1. | 




 

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




