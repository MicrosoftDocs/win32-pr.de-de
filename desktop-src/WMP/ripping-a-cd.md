---
title: Erstellen einer CD
description: Erstellen einer CD
ms.assetid: f5c1b5bf-d616-48cb-8690-e0237c56e402
keywords:
- Windows Media Player,CD-Lässing
- Windows Media Player-Objektmodell,CD-Bebauung
- Objektmodell,CD-Bebauung
- Windows Media Player ActiveX,CD-Steuerung
- ActiveX,CD-Steuerung
- Windows Media Player Mobile ActiveX,CD-Steuerung
- Windows Media Player Mobil, CD-10
- CD-Ing, Informationen
- Verwenden von CDs, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313262bf29f3ee873b546dd639ec7b32c774be476e87f75592041f1bda6a2cdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002530"
---
# <a name="ripping-a-cd"></a>Erstellen einer CD

Es gibt zwei Möglichkeiten, eine CD mithilfe des Steuerelements Windows Media Player zu reißt. Windows Media Player 9 können CDs mithilfe von **IWMPPlayerServices::setTaskPane reißen.** Windows Media Player 11 führt die **IWMPCiererRip-Schnittstelle** für die Benutzeroberfläche von CDs ein. Diese Schnittstelle bietet mehr Funktionalität als **IWMPPlayerServices::setTaskPane,** und es wird empfohlen, **IWMPCiererRip** zu verwenden, sofern verfügbar.

In den folgenden Abschnitten wird beschrieben, wie Sie eine CD mithilfe von Windows Media Player.

-   [Anzippen mithilfe der IWMPCiererRip-Schnittstelle](ripping-by-using-the-iwmpcdromrip-interface.md)
-   [Beschriftung mitHILFE von IWMPPlayerServices::setTaskPane](ripping-by-using-iwmpplayerservices--settaskpane.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Leitfaden zum Player-Steuerelement**](player-control-guide.md)
</dt> </dl>

 

 




