---
description: Sie können das Installationsprogramm verwenden, um die Informationen in einer Datenbank einer anderen Datenbank hinzuzufügen, indem Sie eine Zusammenführung ausführen.
ms.assetid: c53ef3d2-b3dc-4cd1-bd98-a856a223917f
title: Zusammenführen von Datenbanken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2931bb624037f2f909b99cfeb19a64fcb4abef689fe988a308d35766f50b1dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628706"
---
# <a name="merging-databases"></a>Zusammenführen von Datenbanken

Sie können das Installationsprogramm verwenden, um die Informationen in einer Datenbank einer anderen Datenbank hinzuzufügen, indem Sie eine Zusammenführung ausführen. [Zusammenführungen und Transformationen](merges-and-transforms.md) werden für eine gesamte Datenbank verwendet, und bei einem Merge werden zwei Datenbanken zu einer Datenbank kombiniert. Zusammenführungen sind für Entwicklungsteams nützlich, da sie es ermöglichen, die Installationsdatenbank großer Anwendungen in kleinere Teile zu unterteilen und später erneut in die vollständige Installationsdatenbank zu unterteilen.

**So führen Sie mehrere Komponentendatenbanken in einer einzelnen vollständigen Datenbank zusammen**

1.  Entwickeln Sie die Partiellen Komponentendatenbanken separat.
2.  Führen Sie jede Komponentendatenbank mit der Hauptproduktdatenbank zusammen, indem Sie die [**MsiDatabaseMerge-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) aufrufen.

 

 



