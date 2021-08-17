---
title: Unterschiede zwischen den Objektmodellen
description: Unterschiede zwischen den Objektmodellen
ms.assetid: a6d2a2d5-2892-461a-aa6d-7e11b504b2af
keywords:
- Windows Media Player,Objektmodell
- Windows Media Player-Objektmodell, Versionsunterschiede
- Objektmodell, Versionsunterschiede
- Windows Media Player ActiveX,Versionsunterschiede
- ActiveX,Versionsunterschiede
- Windows Media Player Mobile ActiveX,Versionsunterschiede
- Windows Media Player Mobil, Objektmodell
- Migrationshandbuch, Versionsunterschiede
- Versionen von Windows Media Player,Objektmodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49dd3b7862e2d9c5580950ad2eb718bd1c8125a5d22ec6a08533c140de545086
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749741"
---
# <a name="differences-between-the-object-models"></a>Unterschiede zwischen den Objektmodellen

Es gibt zwei Hauptunterschiede zwischen dem Windows Media Player 6.4-Objektmodell und dem Windows Media Player 7 oder höher-Objektmodell.

-   **CLSID** Das objektmodell Windows Media Player 7 oder höher ist ein vollständiger Abstieg vom Objektmodell der Version 6.4. Die com-Spezifikation (Component Object Model) erfordert, dass alle vorhandenen Schnittstellen in neuen Versionen einer COM-Komponente weiterhin funktionieren müssen. Dies bedeutet, dass einer COM-Komponente neue Schnittstellen hinzugefügt werden können, vorhandene Schnittstellen jedoch nie geändert werden dürfen. Dadurch wird sichergestellt, dass älterer Clientcode immer mit der bestimmten Komponente funktioniert, für die er entwickelt wurde. Daher hat das Windows Media Player 7 oder höher ActiveX Steuerelement eine neue Klassen-ID: 6BF52A52-394A-11D3-B153-00C04F79FAA6. Wenn Sie die neuen Funktionen des Steuerelements für diese Version nutzen möchten, müssen Sie Ihre CLSID ändern.
-   **Hierarchisches Objektmodell** Wenn Sie das Windows Media Player 6.4 ActiveX-Steuerelements verwendet haben, haben Sie möglicherweise bemerkt, dass auf alle Eigenschaften, Methoden und Ereignisse über dasselbe Objekt zugegriffen wird: das **Player-Objekt.** Im Gegensatz dazu ist das Windows Media Player 7 oder höher-Objektmodell als Hierarchie von Objekten organisiert. Das **Player-Objekt** ist immer noch das Stammobjekt, aber auf Funktionen wird jetzt über eine Vielzahl von untergeordneten Objekten zugegriffen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Leitfaden zur Migration von Objektmodellen**](object-model-migration-guide.md)
</dt> </dl>

 

 




