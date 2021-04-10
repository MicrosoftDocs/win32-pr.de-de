---
description: Der Bezeichnertyp des semantischen Typs ist einer der Text Format Typen.
ms.assetid: 137c3ad8-e47c-4cc5-b5c5-ea130236551a
title: Bezeichnertyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6d4e63b473c9ba0705c093f1dec5bcdbc1e26f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131481"
---
# <a name="identifier-type"></a>Bezeichnertyp

Der Bezeichnertyp des [semantischen Typs](semantic-types.md) ist einer der [Text Format Typen](text-format-types.md). Dieser Typ besteht aus einer Text Zeichenfolge, die vom Benutzer im Format eines Windows Installer [Bezeichners](identifier.md)bereitgestellt wird. Das Merge-Tool ersetzt diese Zeichenfolge in den Vorlagen, die in der Spalte Wert der [Tabelle ModuleSubstitution](modulesubstitution-table.md)angegeben sind.

Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modul Autoren den Namen der Text Zeichenfolge in die Spalte "Name" eingeben, "0" in die Spalte "Format" eingeben, "Identifier" in die Spalte "Type" eingeben und die Spalte "ContextData" der [Tabelle "ModuleConfiguration](moduleconfiguration-table.md)" leer lassen. Die Zeichenfolge kann in jeder Sprache vorliegen, die mit der Codepage der Datenbank kompatibel ist. Weitere Informationen finden Sie unter [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md). NULL ist ein gültiger Wert für die Text Zeichenfolge, es sei denn, der msmconfigitemnonable-Wert ist im Feld Attribute der Tabelle ModuleConfiguration enthalten.

 

 



