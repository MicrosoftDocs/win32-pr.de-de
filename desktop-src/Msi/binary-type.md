---
description: Der binäre Typ des semantischen Typs ist einer der Schlüssel Format Typen. Dieser Typ besteht aus einem Schlüssel in der binären Tabelle, die vom Benutzer bereitgestellt wird.
ms.assetid: b6a25100-9f3e-4207-b56f-0c27ee16f188
title: Binary-Typ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fda0711b53f865bbd844514ed2429d97d91e07a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528859"
---
# <a name="binary-type"></a>Binary-Typ

Der binäre Typ des [semantischen Typs](semantic-types.md) ist einer der [Schlüssel Format Typen](key-format-types.md). Dieser Typ besteht aus einem Schlüssel in der [binären Tabelle](binary-table.md) , die vom Benutzer bereitgestellt wird.

Das Merge-Tool muss einen gültigen Windows Installer [Bezeichner](identifier.md) für Elemente dieses Typs ersetzen. Mergemod.dll erzwingt diese Einschränkung nicht, und es liegt an dem Merge-Tool, sicherzustellen, dass der Benutzer einen gültigen Schlüssel für die binäre Tabelle bereitstellt.

NULL ist ein gültiger Wert für diesen Typ, es sei denn, der msmconfigitemnonable-Wert ist im Feld Attribute der [Tabelle ModuleConfiguration](moduleconfiguration-table.md)enthalten.

Der binäre Typ kann mit den folgenden Arten von ContextData verwendet werden.

**Bitmap ContextData**

Ein konfigurierbares Mergemodul kann diesen Typ verwenden, um dem Benutzer zu ermöglichen, einen Fremdschlüssel für eine Zeile in der binären Tabelle bereitzustellen, die ein Bitmapbild enthält. Mergmod.dll garantiert keine bestimmte Größe oder Art von Bitmap, und das Mergetool muss sicherstellen, dass die Daten ein gültiges Image sind. Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modul Autoren den Namen des konfigurierbaren Elements in die Spalte "Name" eingeben, "1" in die Spalte "Format" eingeben, "Binary" in die Spalte "Type" eingeben und "Bitmap" in die Spalte "ContextData" der Tabelle "ModuleConfiguration" eingeben.

**Symbol "ContextData"**

Ein konfigurierbares Mergemodul kann diesen Typ verwenden, um dem Benutzer zu ermöglichen, einen Fremdschlüssel für eine Zeile in der binären Tabelle bereitzustellen, die ein Symbolbild enthält. Mergmod.dll garantiert keine bestimmte Größe oder Art von Symbol, und das Mergetool muss sicherstellen, dass die Daten ein gültiges Image sind. Wenn Sie ein konfigurierbares Element dieses Typs angeben möchten, geben Modul Autoren den Namen des konfigurierbaren Elements in die Spalte Name ein, geben Sie "1" in die Spalte "Format" ein, geben Sie "Binary" in die Spalte "Type" ein, und geben Sie "Icon" in die Spalte "ContextData" der Tabelle "ModuleConfiguration" ein. Dieser Typ ist nicht für die Verwendung in einer Ankündigungs Tabelle geeignet.

**"ContextData" für exe**

Ein konfigurierbares Mergemodul kann diesen Typ verwenden, um dem Benutzer zu ermöglichen, einen Fremdschlüssel für eine Zeile in der binären Tabelle bereitzustellen, die ein ausführbares 32-Bit-Image enthält. Mergmod.dll überprüft nicht, ob die Daten gültig sind, und das Mergetool muss sicherstellen, dass die Daten eine gültige PE-Datei sind. Wenn Sie ein konfigurierbares Element dieses Typs angeben möchten, geben Modul Autoren den Namen des konfigurierbaren Elements in die Spalte Name ein, geben Sie "1" in die Spalte "Format" ein, geben Sie "Binary" in die Spalte "Type" ein, und geben Sie "exe" in die Spalte "ContextData" der Tabelle "ModuleConfiguration" ein.

**EXE64 ContextData**

Ein konfigurierbares Mergemodul kann diesen Typ verwenden, um dem Benutzer zu ermöglichen, einen Fremdschlüssel für eine Zeile in der binären Tabelle bereitzustellen, die entweder ein ausführbares 32-Bit-oder 64-Bit-Image enthält. Mergmod.dll überprüft nicht, ob die Daten gültig sind, und das Mergetool muss sicherstellen, dass die Daten eine gültige PE-Datei sind. Wenn Sie ein konfigurierbares Element dieses Typs angeben möchten, geben Modul Autoren den Namen des konfigurierbaren Elements in die Spalte Name ein, geben Sie "1" in die Spalte "Format" ein, geben Sie "Binary" in die Spalte "Type" ein, und geben Sie "EXE64" in die Spalte "ContextData" der Tabelle "ModuleConfiguration" ein.

 

 



