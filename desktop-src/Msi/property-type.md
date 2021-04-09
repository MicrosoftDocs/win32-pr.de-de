---
description: Der Eigenschaftentyp des semantischen Typs ist einer der Schlüssel Format Typen. Dieser Typ besteht aus einem Fremdschlüssel in der vom Benutzer bereitgestellten Eigenschaften Tabelle.
ms.assetid: 819e4e90-0bc3-41ba-851d-1d4c52b6eeea
title: Eigenschaftstyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36236c78160abbfe3ad64c6b801a3cdbdbb98b48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042236"
---
# <a name="property-type"></a>Eigenschaftstyp

Der Eigenschaftentyp des [semantischen Typs](semantic-types.md) ist einer der [Schlüssel Format Typen](key-format-types.md). Dieser Typ besteht aus einem Fremdschlüssel in der vom Benutzer bereitgestellten [Eigenschaften Tabelle](property-table.md) .

Das Merge-Tool muss einen gültigen Windows Installer [Bezeichner](identifier.md) für Elemente dieses Typs ersetzen. Mergemod.dll erzwingt diese Einschränkung nicht, und es liegt an dem Merge-Tool, sicherzustellen, dass der Benutzer einen gültigen Schlüssel in der Eigenschaften Tabelle bereitstellt. Die Primärschlüssel der Eigenschaften Tabelle sind die Eigenschaftsnamen.

NULL ist ein gültiger Wert für diesen Typ, es sei denn, der msmconfigitemnonable-Wert ist im Feld Attribute der [Tabelle ModuleConfiguration](moduleconfiguration-table.md)enthalten.

Der Eigenschaftentyp kann mit den folgenden Arten von ContextData verwendet werden.

**NULL-ContextData**

Ein konfigurierbares Mergemodul kann diesen Typ verwenden, um dem Benutzer zu ermöglichen, einen Eigenschaftsnamen für eine Datenbanktabelle im Modul bereitzustellen. Das Merge-Tool ersetzt den Bezeichner der Eigenschaft in den Vorlagen in der Spalte Wert der [Tabelle ModuleSubstitution](modulesubstitution-table.md). Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modul Autoren den Namen des konfigurierbaren Elements in die Spalte "Name" eingeben. Geben Sie "1" in die Spalte "Format" ein, geben Sie "Property" in die Spalte "Type" ein, und lassen Sie die Spalte "ContextData" der [Tabelle "ModuleConfiguration](moduleconfiguration-table.md)" leer.

**Öffentliches ContextData**

Ein konfigurierbares Mergemodul kann diesen Typ verwenden, um dem Benutzer zu ermöglichen, den Namen einer [öffentlichen Eigenschaft](public-properties.md) für eine Datenbanktabelle im Modul bereitzustellen. Das Merge-Tool ersetzt den Bezeichner der Eigenschaft in den Vorlagen in der Spalte Wert der [Tabelle ModuleSubstitution](modulesubstitution-table.md). Wenn Sie ein konfigurierbares Element dieses Typs angeben möchten, geben Modul Autoren den Namen des konfigurierbaren Elements in die Spalte Name ein, geben Sie "1" in die Spalte "Format" ein, geben Sie "Property" in die Spalte "Type" ein, und geben Sie "Public" in die Spalte "ContextData" der Tabelle "ModuleConfiguration" ein.

**Private ContextData**

Ein konfigurierbares Mergemodul kann diesen Typ verwenden, um dem Benutzer zu ermöglichen, den Namen einer [privaten Eigenschaft](private-properties.md) für eine Datenbanktabelle im Modul bereitzustellen. Das Merge-Tool ersetzt den Bezeichner der Eigenschaft in den Vorlagen in der Spalte Wert der [Tabelle ModuleSubstitution](modulesubstitution-table.md). Wenn Sie ein konfigurierbares Element dieses Typs angeben möchten, geben Modul Autoren den Namen des konfigurierbaren Elements in die Spalte Name ein, geben Sie "1" in die Spalte "Format" ein, geben Sie "Property" in die Spalte "Type" ein, und geben Sie "private" in die Spalte "ContextData" der Tabelle "ModuleConfiguration" ein.

 

 



