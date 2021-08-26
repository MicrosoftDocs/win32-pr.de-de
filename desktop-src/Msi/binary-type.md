---
description: Der binäre Typ des semantischen Typs ist einer der Schlüsselformattypen. Dieser Typ besteht aus einem Schlüssel in der vom Benutzer bereitgestellten Binärtabelle.
ms.assetid: b6a25100-9f3e-4207-b56f-0c27ee16f188
title: Binärtyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8412d63891f3028c1ef2beb8fa0e6a17c4a35c33df182cbd9f1059a593c50915
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105370"
---
# <a name="binary-type"></a>Binärtyp

Der binäre Typ des [semantischen Typs](semantic-types.md) ist einer der [Schlüsselformattypen.](key-format-types.md) Dieser Typ besteht aus einem Schlüssel in der vom Benutzer [bereitgestellten Binärtabelle.](binary-table.md)

Das Mergetool muss einen gültigen Windows [Installer-Bezeichner](identifier.md) für Elemente dieses Typs ersetzen. Mergemod.dll erzwingt diese Einschränkung nicht, und es obliegt dem Mergetool, sicherzustellen, dass der Benutzer einen gültigen Schlüssel in der Binärtabelle bereitstellt.

NULL ist ein gültiger Wert für diesen Typ, es sei denn, msmConfigItemNonNullable wurde in das Feld Attributes der [ModuleConfiguration-Tabelle](moduleconfiguration-table.md)eingefügt.

Der Binärtyp kann mit den folgenden Arten von ContextData verwendet werden.

**Bitmap ContextData**

Ein konfigurierbares Mergemodul kann diesen Typ verwenden, um dem Benutzer das Bereitstellen eines Fremdschlüssels für eine Zeile in der Binärtabelle zu ermöglichen, die ein Bitmapbild enthält. Mergmod.dll garantiert keine bestimmte Größe oder einen bestimmten Bitmaptyp, und das Mergetool muss sicherstellen, dass die Daten ein gültiges Bild sind. Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modulautoren den Namen des konfigurierbaren Elements in die Spalte Name eingeben, "1" in die Spalte Format eingeben, "Binary" in die Spalte Typ eingeben und "Bitmap" in die Spalte ContextData der Tabelle ModuleConfiguration eingeben.

**Symbol ContextData**

Ein konfigurierbares Mergemodul kann diesen Typ verwenden, damit der Benutzer einen Fremdschlüssel für eine Zeile in der Binärtabelle bereitstellen kann, die ein Symbolbild enthält. Mergmod.dll garantiert keine bestimmte Größe oder Art von Symbol, und das Mergetool muss sicherstellen, dass die Daten ein gültiges Bild sind. Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modulautoren den Namen des konfigurierbaren Elements in die Spalte Name eingeben, "1" in die Spalte Format eingeben, "Binary" in die Spalte Typ eingeben und "Icon" in die ContextData-Spalte der Tabelle ModuleConfiguration eingeben. Dieser Typ eignet sich nicht für die Verwendung in einer Ankündigungstabelle.

**EXE ContextData**

Ein konfigurierbares Mergemodul kann diesen Typ verwenden, um dem Benutzer das Bereitstellen eines Fremdschlüssels für eine Zeile in der Binärtabelle zu ermöglichen, die ein ausführbares 32-Bit-Image enthält. Mergmod.dll überprüft nicht, ob die Daten gültig sind, und das Mergetool muss sicherstellen, dass es sich bei den Daten um eine gültige PE-Datei handelt. Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modulautoren den Namen des konfigurierbaren Elements in die Spalte Name eingeben, "1" in die Spalte Format eingeben, "Binary" in die Spalte Type und "EXE" in die ContextData-Spalte der Tabelle ModuleConfiguration eingeben.

**EXE64 ContextData**

Ein konfigurierbares Mergemodul kann diesen Typ verwenden, um dem Benutzer das Bereitstellen eines Fremdschlüssels für eine Zeile in der Binärtabelle zu ermöglichen, die entweder ein ausführbares 32-Bit- oder 64-Bit-Image enthält. Mergmod.dll überprüft nicht, ob die Daten gültig sind, und das Mergetool muss sicherstellen, dass es sich bei den Daten um eine gültige PE-Datei handelt. Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modulautoren den Namen des konfigurierbaren Elements in die Spalte Name eingeben, "1" in die Spalte Format eingeben, "Binary" in die Spalte Typ eingeben und "EXE64" in die ContextData-Spalte der Tabelle ModuleConfiguration eingeben.

 

 



