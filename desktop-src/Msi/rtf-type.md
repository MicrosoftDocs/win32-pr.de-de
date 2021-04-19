---
description: Der RTF-Typ des semantischen Typs ist einer der Text Format Typen.
ms.assetid: 91fc47c1-520a-4002-9dbe-4ee2b56f84b3
title: RTF-Typ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81c708183596d794f20e38bf89c073472e3affb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358522"
---
# <a name="rtf-type"></a>RTF-Typ

Der RTF-Typ des [semantischen Typs](semantic-types.md) ist einer der [Text Format Typen](text-format-types.md). Dieser Typ besteht aus einer beliebigen Text Zeichenfolge im Rich-Text-Format (RTF) jeder vom Benutzer bereitgestellten Länge. Das Merge-Tool ersetzt diese Zeichenfolge in den Vorlagen, die in der Spalte Wert der [Tabelle ModuleSubstitution](modulesubstitution-table.md)angegeben sind.

Wenn Sie ein konfigurierbares Element dieses Typs angeben möchten, geben Modul Autoren den Namen der Text Zeichenfolge in die Spalte Name ein, geben Sie "0" in die Spalte "Format" ein, geben Sie "RTF" in die Typspalte ein, und lassen Sie die Spalte "ContextData" der [Tabelle "ModuleConfiguration](moduleconfiguration-table.md)" leer. Die Zeichenfolge kann in jeder Sprache vorliegen, die mit der Codepage der Datenbank kompatibel ist. Weitere Informationen finden Sie unter [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md). NULL ist ein gültiger Wert für die Text Zeichenfolge, es sei denn, der msmconfigitemnonable-Wert ist im Feld Attribute der Tabelle ModuleConfiguration enthalten.

 

 



