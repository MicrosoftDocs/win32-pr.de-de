---
description: Der formatierte Typ des semantischen Typs ist einer der Text Format Typen.
ms.assetid: 44af5b5c-bbf9-4043-8076-0881680a36c1
title: Formatierter Typ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b97e0c0c1763352f75424bf54d01f6871604f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041946"
---
# <a name="formatted-type"></a>Formatierter Typ

Der formatierte Typ des [semantischen Typs](semantic-types.md) ist einer der [Text Format Typen](text-format-types.md). Dieser Typ besteht aus einer beliebigen Text Zeichenfolge beliebiger Länge, die vom Benutzer bereitgestellt wird, und im Windows Installer formatierten Textformat. Weitere Informationen finden Sie unter [formatiert](formatted.md). Das Merge-Tool ersetzt diese Zeichenfolge in den Vorlagen, die in der Spalte Wert der [Tabelle ModuleSubstitution](modulesubstitution-table.md)angegeben sind.

Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modul Autoren den Namen der Text Zeichenfolge in die Spalte "Name" eingeben, "0" in die Spalte "Format" eingeben, "formatiert" in die Spalte "Type" eingeben und die Spalte "ContextData" der [Tabelle "ModuleConfiguration](moduleconfiguration-table.md)" leer lassen. Die Zeichenfolge kann in jeder Sprache vorliegen, die mit der Codepage der Datenbank kompatibel ist. Weitere Informationen finden Sie unter [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md). NULL ist ein gültiger Wert für die Text Zeichenfolge, es sei denn, der msmconfigitemnonable-Wert ist im Feld Attribute der Tabelle ModuleConfiguration enthalten.

 

 



