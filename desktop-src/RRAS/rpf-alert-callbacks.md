---
title: RPF-Warnungs Rückrufe
description: Nachdem der Multicast-Gruppen-Manager eine Benachrichtigung über ein Paket von einer neuen Quelle oder einem Paket erhalten hat, das für eine neue Gruppe bestimmt ist, sucht der Multicast-Gruppen-Manager in der Multicast Ansicht der Routing Tabelle die Route zur Quelle.
ms.assetid: dacccca2-e6a5-417a-a217-06ff846d55f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7832a25f8b44821f4b46a69943b4bba3519207c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714664"
---
# <a name="rpf-alert-callbacks"></a>RPF-Warnungs Rückrufe

Nachdem der Multicast-Gruppen-Manager eine Benachrichtigung über ein Paket von einer neuen Quelle oder einem Paket erhalten hat, das für eine neue Gruppe bestimmt ist, sucht der Multicast-Gruppen-Manager in der Multicast Ansicht der Routing Tabelle die Route zur Quelle. Der Multicast-Gruppen-Manager ruft dann den [**pmgm \_ RPF- \_ Rückruf**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback) Rückruf für das Protokoll auf, das die Schnittstelle besitzt, auf der die Daten eingetroffen sind.

Nachdem dieser Rückruf aufgerufen wurde, kann das Routing Protokoll die eingehende Schnittstelle ändern, wenn das Routing Protokoll die Daten für die Gruppe auf einer anderen Schnittstelle empfangen muss.

 

 




