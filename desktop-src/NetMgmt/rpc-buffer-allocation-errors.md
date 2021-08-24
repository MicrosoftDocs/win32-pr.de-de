---
title: RPC-Pufferzuordnungsfehler
description: Da die RPC-Laufzeitbibliothek Arbeitsspeicher für Sende- und Empfangspuffer zuteilen, sollte die Funktion RPC-Zuordnungsfehler erwarten.
ms.assetid: be9105df-1183-48d6-8cea-391ca628c8b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d68c484837f1f03bce8a8175ddb343065051e3695eec7c65d8a9de89c15fb5d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745010"
---
# <a name="rpc-buffer-allocation-errors"></a>RPC-Pufferzuordnungsfehler

Da die RPC-Laufzeitbibliothek Arbeitsspeicher für Sende- und Empfangspuffer zuteilen, sollte die Funktion RPC-Zuordnungsfehler erwarten. Bei einem RPC-Zuordnungsfehler wird ein fortsetzungsfähiges Handle ungültig. Dies ist eine Voraussetzung, da wiederverfetzbare Funktionen nicht zurücklädbar sind.

 

 




