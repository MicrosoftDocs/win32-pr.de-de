---
description: Der Parametertyp des semantischen Typs ist einer der Schlüssel Format Typen. Dieser Typ besteht aus einem Fremdschlüssel in der vom Benutzer bereitgestellten Dialog Feld Tabelle.
ms.assetid: 3656684a-de95-45e1-9c78-5c1cc8ca879a
title: Dialogtyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39ed04dece5702d232f252caa7c0ee02e7576246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373137"
---
# <a name="dialog-type"></a>Dialogtyp

Der Parametertyp des [semantischen Typs](semantic-types.md) ist einer der [Schlüssel Format Typen](key-format-types.md). Dieser Typ besteht aus einem Fremdschlüssel in der vom Benutzer bereitgestellten [Dialog Feld Tabelle](dialog-table.md) .

Das Merge-Tool muss einen gültigen Windows Installer [Bezeichner](identifier.md) für Elemente dieses Typs ersetzen. Mergemod.dll erzwingt diese Einschränkung nicht, und es liegt an dem Merge-Tool, sicherzustellen, dass der Benutzer einen gültigen Schlüssel in der Dialog Tabelle bereitstellt.

NULL ist ein gültiger Wert für diesen Typ, es sei denn, der msmconfigitemnonable-Wert ist im Feld Attribute der [Tabelle ModuleConfiguration](moduleconfiguration-table.md)enthalten.

Der Dialog Typ kann mit den folgenden Arten von ContextData verwendet werden.

**Dialognext ContextData**

Ein konfigurierbares Mergemodul kann diesen Typ verwenden, damit der Benutzer einen Fremdschlüssel in der Dialog Tabelle bereitstellen kann. Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modul Autoren den Namen des konfigurierbaren Elements in die Spalte "Name" eingeben, "1" in die Spalte "Format" eingeben, "Dialog" in die Spalte "Typ" eingeben und "dialognext" in die Spalte "ContextData" der [Tabelle "ModuleConfiguration](moduleconfiguration-table.md)" eingeben.

**Dialogprev ContextData**

Ein konfigurierbares Mergemodul kann diesen Typ verwenden, damit der Benutzer einen Fremdschlüssel in der Dialog Tabelle bereitstellen kann. Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modul Autoren den Namen des konfigurierbaren Elements in die Spalte "Name" eingeben, "1" in die Spalte "Format" eingeben, "Dialog" in die Spalte "Typ" eingeben und "dialogprev" in die Spalte "ContextData" der Tabelle "ModuleConfiguration" eingeben.

 

 



