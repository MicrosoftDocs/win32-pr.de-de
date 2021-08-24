---
description: ICE86 gibt eine Warnung aus, wenn das Paket die AdminUser-Eigenschaft in der Datenbankspalte des Condition-Typs verwendet. Paketautoren sollten die Privileged-Eigenschaft in bedingten Anweisungen verwenden.
ms.assetid: c23c2920-3b8b-4cd1-a570-bdeabcf11436
title: ICE86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c96e572a99fc31fea540fa4fbaad4179d1e8f2ecadebfcd9222527ca6a4afac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894990"
---
# <a name="ice86"></a>ICE86

ICE86 gibt eine Warnung aus, wenn das Paket die [**AdminUser-Eigenschaft**](adminuser.md) in der Datenbankspalte des [Condition-Typs](condition.md) verwendet. Paketautoren sollten die [**Privileged-Eigenschaft**](privileged.md) in bedingten Anweisungen verwenden.

## <a name="result"></a>Ergebnis

ICE86 gibt die folgende Warnung aus.



| ICE86-Warnung                                                                                               | BESCHREIBUNG                                                            |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| Die \` %s-Eigenschaft \` wurde in der \` %s-Spalte \` gefunden. \` %s \` in Zeile %s. \`Privilegierte \` Eigenschaften sind häufig besser geeignet. | [**Die AdminUser-Eigenschaft**](adminuser.md) wurde in einem Condition-Feld verwendet. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



