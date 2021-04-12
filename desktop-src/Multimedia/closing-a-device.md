---
title: Schließen eines Geräts
description: Schließen eines Geräts
ms.assetid: eef40f23-2c58-4deb-a6f0-3563d9c30d10
keywords:
- MCI_CLOSE-Befehl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 824d156baa72ee404f29ae490d4d9816078f4d15
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388009"
---
# <a name="closing-a-device"></a>Schließen eines Geräts

Der [**Close**](close.md) ([**MCI \_ Close**](mci-close.md))-Befehl gibt den Zugriff auf ein Gerät oder eine Datei frei. MCI gibt ein Gerät frei, wenn es von allen Tasks, die ein Gerät verwenden, geschlossen wurde. Um MCI bei der Verwaltung der Geräte zu unterstützen, muss die Anwendung jedes Gerät oder jede Datei schließen, wenn Sie Sie nicht mehr verwenden.

Wenn Sie ein externes MCI-Gerät schließen, das anstelle von Dateien (z. b. CD-Audiodatei) ein eigenes Medium verwendet, verlässt der Treiber das Gerät im aktuellen Betriebsmodus. Wenn Sie also ein CD-Audiogerät schließen, das abgespielt wird, auch wenn der Gerätetreiber aus dem Arbeitsspeicher freigegeben wird, wird das CD-Audiogerät weiterhin abgespielt, bis das Ende seines Inhalts erreicht ist.

> [!Note]  
> Wenn Sie eine Anwendung mit geöffneten MCI-Geräten schließen, können Sie verhindern, dass andere Anwendungen diese Geräte verwenden, bis Windows neu gestartet wird.

 

 

 




