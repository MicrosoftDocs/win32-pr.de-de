---
title: Persistente Speicherung auf dem Server
description: Sie können Ihre Anwendung optimieren, damit der Server-Stub beim Abschluss eines Remote Prozedur Aufrufes keinen Arbeitsspeicher auf dem Server freigibt.
ms.assetid: 340334e2-94ac-4be2-a16d-38bc4c64e7db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7237fe6136918e5495ee1f22bac0991d71c5dbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947897"
---
# <a name="persistent-storage-on-the-server"></a>Persistente Speicherung auf dem Server

Sie können Ihre Anwendung optimieren, damit der Server-Stub beim Abschluss eines Remote Prozedur Aufrufes keinen Arbeitsspeicher auf dem Server freigibt. Wenn ein Kontext Handle z. b. von mehreren Remote Prozeduren bearbeitet wird, können Sie das ACF-Attribut **\[ (nicht \_ frei \] )** verwenden, um den belegten Arbeitsspeicher auf dem Server beizubehalten.

Das Attribut " **\[ zuordnen (nicht \_ frei) \]** " wird der ACF- **typedef** -Deklaration in der ACF hinzugefügt. Beispiel:

``` syntax
/* ACF file fragment */
typedef [allocate(all_nodes, dont_free)] P_TREE_TYPE;
```

Wenn das Attribut " **\[ zuordnen (nicht \_ frei) \]** " angegeben ist, wird die Strukturdaten Struktur vom Serverstub zugeordnet, aber nicht freigegeben. Wenn Sie die Zeiger auf solche permanenten Datenbereiche, die für andere Routinen verfügbar sind, – z. b. durch Kopieren der Zeiger auf globale Variablen –, sind die beibehaltenen Daten für andere Serverfunktionen zugänglich. Das Attribut " **\[ zuordnen" (nicht \_ frei) \]** ist besonders nützlich für die Beibehaltung von permanenten Zeiger Strukturen als Teil der Server Zustandsinformationen, die einem Kontext Handle-Typ zugeordnet sind.

 

 




