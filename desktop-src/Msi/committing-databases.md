---
description: Änderungen an der Installations Datenbank werden erst dann in die Datenbank geschrieben, wenn Sie msidatabasecommit aufgerufen haben.
ms.assetid: 65271631-457c-4d3e-9384-126d2c9d63d7
title: Commit für Datenbanken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1336b094703e61b14966e7a73a6e67f73762024
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866724"
---
# <a name="committing-databases"></a>Commit für Datenbanken

Änderungen an der Installations Datenbank werden erst dann in die Datenbank geschrieben, wenn Sie [**msidatabasecommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)aufgerufen haben.

**So stellen Sie sicher, dass in einer Datenbank vorgenommene Änderungen abgeschlossen werden**

1.  Überprüfen Sie, ob eine Tabelle geschrieben wird, wenn Sie [**msidatabasecommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) aufrufen, indem Sie [**msidatabaseistablepersistent**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta)aufrufen.
2.  Ruft die [**msidatabasecommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) -Funktion auf, um Änderungen an der Datenbank abzuschließen.

Änderungen, die in einer Datenbank vorgenommen werden, werden akkumuliert und nicht in der eigentlichen Datenbank wiedergegeben, bis Sie [**msidatabasecommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)aufgerufen haben. Für temporäre Spalten oder Zeilen wird kein Commit an die Datenbank ausgeführt. Wenn eine Datenbank geschlossen wird, wird für alle seit dem letzten **msidatabasecommit** vorgenommenen Änderungen automatisch ein Rollback ausgeführt.

 

 



