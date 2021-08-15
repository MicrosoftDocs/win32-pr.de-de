---
title: Bandinitialisierung
description: Eine Anwendung muss die CreateFile-Funktion verwenden, um ein Handle eines Bandgeräts zu erstellen. Dieses Handle wird in nachfolgenden Vorgängen auf dem Band auf dem Gerät verwendet.
ms.assetid: 5e7eddd2-8137-4e79-b1ee-c371bc4c7f75
keywords:
- Sicherung der Bandinitialisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aeba729feb9351b5af15d26f6366b455c5ce74a9cc6300c9ab8d25047b4760b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835403"
---
# <a name="tape-initialization"></a>Bandinitialisierung

Eine Anwendung muss die [**CreateFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) verwenden, um ein Handle eines Bandgeräts zu erstellen. Dieses Handle wird in nachfolgenden Vorgängen auf dem Band auf dem Gerät verwendet.

Bevor eine Anwendung auf ein Band schreibt, muss das Band entsprechend den Anforderungen der Anwendung und den Funktionen des verwendeten Bandlaufwerks formatiert werden. Die [**CreateTapePartition-Funktion**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition) formatiert ein Band neu und erstellt darauf eine bestimmte Anzahl von Partitionen einer angegebenen Größe.

Die [**PrepareTape-Funktion**](/windows/desktop/api/Winbase/nf-winbase-preparetape) bereitet ein Band für den Zugriff auf oder das Entfernen vor. Diese Funktion kann ein Band laden, entladen, sperren oder entsperren. Diese Funktion kann das Band auch absichern, indem sie das Band an das Ende des Bandes und wieder zurück an den Anfang bewegt.

Zum Abrufen und Festlegen von Informationen zu einem Band- und Bandlaufwerk verwendet eine Anwendung die Funktionen [**GetTapeParameters,**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) [**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters)und [**GetTapeStatus.**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus)

[**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) ruft Informationen ab, die ein Band oder ein Bandlaufwerk beschreiben. Die Bandinformationen umfassen den Typ, die Dichte und die Blockgröße des Bands. die Anzahl der Partitionen auf dem Band; die menge des verbleibenden Bandes; Und so weiter. Die Informationen zum Bandlaufwerk umfassen die Standardblockgröße des Laufwerks, die maximale Partitionsanzahl und die unterstützten Features.

[**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters) legt entweder die Bandblockgröße oder die Bandlaufwerkflags fest, die angeben, ob das Laufwerk hardwarefehlerkorrektur, Datenkomprimierung, Datenauffüllung oder eine beliebige Kombination der drei unterstützt.

[**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) gibt an, ob das Bandlaufwerk bereit ist, Bandbefehle zu verarbeiten.

 

 