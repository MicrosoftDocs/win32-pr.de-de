---
description: Die msipatchsequence-Tabelle enthält alle Informationen, die das Installationsprogramm benötigt, um die Reihenfolge der Anwendung eines kleinen Update Patches relativ zu allen anderen Patches zu bestimmen.
ms.assetid: ae8319ad-8136-4201-9fcf-ea58ce05f88b
title: Msipatchsequence-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e63252b98156a5eac1ebdc5ed5d94c7a42ec93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352568"
---
# <a name="msipatchsequence-table"></a>Msipatchsequence-Tabelle

Die msipatchsequence-Tabelle enthält alle Informationen, die das Installationsprogramm benötigt, um die Reihenfolge der Anwendung eines [kleinen Update](small-updates.md) Patches relativ zu allen anderen Patches zu bestimmen. Die Tabelle muss sich in der Datenbank der Patchdatei befinden und nicht in einer Transformation im Patch. Das Installationsprogramm ignoriert diese Tabelle beim Anwenden eines [wichtigen Upgradepatches](major-upgrades.md) . Beim Anwenden eines [geringfügigen Upgradepatches](minor-upgrades.md) verwendet das Installationsprogramm diese Tabelle nur, um ersetzte Patches zu identifizieren, die nicht sequenziert werden dürfen.

Die **msipatchsequence-Tabelle** weist die folgenden Spalten auf.



| Spalte      | Typ                         | Schlüssel | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Patchfamilie | [Bezeichner](identifier.md) | J   | N        |
| ProductCode | [GUID](guid.md)             | J   | J        |
| Sequenz    | [Version](version.md)       | N   | N        |
| Attribute  | [Integer](integer.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>Patchfamilie
</dt> <dd>

Gibt an, dass der Patch Mitglied der patchfamilie ist, die in diesem Feld benannt ist. Patches in derselben patchfamilie, die auf dieselbe Produktversion abzielen, werden nach den Werten in der Sequence-Spalte sortiert. Die Patches innerhalb der patchfamilie werden in der Reihenfolge der zunehmenden Reihenfolge auf das Ziel Produkt angewendet. Die patchfamilie wird auch verwendet, um zu bestimmen, welche Patches ersetzt werden sollen. Ein Patch kann in mehreren Zeilen aufgelistet werden und zu mehreren patchfamilien gehören, wenn er für mehr als ein Produkt gilt oder mehrere Korrekturen umfasst.

Der-Windows Installer interpretiert den Wert der patchfamilie nicht auf andere Weise als Vergleiche mit anderen patchfamilienwerten. Ein patchfamilienwert muss innerhalb von ProductCode eindeutig sein, der auf den Satz von Patches abzielt. In den komplexen patchszenarien muss der Patch-Familien Bezeichner möglicherweise global eindeutig sein.

</dd> <dt>

<span id="ProductCode"></span><span id="productcode"></span><span id="PRODUCTCODE"></span>ProductCode
</dt> <dd>

Ein Wert in diesem Feld ist optional. Wenn ein [Produktcode](product-codes.md) -GUID in dieses Feld eingegeben wird und der Patch auf das angegebene Produkt angewendet wird, wird der Patch sortiert und als Mitglied der angegebenen patchfamilie angewendet. Wenn ein Produktcode-GUID in dieses Feld eingegeben wird und der Patch nicht auf das von ProductCode angegebene Produkt angewendet wird, wird diese Zeile ignoriert. Wenn der Wert in ProductCode NULL ist, wird der Patch sortiert und als Mitglied der patchfamily für alle Ziele des Patches unabhängig vom Produktcode angewendet.

Ein Patch kann mehrere Zeilen in derselben patchfamilie und einen anderen ProductCode für jedes Produkt enthalten, das auf den Patch ausgerichtet ist. Eine Zeile für die patchfamilie kann NULL für ProductCode angeben. Wenn das Ziel Produkt einer Zeile mit einem ProductCode ungleich Null entspricht, verwendet das Installationsprogramm die übereinstimmende Zeile und ignoriert die Zeile mit dem NULL-ProductCode. Wenn keiner der angegebenen Produktcodes mit dem Ziel identisch ist, wird der Patch entsprechend des Produktcodes sortiert und als Mitglied der patchfamily für alle Ziele des Patches angewendet.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenz
</dt> <dd>

Der Wert in der Sequenz Spalte gibt die Sequenz dieses Patches in der angegebenen patchfamilie an. Der Wert in der Sequenz wird im Format der [Versions](version.md) Daten ausgedrückt. Der Wert enthält zwischen 1 und 4 Felder, und jedes Feld hat einen Bereich von 0 bis 65535. Member von patchfamily werden sortiert und auf das Ziel Produkt in der Reihenfolge der Vergrößerung von Sequenz Werten angewendet. Beispielsweise werden die folgenden sechs Werte vergrößert: 1, 1,1, 1,2, 2,01, 2.01.1, 2.01.1.1.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Legt
</dt> <dd>

Das vorhanden sein des **msidbpatchsequencesupersedefrühere** -Attributs in einer Zeile gibt an, dass der Patch für [kleine](small-updates.md) Updates die von allen Patches bereitgestellten Updates mit geringeren Sequenz Werten in derselben patchfamilie ablöst. Dieser Patch enthält alle Fixes, die von früheren Patches in der angegebenen patchfamilie bereitgestellt wurden. Dieses Attribut bedeutet nicht, dass dieser Patch die früheren Patches in allen Fällen ablöst, weil die früheren Patches mehreren patchfamilien angehören können.

Ein [kleiner Update](small-updates.md) Patch kann unter keinen Umständen ein [geringfügiges Upgrade](minor-upgrades.md) oder ein [wichtiges Upgradepatch](major-upgrades.md) ersetzen, auch wenn **msidbpatchsequencesupersedefrüher** festgelegt ist. 

| Name                                   | Wert | Bedeutung                                                           |
|----------------------------------------|-------|-------------------------------------------------------------------|
|                                        | 0x00  | Gibt einen einfachen Sequenzierungs Wert an.                              |
| **msidbpatchsequencesupersede früher** | 0x01  | Gibt einen Patch an, durch den frühere Patches in dieser Familie abgelöst werden. |



 

</dd> </dl>

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



