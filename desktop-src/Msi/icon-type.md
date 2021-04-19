---
description: Der Symboltyp des semantischen Typs ist einer der Schlüssel Format Typen. Dieser Typ besteht aus einem Schlüssel in der vom Benutzer bereitgestellten Symboltabelle.
ms.assetid: 8e155846-cc29-43f4-b1f7-9880320edbec
title: Symboltyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a7c90de925ff34977e7ff192dffe0b8614e5734
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345774"
---
# <a name="icon-type"></a>Symboltyp

Der Symboltyp des [semantischen Typs](semantic-types.md) ist einer der [Schlüssel Format Typen](key-format-types.md). Dieser Typ besteht aus einem Schlüssel in der vom Benutzer bereitgestellten [Symboltabelle](icon-table.md) .

Das Merge-Tool muss einen gültigen Windows Installer [Bezeichner](identifier.md) für Elemente dieses Typs ersetzen. Mergemod.dll erzwingt diese Einschränkung nicht, und es liegt an dem Merge-Tool, sicherzustellen, dass der Benutzer einen gültigen Schlüssel für die Symboltabelle bereitstellt.

NULL ist ein gültiger Wert für diesen Typ, es sei denn, der msmconfigitemnonable-Wert ist im Feld Attribute der [Tabelle ModuleConfiguration](moduleconfiguration-table.md)enthalten.

Der binäre Typ kann mit den folgenden Arten von ContextData verwendet werden.

**Shortcuticon ContextData**

Ein konfigurierbares Mergemodul kann diesen Typ verwenden, um dem Benutzer zu ermöglichen, einen Fremdschlüssel für eine Zeile in der [Symboltabelle](icon-table.md) bereitzustellen, die ein Bild enthält, das für die Verwendung als Verknüpfungs Symbol geeignet ist. Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modul Autoren den Namen des konfigurierbaren Elements in die Spalte "Name" eingeben, "1" in die Spalte "Format" eingeben, "Symbol" in die Spalte "Type" eingeben und "shorcuticon" in die Spalte "ContextData" der Tabelle "ModuleConfiguration" eingeben. Dieser Typ ist nicht für die Verwendung in einer Benutzeroberflächen Tabelle geeignet. Informationen zum Ändern eines Schlüssels für die Symboltabelle in diesen Tabellen finden Sie unter "Symbol" ContextData "unter [Binary Type](binary-type.md).

 

 



