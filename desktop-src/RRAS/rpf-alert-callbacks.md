---
title: RPF-Warnungsrückrufe
description: Nachdem der Multicastgruppen-Manager eine Benachrichtigung über ein Paket von einer neuen Quelle oder von einem Paket empfängt, das für eine neue Gruppe bestimmt ist, sucht der Multicastgruppen-Manager die Route zur Quelle in der Multicastansicht der Routingtabelle.
ms.assetid: dacccca2-e6a5-417a-a217-06ff846d55f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ff1c2dc66b2307b60fb649fd8a0adb6992a63532bf9aa45350d261ab04b6c5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035920"
---
# <a name="rpf-alert-callbacks"></a>RPF-Warnungsrückrufe

Nachdem der Multicastgruppen-Manager eine Benachrichtigung über ein Paket von einer neuen Quelle oder von einem Paket empfängt, das für eine neue Gruppe bestimmt ist, sucht der Multicastgruppen-Manager die Route zur Quelle in der Multicastansicht der Routingtabelle. Der Multicastgruppen-Manager ruft dann den [**PMGM \_ RPF \_ CALLBACK-Rückruf**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback) für das Protokoll auf, das die Schnittstelle besitzt, an der die Daten eingetroffen sind.

Nachdem dieser Rückruf aufgerufen wurde, kann das Routingprotokoll die eingehende Schnittstelle ändern, wenn das Routingprotokoll die Daten für die Gruppe auf einer anderen Schnittstelle empfangen muss.

 

 




