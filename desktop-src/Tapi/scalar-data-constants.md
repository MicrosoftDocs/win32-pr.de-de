---
description: Für erweiterbare skalare Datenkonstanten kann ein Dienstanbieteranbieter neue Werte in einem angegebenen Bereich definieren.
ms.assetid: 62280b71-9bec-4a9d-abd2-d3e1c2cee43f
title: Skalare Datenkonstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 815288ca4a22da741e5b98257ae50732f818b466404a95712ee74756785fd699
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773310"
---
# <a name="scalar-data-constants"></a>Skalare Datenkonstanten

Für erweiterbare skalare Datenkonstanten kann ein Dienstanbieteranbieter neue Werte in einem angegebenen Bereich definieren. Da die meisten Datenkonstanten **DWORD-S** sind, ist der Bereich 0x00000000 über 0x7FFFFFFF in der Regel für allgemeine zukünftige Erweiterungen reserviert, während 0x80000000 über 0xFFFFFFFF für anbieterspezifische Erweiterungen verfügbar ist. Es wird davon ausgegangen, dass ein Anbieter Werte definiert, die natürliche Erweiterungen der von der API definierten Datentypen sind.

 

 



