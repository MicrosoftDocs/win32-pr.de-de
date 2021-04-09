---
description: Der Verzeichnistyp des semantischen Typs ist einer der Schlüssel Format Typen, der aus einem Fremdschlüssel in der vom Benutzer bereitgestellten Verzeichnis Tabelle besteht.
ms.assetid: b5a0ed38-1dda-4c33-9429-0cbe87e13aef
title: Verzeichnistyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e3ba336dd5de7cd45ef9215f0397ba51ce544d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866336"
---
# <a name="directory-type"></a>Verzeichnistyp

Der Verzeichnistyp des [semantischen Typs](semantic-types.md) ist einer der [Schlüssel Format Typen](key-format-types.md), der aus einem Fremdschlüssel in der vom Benutzer bereitgestellten [Verzeichnis Tabelle](directory-table.md) besteht.

Das Merge-Tool muss einen gültigen Windows Installer [Bezeichner](identifier.md) für Elemente dieses Typs ersetzen. Mergemod.dll erzwingt diese Einschränkung nicht, und es liegt an dem Merge-Tool, sicherzustellen, dass der Benutzer einen gültigen Schlüssel für die Verzeichnis Tabelle bereitstellt.

Ein konfigurierbares Element des Verzeichnis Typs sollte nur das Zielverzeichnis der Installation ändern und das Quell Abbild nicht ändern. Ein konfigurierbares Element dieses Typs sollte daher nur Fremdschlüssel in der Verzeichnis Tabelle ändern und die Verzeichnis Tabelle nicht direkt ändern.

Da die Verzeichnis \_ Spalte der [Komponenten Tabelle](component-table.md) nicht auf NULL festgelegt werden kann, ist NULL ein ungültiger Wert für ein konfigurierbares Element dieses Typs, auch wenn die msmconfigitemnonable-Eigenschaft in der Spalte Attribute nicht festgelegt ist.

Der Verzeichnistyp kann mit zwei Arten von ContextData verwendet werden.

**Isolationdirectory ContextData**

Ein konfigurierbares Mergemodul kann diesen Typ verwenden, um dem Benutzer zu ermöglichen, ein Zielverzeichnis für Dateien im Modul bereitzustellen. Das Merge-Tool ersetzt den Bezeichner des Verzeichnisses in den Vorlagen in der Value-Spalte der [ModuleSubstitution-Tabelle](modulesubstitution-table.md). Wenn Sie ein konfigurierbares Element dieses Typs angeben möchten, geben Modul Autoren den Namen des Verzeichnisses in die Spalte Name ein, geben Sie "1" in die Spalte "Format" ein, geben Sie "Directory" in die Spalte "Type" ein, und geben Sie "isolationdirectory" in die Spalte "ContextData" der [Tabelle "ModuleConfiguration](moduleconfiguration-table.md)" ein.

**ShortcutLocation ContextData**

Ein konfigurierbares Mergemodul kann diesen Typ verwenden, um dem Benutzer zu ermöglichen, ein Zielverzeichnis für Verknüpfungen im Modul bereitzustellen. Das Merge-Tool ersetzt den Bezeichner der Verknüpfung in den Vorlagen in der Value-Spalte der [ModuleSubstitution-Tabelle](modulesubstitution-table.md). Wenn Sie ein konfigurierbares Element dieses Typs angeben möchten, geben Modul Autoren den Namen des Verzeichnisses in die Spalte Name ein, geben Sie "1" in die Spalte "Format" ein, geben Sie "Directory" in die Spalte "Type" ein, und geben Sie "ShortcutLocation" in die Spalte "ContextData" der [Tabelle "ModuleConfiguration](moduleconfiguration-table.md)" ein.

 

 



