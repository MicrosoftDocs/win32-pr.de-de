---
description: Bezeichner geben die Namen der Spalten (manchmal als Eigenschaften bezeichnet), Kataloge und Aliase an.
ms.assetid: 799afe2c-9217-4006-a4a3-644e5393993c
title: Bezeichner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df79bd0d70564ea3e87ff4821a1cb59e3d0a5eb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128540"
---
# <a name="identifiers"></a>Bezeichner

Bezeichner geben die Namen der Spalten (manchmal als Eigenschaften bezeichnet), Kataloge und Aliase an. System. ItemName und System. DateCreated sind z. b. die Bezeichner von zwei System definierten Eigenschafts Spalten. Literale geben dagegen Zeichen folgen Werte und numerische Werte an.


Sie können Bezeichner erstellen, die bis zu 128 Zeichen lang sind, und in einem von zwei Typen, die von den im Bezeichnernamen verwendeten Zeichen unterschieden werden:

-   **Reguläre** Bezeichner enthalten nur die Zeichen a-z, a-z, 0-9, Unterstrich ( \_ ) und Punkt (.) und beginnen mit einem Buchstaben. Sie müssen reguläre Bezeichner nicht in doppelte Anführungszeichen ("") einschließen.
-   **Begrenzungs** Bezeichner können ein beliebiges gültiges Unicode-Zeichen enthalten und müssen in doppelte Anführungszeichen eingeschlossen werden.

> [!Note]  
> In den Freitext-und enthält-Klauseln können Sie das Sternchen ( \* ) als speziellen Spalten Bezeichner verwenden, wenn Sie angeben möchten, dass die Windows-Suche alle indizierten Eigenschaften in der Abfrage enthält. Obwohl es sich nicht um einen regulären Bezeichner handelt, sind keine doppelten Anführungszeichen erforderlich.

 

 

 



