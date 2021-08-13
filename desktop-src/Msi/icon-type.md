---
description: Der Symboltyp des semantischen Typs ist einer der Schlüsselformattypen. Dieser Typ besteht aus einem Schlüssel in der Vom Benutzer bereitgestellten Icon-Tabelle.
ms.assetid: 8e155846-cc29-43f4-b1f7-9880320edbec
title: Symboltyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28510eff674d1f25e632b1181943af70da73d9fc97a6a64ec5abd0807fe15cf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118634953"
---
# <a name="icon-type"></a>Symboltyp

Der Symboltyp des [semantischen Typs](semantic-types.md) ist einer der [Schlüsselformattypen](key-format-types.md). Dieser Typ besteht aus einem Schlüssel in der [Vom Benutzer](icon-table.md) bereitgestellten Icon-Tabelle.

Das Mergetool muss einen gültigen Windows [Installer-Bezeichner](identifier.md) für Elemente dieses Typs ersetzen. Mergemod.dll diese Einschränkung nicht erzwingt, und es liegt in der Rolle des Mergetools, sicherzustellen, dass der Benutzer einen gültigen Schlüssel in der Icon-Tabelle zur Verfügung stellt.

NULL ist ein gültiger Wert für diesen Typ, es sei denn, msmConfigItemNonNullable wurde im Feld Attribute der [ModuleConfiguration-Tabelle enthalten.](moduleconfiguration-table.md)

Der Binärtyp kann mit den folgenden Arten von ContextData verwendet werden.

**ShortcutIcon ContextData**

Ein konfigurierbares Mergemodul kann diesen Typ verwenden, um dem Benutzer die Bereitstellung eines Fremdschlüssels für eine Zeile in der [Symboltabelle](icon-table.md) zu ermöglichen, die ein Bild enthält, das als Verknüpfungssymbol verwendet werden kann. Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modulautoren den Namen des konfigurierbaren Elements in die Spalte Name eingeben, "1" in die Spalte Format eingeben, "Symbol" in die Spalte Typ eingeben und "ShorcutIcon" in die Spalte ContextData der Tabelle ModuleConfiguration eingeben. Dieser Typ ist nicht für die Verwendung in einer Benutzeroberflächentabelle geeignet. Informationen zum Ändern eines Schlüssels für die Icon-Tabelle in diesen Tabellen finden Sie unter Icon ContextData unter [Binary Type](binary-type.md).

 

 



