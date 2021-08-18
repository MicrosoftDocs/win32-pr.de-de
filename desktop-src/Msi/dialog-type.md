---
description: Der Dialogtyp des semantischen Typs ist einer der Schlüsselformattypen. Dieser Typ besteht aus einem Fremdschlüssel in der vom Benutzer bereitgestellten Dialogtabelle.
ms.assetid: 3656684a-de95-45e1-9c78-5c1cc8ca879a
title: Dialogtyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f945b499cfab5ca8b3bf85180c16d9be88f4093b258513a11b5059874cb403
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764020"
---
# <a name="dialog-type"></a>Dialogtyp

Der Dialogtyp des [semantischen Typs](semantic-types.md) ist einer der [Schlüsselformattypen.](key-format-types.md) Dieser Typ besteht aus einem Fremdschlüssel in der vom Benutzer bereitgestellten [Dialogtabelle.](dialog-table.md)

Das Mergetool muss einen gültigen Windows [Installer-Bezeichner](identifier.md) für Elemente dieses Typs ersetzen. Mergemod.dll erzwingt diese Einschränkung nicht, und das Mergetool muss sicherstellen, dass der Benutzer einen gültigen Schlüssel in der Tabelle Dialog bereitstellt.

NULL ist ein gültiger Wert für diesen Typ, es sei denn, msmConfigItemNonNullable wurde in das Feld Attributes der [ModuleConfiguration-Tabelle](moduleconfiguration-table.md)eingefügt.

Der Dialogtyp kann mit den folgenden Arten von ContextData verwendet werden.

**DialogNext ContextData**

Ein konfigurierbares Mergemodul kann diesen Typ verwenden, um dem Benutzer das Bereitstellen eines Fremdschlüssels in der Dialogtabelle zu ermöglichen. Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modulautoren den Namen des konfigurierbaren Elements in die Spalte Name eingeben, "1" in die Spalte Format eingeben, "Dialog" in die Spalte Typ eingeben und "DialogNext" in die ContextData-Spalte der [Tabelle ModuleConfiguration](moduleconfiguration-table.md)eingeben.

**DialogPrev ContextData**

Ein konfigurierbares Mergemodul kann diesen Typ verwenden, um dem Benutzer das Bereitstellen eines Fremdschlüssels in der Dialogtabelle zu ermöglichen. Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modulautoren den Namen des konfigurierbaren Elements in die Spalte Name eingeben, "1" in die Spalte Format eingeben, "Dialog" in die Spalte Typ eingeben und "DialogPrev" in die Spalte ContextData der Tabelle ModuleConfiguration eingeben.

 

 



