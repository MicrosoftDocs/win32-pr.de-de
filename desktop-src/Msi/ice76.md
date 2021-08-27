---
description: ICE76 überprüft die Verwendung des SFP-Katalogs (WFP) in Windows Installer-Paketen für Windows Me. Dieser ICE überprüft auch, ob keine Dateien in der BindImage-Tabelle auf SFP-Kataloge verweisen.
ms.assetid: e8b60b11-19ac-4ec4-aa36-a1f7a3ccd6f6
title: ICE76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a0b6caf5e29d26ba68721daa156dd0fc78a1868b5aa1ba1b7ea165834dd5ac8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129430"
---
# <a name="ice76"></a>ICE76

ICE76 überprüft die Verwendung des SFP-Katalogs (WFP) in Windows Installer-Paketen für Windows Me. Dieser ICE überprüft auch, ob keine [](bindimage-table.md) Dateien in der BindImage-Tabelle auf SFP-Kataloge verweisen.

Windows Der Dateischutz erfordert eine genaue Übereinstimmung zwischen der Datei und der signatur, die in die Katalogdatei eingebettet ist. Dateien, die auf einen SFP-Katalog verweisen, dürfen nicht in der BindImage-Tabelle aufgeführt werden, da sich die Auswirkungen der [BindImage-Aktion](bindimage-action.md) auf diese Dateien von Computer zu Computer unterscheiden. Dateien, auf die von SFP-Katalogen verwiesen wird, müssen sich in permanenten oder lokal installierten Komponenten befinden.

## <a name="result"></a>Ergebnis

ICE76 sendet einen Fehler für jede Datei in der [BindImage-Tabelle,](bindimage-table.md) die sich ebenfalls in der [FileSFPCatalog-Tabelle befindet.](filesfpcatalog-table.md)

ICE76 gibt einen Fehler aus, wenn eine Datei in der FileSFPCatalog-Tabelle zu einer Komponente mit einer der folgenden TRUE-Angaben gehört:

-   **msidbComponentAttributesPermanent** ist nicht in der Attributes -Spalte der [Component-Tabelle](component-table.md)festgelegt.
-   **msidbComponentAttributesSourceOnly** wird in der Attributes -Spalte der Component-Tabelle festgelegt.
-   **msidbAttributesOptional** wird in der Attributes -Spalte der Component-Tabelle festgelegt.

## <a name="example"></a>Beispiel

ICE76 meldet den folgenden Fehler für das Beispiel:

``` syntax
File 'File1' references a SFP catalog. Therefore it cannot be in the BindImage table.
```

[FileSFPCatalog-Tabelle](filesfpcatalog-table.md) (partiell)



| Datei\_ | SFPCatalog\_ |
|--------|--------------|
| Datei1  | Catalog1.Cat |



 

[BindImage-Tabelle](bindimage-table.md) (partiell)



| Datei\_ |
|--------|
| Datei1  |



 

Geben Sie zum Beheben dieses Problems keine Dateien ein, die auf SFP-Kataloge verweisen, in die BindImage-Tabelle.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[BindImage-Tabelle](bindimage-table.md)
</dt> <dt>

[Komponententabelle](component-table.md)
</dt> <dt>

[FileSFPCatalog-Tabelle](filesfpcatalog-table.md)
</dt> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



