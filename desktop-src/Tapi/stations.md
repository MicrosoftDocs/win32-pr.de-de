---
description: Stations Sätze, die über einen Drittanbieter Link überwacht werden, werden als Linien Gerät und möglicherweise als zugehöriges Telefongerät modelliert.
ms.assetid: 1d116734-cd8f-40f1-9069-2dad351a24bf
title: Station
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff497eb70d1a1fd8441eeb8ad24bae6e5d1cd03e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360875"
---
# <a name="stations"></a>Station

Stations Sätze, die über einen Drittanbieter Link überwacht werden, werden als Linien Gerät und möglicherweise als zugehöriges Telefongerät modelliert. Das liniengerät kann mehrere Adressen haben, wenn das modellierte Terminal mehr als eine Verzeichnis Nummer (DN) unterstützt. Mehrere Aufrufe zum Aufrufen desselben DN können als einzelne Adresse modelliert werden, die mehrere Aufrufe unterstützt.

Aufrufe zwischen zwei Stationen auf dem Switch verfügen über zwei Aufruf Handles, von denen eine die Aufruf Ansicht von der ersten Station (auf Ihrem liniengerät) und die andere die Aufruf Ansicht von der zweiten Station (auf dem liniengerät) gibt. Beispielsweise würde ein [**linemakecall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) eines Drittanbieters, das von einer Anwendung auf dem Server platziert wurde, an das Zeilen Gerät geleitet, das der Station zugeordnet ist, von der der Anruf gewählt werden soll. in dieser Zeile wird ein Anruf Handle für die in [**linecallparamemes**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) angegebene Adresse erstellt (auf diese Weise wird gesteuert, welcher DN auf einem Telefon verwendet wird, das mehrere DNS unterstützt). Wenn der-Befehl für die Zieladresse bereitgestellt wird, wird ein neues Rückruf Handle erstellt, das einen aufrufenden Ansichts *Zustand anzeigt* . Anwendungen wissen, dass es sich um eine weitere Ansicht desselben Aufrufs durch den **dwcallid** -Member in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) handelt, der für beide Aufrufe gleich ist. Beide Aufrufe laufen in den *Leerlauf* , wenn der Aufruf gelöscht wurde. ein-Rückruf konnte von der Drittanbieter Anwendung gelöscht werden, indem ein [**linedrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) für einen der-Rückruf Handles ausgeführt wird.

 

 



