---
description: Der Bezeichnertyp des semantischen Typs ist einer der Textformattypen.
ms.assetid: 137c3ad8-e47c-4cc5-b5c5-ea130236551a
title: Bezeichnertyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab1061f6d813b0803dbe1aa0d8e49e7f93cffba6e100f778901441f4bc4ed710
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118634781"
---
# <a name="identifier-type"></a>Bezeichnertyp

Der Bezeichnertyp des [semantischen Typs](semantic-types.md) ist einer der [Textformattypen](text-format-types.md). Dieser Typ besteht aus einer Vom Benutzer bereitgestellten Textzeichenfolge im Format Windows Installer [Identifier](identifier.md). Das Mergetool ersetzt diese Zeichenfolge in die Vorlagen, die in der Spalte Wert der [ModuleSubs standardwerten -Tabelle angegeben sind.](modulesubstitution-table.md)

Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modulautoren den Namen der Textzeichenfolge in die Spalte Name eingeben, "0" in die Spalte Format eingeben, "Identifier" in die Spalte Type eingeben und die Spalte ContextData der [ModuleConfiguration-Tabelle leer lassen.](moduleconfiguration-table.md) Die Zeichenfolge kann in einer beliebigen Sprache vorhanden sein, die mit der Codepage der Datenbank kompatibel ist. Weitere Informationen [finden Sie unter Codepagebehandlung (Windows Installer).](code-page-handling-windows-installer-.md) NULL ist ein gültiger Wert für die Textzeichenfolge, es sei denn, msmConfigItemNonNullable wurde im Feld Attribute der ModuleConfiguration-Tabelle enthalten.

 

 



