---
description: Für erweiterbare Bitflag-Daten Konstanten kann ein Anbieter von Dienstanbietern neue Werte für angegebene Bits definieren.
ms.assetid: bf3ca2b0-a9fb-4e63-87de-6d5cbe5cd746
title: Daten Konstanten Bit-Flag
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238627505bf414ed0ab94ff2f5c35197705c91d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368222"
---
# <a name="bit-flag-data-constants"></a>Daten Konstanten Bit-Flag

Für erweiterbare Bitflag-Daten Konstanten kann ein Anbieter von Dienstanbietern neue Werte für angegebene Bits definieren. Da die meisten bitflagkonstanten **DWORD** s sind, ist eine bestimmte Anzahl von niedrigeren Bits in der Regel für allgemeine Erweiterungen reserviert, während die restlichen oberen Bits für herstellerspezifische Erweiterungen verfügbar sind. Allgemeine Bitflags werden aus Bit 0 (null) zugewiesen, und herstellerspezifische Erweiterungen sollten von Bit 31 nach unten zugewiesen werden. Dieses Schema bietet maximale Flexibilität beim Zuweisen von Bitpositionen zu allgemeinen Erweiterungen, im Gegensatz zu herstellerspezifischen Erweiterungen. Es wird erwartet, dass ein Anbieter neue Werte definiert, bei denen es sich um natürliche Erweiterungen der von der API definierten Bitflags handelt.

Erweiterbare Datenstrukturen verfügen über ein Feld mit variabler Größe, das für die gerätespezifische Verwendung reserviert ist. Da die Größe des Felds variabel ist, entscheidet der Dienstanbieter die Menge an Informationen und die Interpretation des Felds. Ein Anbieter, der ein Geräte spezifisches Feld definiert, wird davon ausgegangen, dass diese natürlichen Erweiterungen der ursprünglichen Datenstruktur durch die API definiert werden.

 

 



