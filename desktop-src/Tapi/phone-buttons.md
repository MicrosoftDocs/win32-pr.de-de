---
description: TAPI modelliert Telefonschaltflächen und -schläge als Tasten-/Lampe-Paare.
ms.assetid: e4c50bd6-a256-407f-af3b-b24383a30ea0
title: Telefon Schaltflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e72288133615b19e622434b8727608aaec9a9136dd58eaa03e339708c42a13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774160"
---
# <a name="phone-buttons"></a>Telefon Schaltflächen

TAPI modelliert die Schaltflächen und Brillen eines Telefons als Schaltflächen-Lampe-Paare. Eine Schaltfläche ohne Lampe oder eine Lampe ohne Schaltfläche wird mithilfe eines Dummyindikators für die fehlende Lampe oder Schaltfläche angegeben. Eine Schaltfläche mit mehreren Strahlen wird mit mehreren Schaltflächen-Lampe-Paaren modelliert.

Informationen, die einer Telefonschaltfläche zugeordnet sind, können festgelegt und abgerufen werden. Wenn eine Schaltfläche gedrückt wird, wird eine [**PHONE \_ BUTTON-Nachricht**](phone-button.md) an die Anwendungsfunktion gesendet. Die Parameter dieser Nachricht sind ein Handle für das Telefongerät und der Button-Lampe-Bezeichner der Schaltfläche, die gedrückt wurde. Den Tastaturtastenschaltflächen "0" bis "9", \* "" " und " \# " " werden die festen Button-Lamp-Bezeichner 0 bis 11 zugewiesen.

Die Funktionen, die Schaltflächen zugeordnet sind, sind [**phoneSetButtonInfo,**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo)die die einer Schaltfläche auf einem Telefongerät zugeordneten Informationen festlegt, und [**phoneGetButtonInfo,**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo)die Informationen zurückgibt, die einer Schaltfläche auf einem Telefongerät zugeordnet sind. Die NACHRICHT PHONE \_ BUTTON wird an eine Anwendung gesendet, wenn eine Schaltfläche auf dem Telefon gedrückt wird.

Die einer Schaltfläche zugeordneten Informationen haben hinsichtlich TAPI keine semantische Bedeutung. Dies ist nützlich für gerätespezifische Anwendungen, die die Bedeutung dieser Informationen für ein bestimmtes Telefongerät verstehen, oder für die Anzeige für den Benutzer, z. B. Onlinehilfe.

 

 



