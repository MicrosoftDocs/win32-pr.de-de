---
description: Wenn eine Tabelle im Mergemodul in der Tabelle "moduleignoretable" aufgeführt ist, wird Sie nicht in die MSI-Datei zusammengeführt.
ms.assetid: 9ff87993-74f6-4436-b0a9-d7ebed6555bd
title: Moduleignoretable-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7b0191f616eced187411a148e40e0ae6575cca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218004"
---
# <a name="moduleignoretable-table"></a>Moduleignoretable-Tabelle

Wenn eine Tabelle im Mergemodul in der Tabelle "moduleignoretable" aufgeführt ist, wird Sie nicht in die MSI-Datei zusammengeführt. Wenn die Tabelle bereits in der MSI-Datei vorhanden ist, wird Sie nicht durch den Merge geändert. Die Tabellen in der moduleignoretable können daher Daten enthalten, die nach dem Merge nicht benötigt werden.

Die moduleignoretable-Tabelle weist die folgenden Spalten auf.



| Spalte | Typ                         | Schlüssel | Nullwerte zulässig |
|--------|------------------------------|-----|----------|
| Tabelle  | [Bezeichner](identifier.md) | J   | Nein       |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Glaub
</dt> <dd>

Der Name der Tabelle im Mergemodul, die nicht in der MSI-Datei zusammengeführt werden soll.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Um die Größe der MSM-Datei zu minimieren, wird empfohlen, dass Entwickler nicht verwendete Tabellen aus Modulen entfernen, die für die Verteilung vorgesehen sind, anstatt diese Tabellen in der Tabelle "moduleignoretable" aufzulisten.

 

 



