---
description: Der Enum-Typ des semantischen Typs ist einer der Textformattypen.
ms.assetid: fff01044-5749-42a5-b026-5b22671870bd
title: Enum-Typ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56c5df6b0f76cc789c148e841827a75e7184aca2892d7d6e2233843e26aac80f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869320"
---
# <a name="enum-type"></a>Enum-Typ

Der Enum-Typ des [semantischen Typs](semantic-types.md) ist einer der [Textformattypen](text-format-types.md). Dieser Typ besteht aus einer Textzeichenfolge, die vom Benutzer aus einer Reihe von Optionen ausgewählt wird. Das Mergetool ersetzt die ausgewählte Zeichenfolge in den Vorlagen, die in der Spalte Wert der [Tabelle ModuleSubs standardwert angegeben sind.](modulesubstitution-table.md)

Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modulautoren den Namen der Textzeichenfolge in die Spalte Name eingeben, "0" in die Spalte Format eingeben, "Enum" in die Spalte Typ eingeben und die Liste der möglichen Zeichenfolgen in der ContextData -Spalte der [ModuleConfiguration-Tabelle eingeben.](moduleconfiguration-table.md) Die Liste der möglichen Zeichenfolgen muss als Liste von Zeichenfolgen bereitgestellt werden, die durch Semikolons getrennt werden. Jede Auswahl muss das Formular "Name=Wert" haben. Ein literales Semikolon kann dem Wert hinzugefügt werden, indem dem Semikolon ein schräger Schrägstrich vorangestellt wird. NULL ist ein gültiger Wert, es sei denn, msmConfigItemNonNullable wurde in das Feld Attribute der ModuleConfiguration-Tabelle aufgenommen.

 

 



