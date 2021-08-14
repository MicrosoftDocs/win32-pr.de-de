---
title: Ändern der aktuellen Position
description: Ändern der aktuellen Position
ms.assetid: f8c4b9b5-c5fb-4292-8418-41650dcd65c0
keywords:
- MCI_SEEK Befehlsmeldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14f062fc93a89f54fb89a30b6ac3e53c8d6240cfc28b661a25da48a0b1b2fbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941288"
---
# <a name="changing-the-current-position"></a>Ändern der aktuellen Position

Um die aktuelle Position in einem Geräteelement zu ändern, verwenden Sie die [**MCI \_ SEEK-Befehlsmeldung**](mci-seek.md) zusammen mit dem MCI TO-Flag und der \_ [**MCI SEEK \_ \_ PARMS-Struktur.**](mci-seek-parms.md) Wenn Sie das **dwTo-Member** verwenden, um eine Suchposition mit MCI SEEK anzugeben, sollten Sie das Zeitformat abfragen und bei Bedarf \_ festlegen.

Zusätzlich zur Angabe einer Position mit dem **dwTo-Member** können Sie die MCI SEEK TO START- oder \_ \_ \_ MCI SEEK TO END-Flags für den \_ \_ \_ *dwParam1-Parameter* der [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) angeben, um die Anfangs- und Endpositionen des Geräteelements zu finden. Wenn Sie eines dieser Flags verwenden, geben Sie das MCI \_ TO-Flag nicht an.

 

 