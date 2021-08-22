---
title: Übersicht über den Eintrag "Name Service"
description: Der Name-Diensteintrag besteht aus drei verschiedenen Abschnitten.
ms.assetid: 3059a9a9-174d-4d04-8565-e4558f17f465
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2d7982cef018ec91435c647000031ae42a25e2e2bb315a20623ac75e610197e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073560"
---
# <a name="an-overview-of-the-name-service-entry"></a>Übersicht über den Eintrag "Name Service"

Der Name-Diensteintrag besteht aus drei verschiedenen Abschnitten. Der erste Abschnitt gilt für Schnittstellen (UUID + Version), der zweite Abschnitt enthält die Objekt-UUIDs und der dritte Abschnitt für Bindungshandles. Sie geben einen Namen für den Eintrag an, der als Möglichkeit dient, ihn zu identifizieren.

Beim Aufrufen [**von RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta)gibt der Server den Namen des Eintrags an, in dem die exportierten Informationen gespeichert werden. Diese neu exportierte Schnittstelle wird dann dem Schnittstellenabschnitt des Namensdiensteintrags hinzugefügt. Alle Schnittstellen, die bereits im Namensdiensteintrag vorhanden sind, bleiben auch erhalten. Der gleiche Prozess wird für Objekt-UUIDs und Bindungshandles befolgt.

Der Client ruft [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina) (oder [**RpcNsBindingImportBegin)**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)auf, um nach einem geeigneten Bindungshandler zu suchen. Der Eintragsname, das Schnittstellenhand handle und eine Objekt-UUID werden extrahiert. Diese schränken die Einträge ein, von denen Bindungshandles zurückgegeben werden. Wenn ein Eintrag den Suchkriterien entspricht, werden alle Bindungshandles in diesem Eintrag von [**RpcNsBindingImportNext zurückgegeben.**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)

 

 




