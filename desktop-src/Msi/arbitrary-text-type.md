---
description: Der beliebige Texttyp des semantischen Typs ist einer der Textformattypen.
ms.assetid: 503ad2db-0875-4d8b-90f7-3d04318a6b62
title: Beliebiger Texttyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcf22ea2a7c4be001a5c036d3e2ee2e8c441ba061f3a7ba5bda32abde3806c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066260"
---
# <a name="arbitrary-text-type"></a>Beliebiger Texttyp

Der beliebige Texttyp des [semantischen Typs](semantic-types.md) ist einer der [Textformattypen](text-format-types.md). Dieser Typ besteht aus einer beliebigen Textzeichenfolge beliebiger Länge, die vom Benutzer bereitgestellt wird. Das Mergetool ersetzt diese beliebige Zeichenfolge in die Vorlagen, die in der Spalte Wert der [Tabelle ModuleSubs standardwert angegeben sind.](modulesubstitution-table.md)

Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modulautoren den Namen der Textzeichenfolge in die Spalte Name eingeben, "0" in die Spalte Format eingeben und die Spalten Type und ContextData der [ModuleConfiguration-Tabelle](moduleconfiguration-table.md)leer lassen. Die beliebige Textzeichenfolge kann in einer beliebigen Sprache enthalten sein, die mit der Codepage der Datenbank kompatibel ist. Weitere Informationen finden Sie unter [Codepagebehandlung (Windows Installer).](code-page-handling-windows-installer-.md) NULL ist ein gültiger Wert für die Textzeichenfolge, es sei denn, msmConfigItemNonNullable wurde im Feld Attribute der ModuleConfiguration-Tabelle enthalten.

 

 



