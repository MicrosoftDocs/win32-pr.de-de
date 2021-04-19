---
title: Übersicht über den Eintrag "Name Service"
description: Der Name-Dienst Eintrag besteht aus drei unterschiedlichen Abschnitten.
ms.assetid: 3059a9a9-174d-4d04-8565-e4558f17f465
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efc3855f586582b013bc47b11eb058ae461014f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338414"
---
# <a name="an-overview-of-the-name-service-entry"></a>Übersicht über den Eintrag "Name Service"

Der Name-Dienst Eintrag besteht aus drei unterschiedlichen Abschnitten. Der erste Abschnitt ist für Schnittstellen (UUID + Version), der zweite Abschnitt enthält die Objekt-UUIDs und der dritte Abschnitt für Bindungs Handles. Sie geben einen Namen für den Eintrag an, der als Möglichkeit dient, ihn zu identifizieren.

Beim Aufrufen von [**rpcnsbindingexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta)gibt der Server den Namen des Eintrags an, in den die exportierten Informationen platziert werden sollen. Diese neu exportierte Schnittstelle wird dann dem Schnittstellen Abschnitt des Namensdienst Eintrags hinzugefügt. Alle Schnittstellen, die bereits im Namen Dienst Eintrag vorhanden sind, bleiben ebenfalls erhalten. Der gleiche Vorgang wird für Objekt-UUIDs und Bindungs Handles befolgt.

Der Client ruft [**rpcnsbindinglookupbegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina) (oder [**rpcnsbindingimportbegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)) auf, um nach einem entsprechenden Bindungs Handle zu suchen. Der Eintrags Name, das Schnittstellen Handle und eine Objekt-UUID werden extrahiert. Diese schränken die Einträge ein, von denen Bindungs Handles zurückgegeben werden. Wenn ein Eintrag mit den Suchkriterien übereinstimmt, werden alle Bindungs Handles in diesem Eintrag von [**rpcnsbindingimportnext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)zurückgegeben.

 

 




