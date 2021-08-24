---
title: Synchronisierungspunkte
description: Wenn Eigenschaftensätze für dasselbe Objekt wie IStorage unterstützt werden, ist es wichtig, Synchronisierungspunkte zwischen dem Basisspeicher und dem Eigenschaftenspeicher zu beachten.
ms.assetid: 34cc4338-b29f-43f9-946d-14b2b235ccec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf924458d81003e2cc211ff810ebb714399ac28e91189586491b584cff6a3390
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034880"
---
# <a name="synchronization-points"></a>Synchronisierungspunkte

Wenn Eigenschaftensätze für dasselbe Objekt wie [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)unterstützt werden, ist es wichtig, Synchronisierungspunkte zwischen dem Basisspeicher und dem Eigenschaftenspeicher zu beachten.

Der Eigenschaftensatzspeicher enthält den Eigenschaftensatzstream in einem internen Puffer, bis für diesen Puffer ein Commit über die [**IPropertyStorage::Commit-Methode**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) ausgeführt wird. Dies gilt unabhängig davon, ob [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) im Transaktionsmodus oder im direkten Modus geöffnet wurde.

 

 




