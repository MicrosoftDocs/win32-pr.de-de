---
description: Der Verzeichnistyp des semantischen Typs ist einer der Schlüsselformattypen, der aus einem Fremdschlüssel in der vom Benutzer bereitgestellten Directory-Tabelle besteht.
ms.assetid: b5a0ed38-1dda-4c33-9429-0cbe87e13aef
title: Verzeichnistyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c784ea91ceb9baaeb2c97883cace0266a146d80634ec07f5e25f0b01ac057c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119251800"
---
# <a name="directory-type"></a>Verzeichnistyp

Der Verzeichnistyp des [semantischen Typs](semantic-types.md) ist einer der [Schlüsselformattypen,](key-format-types.md)der aus einem Fremdschlüssel in der vom Benutzer bereitgestellten [Directory-Tabelle](directory-table.md) besteht.

Das Mergetool muss einen gültigen Windows [Installer-Bezeichner](identifier.md) für Elemente dieses Typs ersetzen. Mergemod.dll diese Einschränkung nicht erzwingt, und es liegt in der Rolle des Mergetools, sicherzustellen, dass der Benutzer einen gültigen Schlüssel in der Directory-Tabelle zur Verfügung stellt.

Ein konfigurierbares Element des Verzeichnistyps sollte nur das Zielverzeichnis der Installation und nicht das Quellimage ändern. Ein konfigurierbares Element dieses Typs sollte daher nur Fremdschlüssel in der Directory-Tabelle ändern und die Directory-Tabelle nicht direkt ändern.

Da die Directory -Spalte der Component-Tabelle keine NULL-Werte zulässig ist, ist NULL ein ungültiger Wert für ein konfigurierbares Element dieses Typs, auch wenn \_ msmConfigItemNonNullable nicht in der Attributes -Spalte festgelegt ist. [](component-table.md)

Der Verzeichnistyp kann mit zwei Arten von ContextData verwendet werden.

**IsolationDirectory ContextData**

Ein konfigurierbares Mergemodul kann diesen Typ verwenden, damit der Benutzer ein Zielverzeichnis für Dateien im Modul bereitstellen kann. Das Mergetool ersetzt den Bezeichner des Verzeichnisses in die Vorlagen in der Spalte Wert der [ModuleSubskennungstabelle.](modulesubstitution-table.md) Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modulautoren den Namen des Verzeichnisses in die Spalte Name eingeben, "1" in die Spalte Format eingeben, "Directory" in die Spalte Typ eingeben und "IsolationDirectory" in die ContextData -Spalte der [ModuleConfiguration-Tabelle eingeben.](moduleconfiguration-table.md)

**ShortcutLocation ContextData**

Ein konfigurierbares Mergemodul kann diesen Typ verwenden, damit der Benutzer ein Zielverzeichnis für Verknüpfungen im Modul bereitstellen kann. Das Mergetool ersetzt den Bezeichner der Verknüpfung in die Vorlagen in der Spalte Wert der [ModuleSubskennungstabelle.](modulesubstitution-table.md) Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modulautoren den Namen des Verzeichnisses in die Spalte Name eingeben, "1" in die Spalte Format eingeben, "Directory" in die Spalte Typ eingeben und "ShortcutLocation" in die Spalte ContextData der [ModuleConfiguration-Tabelle eingeben.](moduleconfiguration-table.md)

 

 



