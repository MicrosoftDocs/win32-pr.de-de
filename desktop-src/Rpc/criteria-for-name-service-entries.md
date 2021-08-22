---
title: Kriterien für Namensdiensteinträge
description: Kriterien für Namensdiensteinträge mit Remoteprozeduraufruf (RPC).
ms.assetid: f9a7b935-7104-489c-93a8-0c3793d17348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 609c545c72687a0b9b73db56d2f08654941e464c790e091ee886159d9e9593ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931119"
---
# <a name="criteria-for-name-service-entries"></a>Kriterien für Namensdiensteinträge

Die folgenden Kriterien werden bei der Verarbeitung von Namensdiensteinträgen verwendet:

-   Wenn Sie einen Eintragsnamen angeben, der nicht **NULL** für [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)ist, ist dieser Eintrag der einzige Eintrag, der nach Bindungshandles durchsucht wird. Wenn Sie **NULL übergeben,** werden alle Einträge in Ihrer Anmeldedomäne durchsucht. Beachten Sie, dass dies keine vertrauenswürdigen Domänen umfasst.
-   Wenn Sie ein Schnittstellenhandles bereitstellen, werden Bindungshandles nur dann von einem Eintrag zurückgegeben, wenn der Schnittstellenabschnitt des Eintrags eine kompatible Version dieser Schnittstellen-UUID enthält. Das heißt, die Hauptversionsnummer muss mit ihrer Schnittstellen-UUID identisch sein, während die Nebenversionsnummer gleich oder größer als Ihre sein muss.
-   Wenn Sie eine Objekt-UUID bereitstellen, werden Bindungshandles nur dann von einem Eintrag zurückgegeben, wenn der Objekt-UUID-Abschnitt des Eintrags diese bestimmte Objekt-UUID enthält.

Wenn ein Name-Diensteintrag die oben beschriebenen Kriterien überdauert, werden alle Bindungshandles aus diesen Einträgen gesammelt. Handles mit einer Protokollsequenz, die vom Client nicht unterstützt wird, werden verworfen, und die verbleibenden Handles werden als Ausgabe von [**RpcNsBindingLookupNext an**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)Sie zurückgegeben.

 

 




