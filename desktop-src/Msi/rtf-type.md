---
description: Der RTF-Typ des semantischen Typs ist einer der Textformattypen.
ms.assetid: 91fc47c1-520a-4002-9dbe-4ee2b56f84b3
title: RTF-Typ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 269b378644fbf41e906993097cea8bb4fb27f969cbda046aab59700896513774
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039690"
---
# <a name="rtf-type"></a>RTF-Typ

Der RTF-Typ [des semantischen Typs](semantic-types.md) ist einer der [Textformattypen](text-format-types.md). Dieser Typ besteht aus einer beliebigen Textzeichenfolge im Rich Text Format (RTF) einer beliebigen Vom Benutzer bereitgestellten Länge. Das Mergetool ersetzt diese Zeichenfolge in die Vorlagen, die in der Spalte Wert der [ModuleSubs standardwerten -Tabelle angegeben sind.](modulesubstitution-table.md)

Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modulautoren den Namen der Textzeichenfolge in die Spalte Name eingeben, "0" in die Spalte Format eingeben, "RTF" in die Spalte Typ eingeben und die Spalte ContextData der [ModuleConfiguration-Tabelle leer lassen.](moduleconfiguration-table.md) Die Zeichenfolge kann in einer beliebigen Sprache vorhanden sein, die mit der Codepage der Datenbank kompatibel ist. Weitere Informationen [finden Sie unter Codepagebehandlung (Windows Installer).](code-page-handling-windows-installer-.md) NULL ist ein gültiger Wert für die Textzeichenfolge, es sei denn, msmConfigItemNonNullable wurde im Feld Attribute der ModuleConfiguration-Tabelle enthalten.

 

 



