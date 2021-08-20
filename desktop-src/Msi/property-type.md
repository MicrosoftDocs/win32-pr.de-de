---
description: Der Eigenschaftstyp des semantischen Typs ist einer der Schlüsselformattypen. Dieser Typ besteht aus einem Fremdschlüssel in der vom Benutzer bereitgestellten Property-Tabelle.
ms.assetid: 819e4e90-0bc3-41ba-851d-1d4c52b6eeea
title: Eigenschaftstyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6446b5a0ef5f2cf1bc969f531a3b8c35e6990a2ca3eee3c0002e4f62fbf4cea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145333"
---
# <a name="property-type"></a>Eigenschaftstyp

Der Eigenschaftstyp des [semantischen Typs](semantic-types.md) ist einer der [Schlüsselformattypen.](key-format-types.md) Dieser Typ besteht aus einem Fremdschlüssel in der vom Benutzer bereitgestellten [Property-Tabelle.](property-table.md)

Das Mergetool muss einen gültigen Windows [Installer-Bezeichner](identifier.md) für Elemente dieses Typs ersetzen. Mergemod.dll erzwingt diese Einschränkung nicht, und es obliegt dem Mergetool, sicherzustellen, dass der Benutzer einen gültigen Schlüssel in der Property-Tabelle bereitstellt. Die Primärschlüssel der Property-Tabelle sind die Eigenschaftennamen.

NULL ist ein gültiger Wert für diesen Typ, es sei denn, msmConfigItemNonNullable wurde in das Feld Attributes der [ModuleConfiguration-Tabelle](moduleconfiguration-table.md)eingefügt.

Der Eigenschaftstyp kann mit den folgenden Arten von ContextData verwendet werden.

**Null ContextData**

Ein konfigurierbares Mergemodul kann diesen Typ verwenden, damit der Benutzer einen Eigenschaftennamen für eine Datenbanktabelle im Modul angeben kann. Das Mergetool ersetzt den Bezeichner der Eigenschaft in den Vorlagen in der Spalte Wert der [Tabelle ModuleSubsschädigung](modulesubstitution-table.md). Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modulautoren den Namen des konfigurierbaren Elements in die Spalte Name eingeben, "1" in die Spalte Format eingeben, "Property" in die Spalte Typ eingeben und die ContextData-Spalte der [Tabelle ModuleConfiguration](moduleconfiguration-table.md)leer lassen.

**Public ContextData**

Ein konfigurierbares Mergemodul kann diesen Typ verwenden, damit der Benutzer den Namen einer [öffentlichen Eigenschaft](public-properties.md) für eine Datenbanktabelle im Modul angeben kann. Das Mergetool ersetzt den Bezeichner der Eigenschaft in den Vorlagen in der Spalte Wert der [Tabelle ModuleSubsschädigung](modulesubstitution-table.md). Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modulautoren den Namen des konfigurierbaren Elements in die Spalte Name eingeben, "1" in die Spalte Format eingeben, "Property" in die Spalte Typ und "Public" in die ContextData-Spalte der Tabelle ModuleConfiguration eingeben.

**Private ContextData**

Ein konfigurierbares Mergemodul kann diesen Typ verwenden, damit der Benutzer den Namen einer [privaten Eigenschaft](private-properties.md) für eine Datenbanktabelle im Modul angeben kann. Das Mergetool ersetzt den Bezeichner der Eigenschaft in den Vorlagen in der Spalte Wert der [Tabelle ModuleSubsschädigung](modulesubstitution-table.md). Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modulautoren den Namen des konfigurierbaren Elements in die Spalte Name eingeben, "1" in die Spalte Format eingeben, "Property" in die Spalte Type und "Private" in die ContextData-Spalte der Tabelle ModuleConfiguration eingeben.

 

 



