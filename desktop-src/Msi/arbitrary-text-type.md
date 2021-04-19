---
description: Der beliebige Texttyp des semantischen Typs ist einer der Text Format Typen.
ms.assetid: 503ad2db-0875-4d8b-90f7-3d04318a6b62
title: Beliebiger Texttyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9709a560398472fe79a2c77db827acdfa7994148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348343"
---
# <a name="arbitrary-text-type"></a>Beliebiger Texttyp

Der beliebige Texttyp des [semantischen Typs](semantic-types.md) ist einer der [Text Format Typen](text-format-types.md). Dieser Typ besteht aus einer beliebigen Text Zeichenfolge mit jeder vom Benutzer bereitgestellten Länge. Das Merge-Tool ersetzt diese willkürliche Zeichenfolge in den Vorlagen, die in der Spalte Wert der [Tabelle ModuleSubstitution](modulesubstitution-table.md)angegeben sind.

Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modul Autoren den Namen der Text Zeichenfolge in die Spalte "Name" eingeben, "0" in die Spalte "Format" eingeben und die Spalten Type und ContextData der [Tabelle ModuleConfiguration](moduleconfiguration-table.md)leer lassen. Die beliebige Text Zeichenfolge kann in jeder Sprache vorliegen, die mit der Codepage der Datenbank kompatibel ist. Weitere Informationen finden Sie unter [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md). NULL ist ein gültiger Wert für die Text Zeichenfolge, es sei denn, der msmconfigitemnonable-Wert ist im Feld Attribute der Tabelle ModuleConfiguration enthalten.

 

 



