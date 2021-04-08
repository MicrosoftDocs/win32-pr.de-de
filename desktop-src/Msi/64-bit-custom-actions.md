---
description: Bei 64-Bit-Betriebssystemen können Windows Installer benutzerdefinierte Aktionen aufzurufen, die für 32-Bit-oder 64-Bit-Systeme kompiliert wurden.
ms.assetid: fc370ab4-93f3-4e1e-9468-3454d4fee0be
title: benutzerdefinierte 64-Bit-Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77fcd804152abd010f985aab3b92c0de73a2744f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756259"
---
# <a name="64-bit-custom-actions"></a>benutzerdefinierte 64-Bit-Aktionen

Bei 64-Bit-Betriebssystemen können Windows Installer benutzerdefinierte Aktionen aufzurufen, die für 32-Bit-oder 64-Bit-Systeme kompiliert wurden.

Eine benutzerdefinierte 64-Bit-Aktion, die auf [Skripts](scripts.md) basiert, muss explizit als 64 eine benutzerdefinierte 32-Bit-Aktion gekennzeichnet werden, indem das **msidbCustomActionType64BitScript** -Bit dem numerischen Typ benutzerdefinierte Aktionen in der Type-Spalte der [CustomAction-Tabelle](customaction-table.md)hinzugefügt wird.



| Konstante                             | Hexadezimal | Decimal | Bedeutung                                                           |
|--------------------------------------|-------------|---------|-------------------------------------------------------------------|
| **msidbCustomActionType64BitScript** | 0x0001000   | 4096    | Dabei handelt es sich um eine in [Skripts](scripts.md)geschriebene benutzerdefinierte 64-Bit-Aktion. |



 

Benutzerdefinierte Aktionen, die auf [ausführbaren Dateien](executable-files.md) oder [Dynamic Link-Bibliotheken](dynamic-link-libraries.md) basieren, die für ein 64-Bit-Betriebssystem ausgeführt wurden, müssen dieses zusätzliche Bit nicht in die Spalte Type der Tabelle CustomAction einschließen.

 

 



