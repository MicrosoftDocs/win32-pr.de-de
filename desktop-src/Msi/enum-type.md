---
description: Der Enumerationstyp des semantischen Typs ist einer der Text Format Typen.
ms.assetid: fff01044-5749-42a5-b026-5b22671870bd
title: Aufzählungs Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc582a7f96d8fc91aad66387f579f05f9255346f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959393"
---
# <a name="enum-type"></a>Aufzählungs Typen

Der Enumerationstyp des [semantischen Typs](semantic-types.md) ist einer der [Text Format Typen](text-format-types.md). Dieser Typ besteht aus einer vom Benutzer ausgewählten Text Zeichenfolge aus einem Satz von Optionen. Das Merge-Tool ersetzt die ausgewählte ausgewählte Zeichenfolge in den Vorlagen, die in der Spalte Wert der [Tabelle ModuleSubstitution](modulesubstitution-table.md)angegeben sind.

Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modul Autoren den Namen der Text Zeichenfolge in die Spalte "Name" eingeben, "0" in die Spalte "Format" eingeben, "Enum" in die Spalte "Type" eingeben und die Liste der möglichen Zeichen folgen in der Spalte "ContextData" der [Tabelle "ModuleConfiguration](moduleconfiguration-table.md)" eingeben. Die Liste der möglichen Zeichen folgen muss als Liste von Zeichen folgen angegeben werden, die durch Semikolons getrennt werden. Jede Auswahl muss das Format "Name = Wert" aufweisen. Dem Wert kann ein literales Semikolon hinzugefügt werden, indem dem Semikolon ein umgekehrter Schrägstrich vorangestellt wird. NULL ist ein gültiger Wert, es sei denn, der msmconfigitemnonable-Wert ist im Feld Attribute der Tabelle ModuleConfiguration enthalten.

 

 



