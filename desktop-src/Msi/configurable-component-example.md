---
description: In diesem Beispiel kann der modulconsumer ein Bearbeitungs Steuerelement, das Prüfsumme-Attribut und das komprimierte Attribut unabhängig konfigurieren.
ms.assetid: f0500856-18d0-45e5-992a-57e01fb2cca5
title: Beispiel für konfigurierbare Komponente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 971b2a7c442acb96d7ba00a444c8c3a038c339f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350489"
---
# <a name="configurable-component-example"></a>Beispiel für konfigurierbare Komponente

In diesem Beispiel kann der modulconsumer mithilfe der folgenden ModuleConfiguration-und ModuleSubstitution-Tabellen das Kenn Wort Attribut für ein Bearbeitungs Steuerelement, das Prüfsumme-Attribut für eine Datei und das komprimierte Attribut für dieselbe Datei unabhängig konfigurieren.

[ModuleSubstitution-Tabelle](modulesubstitution-table.md)



| Tabelle   | Zeile           | Spalte     | Wert                        |
|---------|---------------|------------|------------------------------|
| Control | Dialog1; Edit1 | Attribute | \[= Kennwort\]                |
| File    | Datei1         | Attribute | \[= Prüfsumme \] \[ = komprimiert\] |



 

[ModuleConfiguration-Tabelle](moduleconfiguration-table.md)



| Name       | Format   | type | ContextData                              | DefaultValue | Attribute | DisplayName | BESCHREIBUNG |
|------------|----------|------|------------------------------------------|--------------|------------|-------------|-------------|
| Kennwort   | Bitfeld |      | 2097152; True = 2097152; False = 0             | 0            | 0          |             |             |
| Checksum   | Bitfeld |      | 1024; Prüfsumme = 1024; Keine Prüfsumme = 0         | 0            | 0          |             |             |
| Compressed | Bitfeld |      | 24576; Komprimiert = 16384; Unkomprimiert = 8192 | 8192         | 0          |             |             |



 

 

 



