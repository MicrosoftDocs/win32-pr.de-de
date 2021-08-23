---
title: Erstellen von Datenträgern mit mehreren Sitzungen
description: IMAPI kann Datendatenträger mit mehreren Sitzungen erstellen. Beim Erstellen eines Datenträgers mit mehreren Sitzungen sind einige Aspekte zu beachten.
ms.assetid: 02405a32-53d5-4618-bfa0-c9a9f5e3c51b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7477b108a6b7b07d6d82230362899da26e7264e62a460c197338e223f0e95078
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977120"
---
# <a name="creating-discs-with-multiple-sessions"></a>Erstellen von Datenträgern mit mehreren Sitzungen

IMAPI kann Datendatenträger mit mehreren Sitzungen erstellen. Beim Erstellen eines Datenträgers mit mehreren Sitzungen sind einige Aspekte zu beachten.

Die [**IDiscMaster::SetActiveDiscRecorder-Methode**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscrecorder) bestimmt beim Festlegen, ob auf dem aktiven Laufwerk ein IMAPI-Datenträger mit mehreren Sitzungen vorhanden ist. Wenn ja, wechselt DIE IMAPI automatisch in den Modus für mehrere Sitzungen. Die Verwendung von [**ClearFormatContent,**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) nachdem der Modus für mehrere Sitzungen eingerichtet wurde, bewirkt, dass IMAPI in den Einzelsitzungsmodus zurückkehrt. Dies bedeutet, dass ein leerer Datenträger für einen [**RecordDisc-Burnvorgang**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) erforderlich ist. Wenn sich der Datenträger im Modus mit mehreren Sitzungen befindet, muss sich derselbe Datenträger im aktiven Aufzeichnungsmodus befinden. Andernfalls wird ein Fehlercode von IMAPI \_ E \_ WRONGDISC zurückgegeben.

Die Auswahl eines Aufzeichnungsgeräts im Joliet-Format bewirkt, dass die IMAPI Informationen vom derzeit installierten Datenträger liest. Wenn es sich bei dem Datenträger um einen vorherigen IMAPI-Joliet-Datenträger handelt, der über Speicherplatz für eine andere Sitzung verfügt, legt sich DIE IMAPI automatisch in den Modus für mehrere Sitzungen fest. Dieser Datenträger muss im aktiven Aufzeichnungsgerät vorhanden sein, wenn [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc)aufgerufen wird.

Das Schließen der ersten Sitzung auf einem Datenträger erfordert 21 MB. Für jede zusätzliche Sitzung sind 11 MB erforderlich, um geschlossen zu werden.

 

 




