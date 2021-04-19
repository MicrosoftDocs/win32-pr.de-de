---
description: 'ICE05 überprüft, ob bestimmte Tabellen erforderliche Einträge enthalten. Dies umfasst, aber ist nicht darauf beschränkt, die Eigenschaften Tabelle auf die erforderlichen Eigenschaften zu überprüfen: ProductName, productlanguage, ProductVersion, ProductCode und Hersteller.'
ms.assetid: 90b35758-c9d9-4104-a352-f0b17b04b571
title: ICE05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9710a81eca3da7ac947afb90a1d6788c0ddd74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349944"
---
# <a name="ice05"></a>ICE05

ICE05 überprüft, ob bestimmte Tabellen erforderliche Einträge enthalten. Dies umfasst, aber ist nicht darauf beschränkt, die Eigenschaften [Tabelle](property-table.md) auf die erforderlichen Eigenschaften zu überprüfen: [**ProductName**](productname.md), [**productlanguage**](productlanguage.md), [**ProductVersion**](productversion.md), [**ProductCode**](productcode.md)und [**Hersteller**](manufacturer.md).

## <a name="result"></a>Ergebnis

ICE05 gibt einen Fehler aus, wenn ein erforderlicher Eintrag fehlt.

## <a name="example"></a>Beispiel

Im gezeigten Beispiel meldet ICE05, dass der Eintrag "ProductVersion" in der Tabelle "Property" erforderlich ist.

[Eigenschaften Tabelle](property-table.md) (partiell)



| Eigenschaft                           | Wert     |
|------------------------------------|-----------|
| [**ProductName**](productname.md) | MyProduct |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



