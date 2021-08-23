---
description: Die Tabelle MsiPatchSequence enthält alle Informationen, die das Installationsprogramm benötigt, um die Anwendungssequenz eines kleinen Updatepatches relativ zu allen anderen Patches zu bestimmen.
ms.assetid: ae8319ad-8136-4201-9fcf-ea58ce05f88b
title: MsiPatchSequence-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc529c0f7d1a4cdd1bab568f64507922d6e28f539636600f88dea603c4fe1a52
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519800"
---
# <a name="msipatchsequence-table"></a>MsiPatchSequence-Tabelle

Die Tabelle MsiPatchSequence enthält alle Informationen, die das Installationsprogramm benötigt, um die Anwendungssequenz eines [kleinen Updatepatches](small-updates.md) relativ zu allen anderen Patches zu bestimmen. Die Tabelle muss sich in der Datenbank der Patchdatei und nicht in einer Transformation im Patch befinden. Das Installationsprogramm ignoriert diese Tabelle, wenn ein [wichtiger Upgradepatch](major-upgrades.md) angewendet wird. Beim Anwenden eines [kleineren Upgradepatches](minor-upgrades.md) verwendet das Installationsprogramm diese Tabelle nur, um abgelöste Patches zu identifizieren, die nicht sequenziert werden dürfen.

Die **Tabelle MsiPatchSequence** weist die folgenden Spalten auf.



| Spalte      | Typ                         | Key | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| PatchFamily | [Identifier](identifier.md) | J   | N        |
| ProductCode | [GUID](guid.md)             | J   | J        |
| Sequenz    | [Version](version.md)       | N   | N        |
| Attribute  | [Integer](integer.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily
</dt> <dd>

Gibt an, dass der Patch Ein Mitglied der Patchfamilie namens in diesem Feld ist. Patches in der gleichen Patchfamilie, die auf die gleiche Produktversion abzielen, werden nach den Werten in der Spalte Sequenz sortiert. Die Patches innerhalb der Patchfamilie werden in der Reihenfolge der zunehmenden Reihenfolge auf das Zielprodukt angewendet. PatchFamily wird auch verwendet, um zu bestimmen, welche Patches ersetzt werden sollen. Ein Patch kann in mehreren Zeilen aufgeführt werden und zu mehreren Patchfamilien gehören, wenn er für mehrere Produkte gilt oder mehrere Fehlerbehebungen enthält.

Der Windows Installer interpretiert den PatchFamily-Wert nur in Vergleichen auf Gleichheit mit anderen PatchFamily-Werten. Ein PatchFamily-Wert muss innerhalb des ProductCode eindeutig sein, auf den der Satz von Patches abzielt. In komplexen Patchszenarien muss der PatchFamily-Bezeichner möglicherweise global eindeutig sein.

</dd> <dt>

<span id="ProductCode"></span><span id="productcode"></span><span id="PRODUCTCODE"></span>Productcode
</dt> <dd>

Ein Wert in diesem Feld ist optional. Wenn [](product-codes.md) eine Produktcode-GUID in dieses Feld eingegeben wird und der Patch auf das angegebene Produkt angewendet wird, wird der Patch sortiert und als Member der angegebenen PatchFamily-Datei angewendet. Wenn eine Produktcode-GUID in dieses Feld eingegeben wird und der Patch nicht auf das von ProductCode angegebene Produkt angewendet wird, wird diese Zeile ignoriert. Wenn der Wert in ProductCode NULL ist, wird der Patch unabhängig vom Produktcode sortiert und als Member von PatchFamily für alle Ziele des Patches angewendet.

Ein Patch kann mehrere Zeilen in derselben PatchFamily-Datei und einen anderen ProductCode für jedes Produkt enthalten, für das der Patch vorgesehen ist. Eine Zeile für PatchFamily kann NULL für ProductCode angeben. Wenn das Zielprodukt einer Zeile mit einem ProductCode ungleich NULL entspricht, verwendet das Installationsprogramm die entsprechende Zeile und ignoriert die Zeile mit dem NULL-ProductCode. Wenn keiner der angegebenen Produktcodes mit dem Ziel übereinstimmt, wird der Patch unabhängig vom Produktcode sortiert und als Member von PatchFamily für alle Ziele des Patches angewendet.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenz
</dt> <dd>

Der Wert in der Spalte Sequence gibt die Sequenz dieses Patches innerhalb des angegebenen PatchFamily an. Der Wert in Sequence wird im Format [der Versionsdaten](version.md) ausgedrückt. Der Wert enthält zwischen 1 und 4 Felder, und jedes Feld hat einen Bereich von 0 bis 65535. Member von PatchFamily werden sortiert und auf das Zielprodukt in der Reihenfolge angewendet, in der Sequenzwerte erhöht werden. Beispielsweise erhöhen sich die folgenden sechs Werte: 1, 1.1, 1.2, 2.01, 2.01.1, 2.01.1.1.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute
</dt> <dd>

Das Vorhandensein des **msidbPatchSequenceSupersedeEarlier-Attributs** in einer Zeile gibt an, dass der [kleine Updatepatch](small-updates.md) die updates ersetzt, die von allen Patches mit kleineren Sequence-Werten in derselben PatchFamily bereitgestellt werden. Dieser Patch enthält alle Korrekturen, die von früheren Patches im angegebenen PatchFamily bereitgestellt wurden. Dieses Attribut bedeutet nicht, dass dieser Patch in allen Fällen die früheren Patches ersetzt, da die früheren Patches zu mehreren Patchfamilien gehören können.

Ein [kleiner Updatepatch](small-updates.md) kann unter keinen Umständen ein [kleineres Upgrade](minor-upgrades.md) oder einen [größeren Upgradepatch](major-upgrades.md) absetzen, auch wenn **msidbPatchSequenceSupersedeEarlier** festgelegt ist. 

| Name                                   | Wert | Bedeutung                                                           |
|----------------------------------------|-------|-------------------------------------------------------------------|
|                                        | 0x00  | Gibt einen einfachen Sequenzwert an.                              |
| **msidbPatchSequenceSupersedeEarlier** | 0x01  | Gibt einen Patch an, der frühere Patches in dieser Familie ersetzt. |



 

</dd> </dl>

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



