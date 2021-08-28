---
description: In diesem Beispiel kann der Modulverbraucher ein Bearbeitungssteuerelement, das Prüfsummenattribut und das komprimierte Attribut unabhängig konfigurieren.
ms.assetid: f0500856-18d0-45e5-992a-57e01fb2cca5
title: Beispiel für konfigurierbare Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ff3e1567a19afd50a0ae2035893c027398816b535d5edfb233e89021ea9e59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500740"
---
# <a name="configurable-component-example"></a>Beispiel für konfigurierbare Komponenten

In diesem Beispiel ermöglicht es die folgenden ModuleConfiguration- und ModuleSubsuma-Tabellen dem Modulverbraucher, das Password-Attribut für ein Bearbeitungssteuerelement, das Prüfsummenattribut für eine Datei und das komprimierte Attribut für dieselbe Datei unabhängig zu konfigurieren.

[Tabelle "ModuleSubsbor"](modulesubstitution-table.md)



| Tabelle   | Zeile           | Spalte     | Wert                        |
|---------|---------------|------------|------------------------------|
| Control | Dialog1; Bearbeiten1 | Attribute | \[=Kennwort\]                |
| Datei    | Datei1         | Attribute | \[=Checksum \] \[ =Compressed\] |



 

[Tabelle "ModuleConfiguration"](moduleconfiguration-table.md)



| Name       | Format   | Typ | ContextData                              | DefaultValue | Attribute | DisplayName | BESCHREIBUNG |
|------------|----------|------|------------------------------------------|--------------|------------|-------------|-------------|
| Kennwort   | Bitfield |      | 2097152; True=2097152; False=0             | 0            | 0          |             |             |
| Checksum   | Bitfield |      | 1024; Checksum=1024; Keine Prüfsumme=0         | 0            | 0          |             |             |
| Compressed | Bitfield |      | 24576; Compressed=16384; Uncompressed=8192 | 8192         | 0          |             |             |



 

 

 



