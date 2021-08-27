---
title: Anzeigen von Flags
description: Verwenden Sie die Ansichtsflags, um Routingtabellenansichten zu steuern.
ms.assetid: 836e3400-0dca-4a21-9a5c-7da357ed72ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ae9763587cf7972aab3ca9880d5ad26350c3161955c17940484cc1cbd801bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024950"
---
# <a name="view-flags"></a>Anzeigen von Flags

Verwenden Sie die Ansichtsflags, um Routingtabellenansichten zu steuern.



| Konstante                 | Wert      | BESCHREIBUNG                                                      |
|--------------------------|------------|------------------------------------------------------------------|
| RTM \_ MAX \_ ADDRESS \_ SIZE | 16         | Maximale Adressgröße für eine Adressfamilie.                          |
| RTM \_ MAX \_ VIEWS          | 32         | Maximale Anzahl von Sichten, die in der Routingtabelle aktiv sein können. |
| RTM \_ VIEW \_ ID \_ UCAST     | 0          | Gibt eine Unicastansicht an.                                        |
| RTM \_ VIEW \_ ID \_ MCAST     | 1          | Gibt eine Multicastansicht an.                                      |
| GRÖßE DER \_ RTM-ANSICHTSMASKE \_ \_    | 0x20       | Gibt die maximale Anzahl von Ansichten an, die konfiguriert werden können.    |
| RTM \_ VIEW \_ MASK \_ NONE    | 0x00000000 | Gibt Informationen unabhängig von der Sicht zurück.                      |
| RTM \_ VIEW \_ MASK \_ ANY     | 0x00000000 | Gibt Ziele aus allen Ansichten zurück. Dies ist der Standardwert.  |
| RTM \_ VIEW \_ MASK \_ UCAST   | 0x00000001 | Gibt Ziele aus der Unicastansicht zurück.                      |
| RTM \_ VIEW \_ MASK \_ MCAST   | 0x00000002 | Gibt Ziele aus der Multicastansicht zurück.                    |
| RTM \_ VIEW \_ MASK \_ ALL     | 0xFFFFFFFF | Gibt Informationen aus allen Ansichten zurück.                              |



 

 

 




