---
description: Um zu ermitteln, ob ein Indikator auf einem bestimmten Computer installiert ist, rufen Sie PdhValidatePath mit dem vollqualifizierten Indikatorpfad auf. Die Funktion gibt ERROR \_ SUCCESS zurück, wenn sich der Leistungsindikator auf dem angegebenen Computer befindet.
ms.assetid: 5533a8d8-3621-4ce7-984c-c3895adef531
title: Bestimmen, ob sich ein Indikator auf einem Computer befindet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2cc6672125f961fc2759d264caa6c33ab68f46347c915e82d1666f667692fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061198"
---
# <a name="determining-whether-a-counter-is-located-on-a-computer"></a>Bestimmen, ob sich ein Indikator auf einem Computer befindet

Um zu ermitteln, ob ein Indikator auf einem bestimmten Computer installiert ist, rufen Sie [**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) mit dem vollqualifizierten Indikatorpfad auf. Die Funktion gibt ERROR \_ SUCCESS zurück, wenn sich der Leistungsindikator auf dem angegebenen Computer befindet.

[**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) überprüft den gesamten Pfad. Wenn also ein Objekt, eine Instanz oder ein Indikator im Pfad nicht vorhanden ist, gibt der Rückgabewert dies an. **PdhValidatePath** überprüft den angegebenen Indikatorpfad in dieser Reihenfolge: Computer, Leistungsobjekt, Instanz und Leistungsindikator.

 

 



