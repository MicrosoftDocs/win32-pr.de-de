---
title: Kriterien für Namensdienst Einträge
description: Kriterien für Namensdienst Einträge mit Remote Prozedur Aufruf (RPC).
ms.assetid: f9a7b935-7104-489c-93a8-0c3793d17348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb32314dc86b179ea98bdf07000dc5ea359bdc77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471453"
---
# <a name="criteria-for-name-service-entries"></a>Kriterien für Namensdienst Einträge

Beim Verarbeiten von Namensdienst Einträgen werden folgende Kriterien verwendet:

-   Wenn Sie für [**rpcnsbindinglookupbegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)einen nicht-**null** -Eingabe Namen angeben, ist dieser Eintrag der einzige Eintrag, der nach Bindungs Handles durchsucht wird. Wenn Sie **null** übergeben, werden alle Einträge in der Anmelde Domäne durchsucht. Beachten Sie, dass dies keine vertrauenswürdigen Domänen umfasst.
-   Wenn Sie ein Schnittstellen handle bereitstellen, werden Bindungs Handles nur von einem Eintrag zurückgegeben, wenn der Schnittstellen Abschnitt des Eintrags eine kompatible Version der Schnittstelle uuid enthält. Das heißt, die Hauptversionsnummer muss mit der UUID der Schnittstelle identisch sein, während die neben Versionsnummer größer oder gleich ihrem Wert sein muss.
-   Wenn Sie eine Objekt-UUID angeben, werden Bindungs Handles nur von einem Eintrag zurückgegeben, wenn der Objekt-UUID-Abschnitt des Eintrags dieses bestimmte Objekt "uuid" enthält.

Wenn ein Name-Dienst Eintrag die oben beschriebenen Kriterien überschreitet, werden alle Bindungs Handles aus diesen Einträgen gesammelt. Handles mit einer Protokoll Sequenz, die vom Client nicht unterstützt wird, werden verworfen, und die restlichen Handles werden als Ausgabe von [**rpcnsbindinglookupnext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)zurückgegeben.

 

 




