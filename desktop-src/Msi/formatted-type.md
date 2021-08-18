---
description: Der formatierte Typ des semantischen Typs ist einer der Textformattypen.
ms.assetid: 44af5b5c-bbf9-4043-8076-0881680a36c1
title: Formatierter Typ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09fc535a48f6d2e89cc46fb0d64ee998b8c062d6c2a406b9d5b8801ef1b62293
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044330"
---
# <a name="formatted-type"></a>Formatierter Typ

Der formatierte Typ des [semantischen Typs](semantic-types.md) ist einer der [Textformattypen.](text-format-types.md) Dieser Typ besteht aus einer beliebigen Textzeichenfolge beliebiger Länge, die vom Benutzer bereitgestellt wird, und im formatierten Textformat Windows Installer. Weitere Informationen finden Sie unter [Formatierte .](formatted.md) Das Mergetool ersetzt diese Zeichenfolge in den Vorlagen, die in der Spalte Wert der [Tabelle ModuleSubsdatenbank](modulesubstitution-table.md)angegeben sind.

Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modulautoren den Namen der Textzeichenfolge in die Spalte Name eingeben, "0" in die Spalte Format eingeben, "Formatted" in die Spalte Typ eingeben und die ContextData-Spalte der [Tabelle ModuleConfiguration](moduleconfiguration-table.md)leer lassen. Die Zeichenfolge kann in einer beliebigen Sprache enthalten sein, die mit der Codepage der Datenbank kompatibel ist. Weitere Informationen finden Sie unter [Codepagebehandlung (Windows Installer).](code-page-handling-windows-installer-.md) NULL ist ein gültiger Wert für die Textzeichenfolge, es sei denn, msmConfigItemNonNullable wurde in das Feld Attributes der Tabelle ModuleConfiguration eingefügt.

 

 



