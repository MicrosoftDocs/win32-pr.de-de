---
title: Unterschiede zwischen den Objekt Modellen
description: Unterschiede zwischen den Objekt Modellen
ms.assetid: a6d2a2d5-2892-461a-aa6d-7e11b504b2af
keywords:
- Windows Media Player, Objektmodell
- Windows Media Player-Objektmodell, Versions Unterschiede
- Objektmodell, Versions Unterschiede
- Windows Media Player ActiveX-Steuerelement, Versions Unterschiede
- ActiveX-Steuerelement, Versions Unterschiede
- Windows Media Player Mobile ActiveX-Steuerelement, Versions Unterschiede
- Windows Media Player Mobile, Objektmodell
- Migrations Handbuch, Versions Unterschiede
- Versionen von Windows Media Player, Objektmodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a5341067e2daad0f44fbdd7075f0f543bac2fd4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341256"
---
# <a name="differences-between-the-object-models"></a>Unterschiede zwischen den Objekt Modellen

Zwischen dem Objektmodell Windows Media Player 6,4 und dem Objektmodell Windows Media Player 7 oder höher bestehen zwei wesentliche Unterschiede.

-   **CLSID** Das Objektmodell von Windows Media Player 7 oder höher ist eine vollständige Abweichung vom Objektmodell der Version 6,4. Die Component Object Model (com)-Spezifikation erfordert, dass alle vorhandenen Schnittstellen in neuen Versionen einer COM-Komponente weiterhin funktionieren. Dies bedeutet, dass neue Schnittstellen zu einer COM-Komponente hinzugefügt werden können, vorhandene Schnittstellen jedoch nie geändert werden müssen, um sicherzustellen, dass der ältere Client Code immer mit der jeweiligen Komponente funktioniert, für die er verwendet werden soll. Das ActiveX-Steuerelement von Windows Media Player 7 oder höher hat daher eine neue Klassen-ID: 6BF 52a52-394a-11d3-b153-00c04s faa6. Wenn Sie die neuen Funktionen des Steuer Elements für diese Version nutzen möchten, müssen Sie die CLSID ändern.
-   **Hierarchisches Objektmodell** Wenn Sie das ActiveX-Steuerelement von Windows Media Player 6,4 verwendet haben, haben Sie möglicherweise bemerkt, dass auf alle Eigenschaften, Methoden und Ereignisse über das gleiche Objekt zugegriffen wird: das **Player** -Objekt. Im Gegensatz dazu ist das Objektmodell Windows Media Player 7 oder höher als eine Hierarchie von Objekten organisiert. Das **Player** -Objekt ist nach wie vor das Root-Objekt, aber auf Funktionen wird jetzt über eine Vielzahl von untergeordneten Objekten zugegriffen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Handbuch für die Migration des Objektmodells**](object-model-migration-guide.md)
</dt> </dl>

 

 




