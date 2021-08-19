---
title: Schließen eines Geräts
description: Schließen eines Geräts
ms.assetid: eef40f23-2c58-4deb-a6f0-3563d9c30d10
keywords:
- MCI_CLOSE Befehl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29f81ddaf42ef5509b55271159b8e36ac56584b92734a6b04e5b555041596530
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498080"
---
# <a name="closing-a-device"></a>Schließen eines Geräts

Der Befehl [**close**](close.md) ([**MCI \_ CLOSE**](mci-close.md)) gibt den Zugriff auf ein Gerät oder eine Datei frei. MCI gibt ein Gerät frei, wenn es von allen Aufgaben, die ein Gerät verwenden, geschlossen wurde. Um MCI bei der Verwaltung der Geräte zu unterstützen, muss Ihre Anwendung jedes Gerät oder jede Datei schließen, wenn die Verwendung abgeschlossen ist.

Wenn Sie ein externes MCI-Gerät schließen, das sein eigenes Medium anstelle von Dateien (z. B. CD-Audio) verwendet, verlässt der Treiber das Gerät in seinem aktuellen Betriebsmodus. Wenn Sie also ein cd-Audiogerät schließen, das wiedergegeben wird, obwohl der Gerätetreiber aus dem Arbeitsspeicher freigegeben wird, wird das CD-Audiogerät weiterhin wiedergegeben, bis es das Ende seines Inhalts erreicht.

> [!Note]  
> Das Schließen einer Anwendung mit geöffneten MCI-Geräten kann verhindern, dass andere Anwendungen diese Geräte verwenden, bis Windows neu gestartet wird.

 

 

 




