---
description: Wenn Sie ermitteln möchten, ob ein-Wert auf einem bestimmten Computer installiert ist, nennen Sie pdhvalidatepath mit dem voll qualifizierten Counter-Pfad. Die Funktion gibt einen Fehler Erfolg zurück, \_ Wenn sich der gegen Computer auf dem angegebenen Computer befindet.
ms.assetid: 5533a8d8-3621-4ce7-984c-c3895adef531
title: Ermitteln, ob sich ein gegen Computer auf einem Computer befindet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 795878e2f9c97989fe924737ec7f8e7f14bdc67c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959765"
---
# <a name="determining-whether-a-counter-is-located-on-a-computer"></a>Ermitteln, ob sich ein gegen Computer auf einem Computer befindet

Wenn Sie ermitteln möchten, ob ein-Wert auf einem bestimmten Computer installiert ist, nennen Sie [**pdhvalidatepath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) mit dem voll qualifizierten Counter-Pfad. Die Funktion gibt einen Fehler Erfolg zurück, \_ Wenn sich der gegen Computer auf dem angegebenen Computer befindet.

[**Pdhvalidatepath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) überprüft den gesamten Pfad. Daher gibt der Rückgabewert an, wenn ein Objekt, eine Instanz oder ein Leistungs Bezeichner im Pfad nicht vorhanden ist. **Pdhvalidatepath** überprüft den angegebenen Leistungswert Pfad in dieser Reihenfolge: Computer, Leistungs Objekt, Instanz und Leistungsdaten.

 

 



