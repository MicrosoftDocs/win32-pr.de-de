---
title: Anzeigen von Flags
description: Verwenden Sie die Ansichts-Flags, um Routing Tabellen Sichten zu steuern.
ms.assetid: 836e3400-0dca-4a21-9a5c-7da357ed72ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5192bf3e1acaa91412d8ae7e06d035e54af1ece6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338216"
---
# <a name="view-flags"></a>Anzeigen von Flags

Verwenden Sie die Ansichts-Flags, um Routing Tabellen Sichten zu steuern.



| Konstante                 | Wert      | BESCHREIBUNG                                                      |
|--------------------------|------------|------------------------------------------------------------------|
| maximale RTM- \_ \_ Adress \_ Größe | 16         | Maximale Adressgröße für eine Adressfamilie.                          |
| maximale RTM- \_ \_ Ansichten          | 32         | Maximale Anzahl von Sichten, die in der Routing Tabelle aktiv sein können. |
| RTM- \_ Ansichts- \_ ID- \_ ucast     | 0          | Gibt eine unicastansicht an.                                        |
| RTM- \_ Ansichts- \_ ID- \_ mcast     | 1          | Gibt eine Multicast Ansicht an.                                      |
| RTM- \_ Ansichts \_ Masken \_ Größe    | 0x20       | Gibt die maximale Anzahl von Sichten an, die konfiguriert werden können.    |
| RTM- \_ Ansicht \_ Maske nicht \_    | 0x00000000 | Gibt Informationen unabhängig von der Sicht zurück.                      |
| RTM- \_ Ansicht \_ maskieren \_     | 0x00000000 | Gibt Ziele aus allen Ansichten zurück. Dies ist der Standardwert.  |
| RTM- \_ Ansichts \_ Maske ( \_ ucast)   | 0x00000001 | Gibt Ziele aus der unicastansicht zurück.                      |
| RTM- \_ Ansicht \_ mask \_ mcast   | 0x00000002 | Gibt Ziele aus der Multicast Ansicht zurück.                    |
| RTM- \_ Ansicht \_ maskieren \_     | 0xFFFFFFFF | Gibt Informationen aus allen Sichten zurück.                              |



 

 

 




