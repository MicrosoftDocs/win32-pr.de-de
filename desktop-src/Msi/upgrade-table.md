---
description: Die upgradetabelle enthält Informationen, die bei größeren Upgrades erforderlich sind.
ms.assetid: f5fda405-8a09-495e-aa8c-b808a2f02b0f
title: Upgradetabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b48ce49f0f931209ccf472cd74b352c270353a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348959"
---
# <a name="upgrade-table"></a>Upgradetabelle

Die upgradetabelle enthält Informationen, die bei [größeren Upgrades](major-upgrades.md)erforderlich sind. Um die upgradefunktionen des Installers vollständig zu aktivieren, sollte jedes Paket über eine UpgradeCode-Eigenschaft und eine [**upgradetabelle**](upgradecode.md) verfügen. Jeder Datensatz in der upgradetabelle bietet eine Merkmal Kombination aus UpgradeCode, Produktversion und Sprachinformationen, die verwendet werden, um eine Gruppe von Produkten zu identifizieren, die vom Upgrade betroffen sind. Wenn die Aktion [FindRelatedProducts](findrelatedproducts-action.md) ein betroffenes Produkt erkennt, das auf dem System installiert ist, fügt Sie den Produktcode an eine Eigenschaft an, die in der Action Property-Spalte angegeben ist. Mit der Aktion " [RemoveExistingProducts](removeexistingproducts-action.md) " und der [MigrateFeatureStates](migratefeaturestates-action.md) -Aktion werden in der Spalte "action Property" aufgeführten Produkte nur entfernt oder migriert.

Die upgradetabelle enthält die in der folgenden Tabelle aufgeführten Spalten.



| Spalte         | Typ                         | Schlüssel | Nullwerte zulässig |
|----------------|------------------------------|-----|----------|
| UpgradeCode auch    | [GUID](guid.md)             | J   | N        |
| Versionmin     | [Text](text.md)             | J   | J        |
| Versionmax     | [Text](text.md)             | J   | J        |
| Sprache       | [Text](text.md)             | J   | J        |
| Attribute     | [Integer](integer.md)       | J   | N        |
| Entfernen         | [Großformatige](formatted.md)   | N   | J        |
| Aktions Eigenschaft | [Bezeichner](identifier.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="UpgradeCode"></span><span id="upgradecode"></span><span id="UPGRADECODE"></span>UpgradeCode auch
</dt> <dd>

Die [UpgradeCode](upgradecode.md) -Eigenschaft in dieser Spalte gibt den UpgradeCode aller Produkte an, die von der [FindRelatedProducts](findrelatedproducts-action.md) -Aktion erkannt werden sollen.

</dd> <dt>

<span id="VersionMin"></span><span id="versionmin"></span><span id="VERSIONMIN"></span>Versionmin
</dt> <dd>

Untere Grenze des Bereichs von Produktversionen, die von [FindRelatedProducts](findrelatedproducts-action.md)erkannt werden. Geben Sie **msidbupgraabattributesversionmininclusive** in Attribute ein, um versionmin in den Bereich einzubeziehen. Wenn versionmin eine leere Zeichenfolge ("") ist, wird Sie mit 0 ausgewertet. Wenn versionmin den Wert NULL hat, ignoriert FindRelatedProducts **msidbupgradeattributesversionmininclusive** und erkennt alle vorherigen Versionen. Versionmin und versionmax dürfen nicht beide NULL sein.

Versionmin muss eine gültige Produktversion sein, wie für die [**ProductVersion**](productversion.md) -Eigenschaft beschrieben. Beachten Sie, dass Windows Installer nur die ersten drei Felder der Produktversion verwendet. Wenn Sie ein viertes Feld in Ihre Produktversion einschließen, wird das vierte Feld vom Installationsprogramm ignoriert.

</dd> <dt>

<span id="VersionMax"></span><span id="versionmax"></span><span id="VERSIONMAX"></span>Versionmax
</dt> <dd>

Obere Grenze des Bereichs von Produktversionen, die von der [FindRelatedProducts](findrelatedproducts-action.md) -Aktion erkannt werden. Geben Sie **msidbupgraabattributesversionmaxinclusive** in Attribute ein, um versionmax in den Bereich einzubeziehen. Wenn versionmax eine leere Zeichenfolge ("") ist, wird Sie mit 0 ausgewertet. Wenn versionmax den Wert NULL hat, ignoriert FindRelatedProducts **msidbupgradeattributesversionmaxinclusive** und erkennt alle Produktversionen größer als (oder größer oder gleich) der unteren Grenze, die durch versionmin und **msidbupgradeattributesversionmininclusive** angegeben wird. Versionmin und versionmax dürfen nicht beide NULL sein.

Versionmax muss eine gültige Produktversion sein, wie für die [**ProductVersion**](productversion.md) -Eigenschaft beschrieben. Beachten Sie, dass Windows Installer nur die ersten drei Felder der Produktversion verwendet. Wenn Sie ein viertes Feld in Ihre Produktversion einschließen, wird das vierte Feld vom Installationsprogramm ignoriert.

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Kurse
</dt> <dd>

Der Satz von Sprachen, die von [FindRelatedProducts](findrelatedproducts-action.md)erkannt werden. Geben Sie eine durch Kommas getrennte Liste mit numerischen sprach Bezeichner (langid) ein. Geben Sie **msidbupgraabattributeslanguagesexclusive** in Attribute ein, um alle Sprachen zu erkennen, die in der Sprache aufgeführt sind. Wenn Language gleich NULL oder eine leere Zeichenfolge ("") ist, ignoriert "FindRelatedProducts" **msidbupgraabattributeslanguagesexclusive** und erkennt alle Sprachen.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Legt
</dt> <dd>

Diese Spalte enthält Bitflags, die Attribute der upgradetabelle angeben.



| Bitflagname                                 | Decimal | Hexadezimal | Attribut                                                                                                            |
|-----------------------------------------------|---------|-------------|----------------------------------------------------------------------------------------------------------------------|
| **msidbUpgradeAttributesMigrateFeatures**     | 1       | 0x001       | Migriert Funktions Zustände durch Aktivieren der Logik in der [MigrateFeatureStates](migratefeaturestates-action.md) -Aktion. |
| **msidbupgraabattributesonlydetect**          | 2       | 0x002       | Erkennt Produkte und Anwendungen, aber nicht.                                                               |
| **msidbupgraabattributesignoreremovefailure** | 4       | 0x004       | Die Installation wird fortgesetzt, wenn ein Produkt oder eine Anwendung nicht entfernt wird.                                              |
| **msidbupgraabattributesversionmininclusive** | 256     | 0x100       | Erkennt den Bereich von Versionen, einschließlich des Werts in versionmin.                                                     |
| **msidbupgraabattributesversionmaxinclusive** | 512     | 0x200       | Erkennt den Bereich von Versionen, einschließlich des Werts in versionmax.                                                     |
| **msidbupgraabattributeslanguagesexclusive**  | 1024    | 0x400       | Erkennt alle Sprachen, ausgenommen der in der Spalte Sprache aufgeführten Sprachen.                                        |



 

</dd> <dt>

<span id="Remove"></span><span id="remove"></span><span id="REMOVE"></span>Aufgeh
</dt> <dd>

Der Installer legt die [**Remove**](remove.md) -Eigenschaft auf Features fest, die in dieser Spalte angegeben sind. Die zu entfernenden Funktionen können zur Laufzeit bestimmt werden. Die in diesem Feld eingegebene [formatierte](formatted.md) Zeichenfolge muss eine durch Trennzeichen getrennte Liste von Featurenamen ergeben. Beispiel: \[ Feature1 \] , \[ Feature2 \] , \[ Feature3 \] . Wenn das Feld formatierten Text enthält, der zu einer leeren Zeichenfolge ("") ausgewertet wird, werden keine Features entfernt. Das Installationsprogramm legt Remove = All nur dann fest, wenn das Feld entfernen leer ist. Beachten Sie den Unterschied zwischen einer leeren Zeichenfolge und einem leeren Feld. Wenn das Feld leer ist, ist es NULL.

</dd> <dt>

<span id="ActionProperty"></span><span id="actionproperty"></span><span id="ACTIONPROPERTY"></span>Aktions Eigenschaft
</dt> <dd>

Wenn die Aktion [FindRelatedProducts](findrelatedproducts-action.md) ein auf dem System installiertes verwandtes Produkt erkennt, fügt Sie den Produktcode an die in diesem Feld angegebene Eigenschaft an. Die in dieser Spalte angegebene Eigenschaft muss eine öffentliche Eigenschaft sein, und der Paket Ersteller muss die Eigenschaft der [**securecustomproperties**](securecustomproperties.md) -Eigenschaft hinzufügen. Jede Zeile in der upgradetabelle muss über einen eindeutigen Wert für die Aktions Eigenschaft verfügen. Nach FindRelatedProducts ist der Wert dieser Eigenschaft eine durch Semikolons (;)) getrennte Liste von Produktcodes, die auf dem System erkannt werden.

</dd> </dl>

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
[ICE61](ice61.md)  
[ICE66](ice66.md)  
</dl>

 

 



