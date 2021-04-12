---
title: Ändern der aktuellen Position
description: Ändern der aktuellen Position
ms.assetid: f8c4b9b5-c5fb-4292-8418-41650dcd65c0
keywords:
- MCI_SEEK Befehls Meldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235dc2639d7d9fc01f94aff700ae9e0ebf1dcbe2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390327"
---
# <a name="changing-the-current-position"></a>Ändern der aktuellen Position

Wenn Sie die aktuelle Position in einem Geräte Element ändern möchten, verwenden Sie die [**MCI \_ Seek**](mci-seek.md) -Befehls Meldung zusammen mit der MCI \_ -Flag und der [**MCI- \_ \_ suchparameterstruktur**](mci-seek-parms.md) . Wenn Sie den **dwto** -Member verwenden, um eine Suchposition mit MCI \_ Seek anzugeben, sollten Sie das Zeitformat Abfragen und ggf. festlegen.

Zusätzlich zur Angabe einer Position mit dem **dwto** -Member können Sie die \_ zu Start enden MCI-Such \_ \_ -oder MCI- \_ \_ \_ Suchflags für den *dwParam1* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion angeben, um die Anfangs-und Endpositionen des Device-Elements zu ermitteln. Wenn Sie eines dieser Flags verwenden, geben Sie nicht den zu flagenden MCI-Wert \_ an.

 

 