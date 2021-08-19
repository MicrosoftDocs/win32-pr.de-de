---
description: Da duplizierte Socketdeskriptoren und nicht die zugrunde liegenden Sockets sind, werden alle einem Socket zugeordneten Zustände für alle Deskriptoren gemeinsam gehalten.
ms.assetid: f3a2cd5a-bc3a-4aeb-8606-7b8aa6afb105
title: Mehrere Handles für einen einzelnen Socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e402d19c3306158a905f2e9ddc263649e52d214a3d9441509e7a277f7d2800
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121400"
---
# <a name="multiple-handles-to-a-single-socket"></a>Mehrere Handles für einen einzelnen Socket

Da duplizierte Socketdeskriptoren und nicht die zugrunde liegenden Sockets sind, werden alle einem Socket zugeordneten Zustände für alle Deskriptoren gemeinsam gehalten. Beispielsweise wird [**ein WSPSetSockOpt-Vorgang,**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) der mit einem Deskriptor ausgeführt wird, anschließend mithilfe eines [**WSPGetSockOpt-Vorgangs**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) von einem oder allen Deskriptoren angezeigt.

Die Benachrichtigung bei freigegebenen Sockets unterliegt den üblichen Einschränkungen von [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) und [**WSPEventSelect.**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)) Wenn einer dieser Aufrufe mit einem der freigegebenen Deskriptoren erfolgt, wird jede vorherige Ereignisregistrierung für den Socket abgebrochen, unabhängig davon, welcher Deskriptor für diese Registrierung verwendet wurde. Daher wäre es beispielsweise nicht möglich, dass Prozess A FD READ-Ereignisse und Prozess \_ B FD \_ WRITE-Ereignisse erhält. In Situationen, in denen eine solche enge Koordination erforderlich ist, wird empfohlen, dass Entwickler die Verwendung von Threads anstelle separater Prozesse in Erwägung ziehen.

 

 
