---
description: Der beliebige ganzzahlige Typ des semantischen Typs ist einer der ganzzahligen Format Typen.
ms.assetid: e35b27ca-be24-4aca-b12f-ca10ab153409
title: Beliebiger Integer-Typ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f55f7b7cd1c66d75a6f3aeeef1741168fad6675
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131493"
---
# <a name="arbitrary-integer-type"></a>Beliebiger Integer-Typ

Der beliebige ganzzahlige Typ des [semantischen Typs](semantic-types.md) ist einer der [ganzzahligen Format Typen](integer-format-types.md). Diese Art von konfigurier barem Element ist eine vom Benutzer bereitgestellte Ganzzahl. Das Merge-Tool ersetzt diese Ganzzahl in den Vorlagen, die in der Spalte Wert der [Tabelle ModuleSubstitution](modulesubstitution-table.md)angegeben sind.

Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modul Autoren den Namen der Text Zeichenfolge in die Spalte "Name" eingeben, "2" in die Spalte "Format" eingeben und die Spalten Type und ContextData der [Tabelle ModuleConfiguration](moduleconfiguration-table.md)leer lassen. Die Spalten "Type" und "ContextData" sind reserviert und müssen NULL sein.

 

 



