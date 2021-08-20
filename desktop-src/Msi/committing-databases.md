---
description: Änderungen an der Installationsdatenbank werden erst in die Datenbank geschrieben, wenn Sie MsiDatabaseCommit aufrufen.
ms.assetid: 65271631-457c-4d3e-9384-126d2c9d63d7
title: Committen von Datenbanken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1ab5f4da5b82fb3b6b2ac7d2371bd8046ab87a23d2ef43b6473f7e36a4771a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145349"
---
# <a name="committing-databases"></a>Committen von Datenbanken

Änderungen an der Installationsdatenbank werden erst in die Datenbank geschrieben, wenn Sie [**MsiDatabaseCommit aufrufen.**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)

**So stellen Sie sicher, dass die in einer Datenbank vorgenommenen Änderungen abgeschlossen sind**

1.  Überprüfen Sie, ob eine Tabelle geschrieben wird, wenn Sie [**MsiDatabaseCommit aufrufen, indem**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) Sie [**MsiDatabaseIsTablePersistent aufrufen.**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta)
2.  Rufen Sie die [**MsiDatabaseCommit-Funktion auf,**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) um Änderungen an der Datenbank zu finalisieren.

In einer Datenbank vorgenommene Änderungen werden gesammelt und erst dann in der tatsächlichen Datenbank widergespiegelt, wenn Sie [**MsiDatabaseCommit aufrufen.**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) Für temporäre Spalten oder Zeilen wird kein Committed für die Datenbank erstellt. Wenn eine Datenbank geschlossen wird, wird für alle Änderungen, die seit dem letzten **MsiDatabaseCommit** vorgenommen wurden, automatisch ein Rollback ausgeführt.

 

 



