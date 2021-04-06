---
title: Synchronisierungs Punkte
description: Wenn Eigenschaften Sätze für dasselbe Objekt wie IStorage unterstützt werden, ist es wichtig, die Synchronisierungs Punkte zwischen dem Basis Speicher und dem Eigenschaften Speicher zu beachten.
ms.assetid: 34cc4338-b29f-43f9-946d-14b2b235ccec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa156efbb1573b2954c1f7da07a58ed663c71781
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714567"
---
# <a name="synchronization-points"></a>Synchronisierungs Punkte

Wenn Eigenschaften Sätze für dasselbe Objekt wie [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)unterstützt werden, ist es wichtig, die Synchronisierungs Punkte zwischen dem Basis Speicher und dem Eigenschaften Speicher zu beachten.

Der Eigenschaften Satz Speicher speichert den Eigenschaften Satz-Stream in einem internen Puffer, bis für den Puffer ein Commit durch die [**IPropertyStorage:: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) -Methode ausgeführt wird. Dies gilt unabhängig davon, ob [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) im transaktiven oder im direkten Modus geöffnet wurde.

 

 




