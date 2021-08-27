---
description: Das Standardziel kann durch einfaches erneutes Aufrufen von WSPConnect geändert werden, auch wenn der Socket bereits verbunden ist. Alle Datagramme, die für den Empfang in die Warteschlange gestellt werden, werden verworfen, wenn sich die neue Adresse von der in einer vorherigen WSPConnect-Verbindung angegebenen Adresse unterscheiden.
ms.assetid: b5f5ab97-03bd-4f5c-8808-d14ad5a56a5a
title: Erneutes Herstellen einer Verbindung und Trennen der Verbindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a4c50872b6690c42d97c3696bcfcb2586b9b5b510c17aafc5dcc159b17ed56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121360"
---
# <a name="reconnecting-and-disconnecting"></a>Erneutes Herstellen einer Verbindung und Trennen der Verbindung

Das Standardziel kann durch einfaches erneutes Aufrufen von [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) geändert werden, auch wenn der Socket bereits verbunden ist. Alle Datagramme, die in die Warteschlange für den Empfang gestellt werden, werden verworfen, wenn sich die neue Adresse von der in einem vorherigen **WSPConnect angegebenen Adresse unterscheiden.**

Wenn die für den Socket angegebene Adresse alle Nullen ist, wird der Socket getrennt. Die Standard-Remoteadresse ist unbestimmt, sodass [**WSPSend-**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) und [**WSPRecv-Aufrufe**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) den Fehlercode WSAENOTCONN zurückgeben, obwohl [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) und [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) weiterhin verwendet werden können.

 

 
