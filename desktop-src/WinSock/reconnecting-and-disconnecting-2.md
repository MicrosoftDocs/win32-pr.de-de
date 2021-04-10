---
description: Das Standardziel kann durch einfaches Aufrufen von wspconnect geändert werden, auch wenn der Socket bereits verbunden ist. Alle in der Warteschlange eingereihten Datagramme werden verworfen, wenn sich die neue Adresse von der Adresse unterscheidet, die in einer früheren wspconnect-Verbindung angegeben wurde.
ms.assetid: b5f5ab97-03bd-4f5c-8808-d14ad5a56a5a
title: Erneutes Herstellen einer Verbindung und trennen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7babefe03be44f942ee60a840aa210ee3c0e25da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864043"
---
# <a name="reconnecting-and-disconnecting"></a>Erneutes Herstellen einer Verbindung und trennen

Das Standardziel kann durch einfaches Aufrufen von [**wspconnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) geändert werden, auch wenn der Socket bereits verbunden ist. Alle in der Warteschlange eingereihten Datagramme werden verworfen, wenn sich die neue Adresse von der Adresse unterscheidet, die in einer früheren **wspconnect-Verbindung** angegeben wurde.

Wenn die für den Socket angegebene Adresse alle Nullen ist, wird der Socket getrennt – die standardmäßige Remote Adresse ist unbestimmt, sodass [**wspsend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) -und [**wsprecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) -Aufrufe den Fehlercode wsaerotconn zurückgeben, obwohl [**wspsendto**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) und [**wsprecvfrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) möglicherweise weiterhin verwendet werden.

 

 
