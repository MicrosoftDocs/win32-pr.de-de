---
description: Nachdem Sie durch Aufrufen der setupopenfilequeue-Funktion ein Handle für eine Datei Warteschlange erhalten haben, können Sie der Warteschlange Datei Vorgänge hinzufügen, entweder Datei-für-Datei oder alle Dateien in einem INF-Abschnitt in die Warteschlange stellen.
ms.assetid: ba2f40cd-b0df-4768-8080-4fd80c50f2c2
title: Warteschlangen Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7b5ab9a9be136e50547076c8daf9bd519ade72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865420"
---
# <a name="queuing-files"></a>Warteschlangen Dateien

Nachdem Sie durch Aufrufen der [**setupopenfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) -Funktion ein Handle für eine Datei Warteschlange erhalten haben, können Sie der Warteschlange Datei Vorgänge hinzufügen, entweder Datei-für-Datei oder alle Dateien in einem INF-Abschnitt in die Warteschlange stellen.

Wenn Sie der Datei Warteschlange einen Kopiervorgang für eine einzelne Datei hinzufügen möchten, rufen Sie die [**setupqueuecopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya) -Funktion auf. Wenn Sie einen Datei Kopiervorgang mithilfe der in einer INF-Datei angegebenen standardmäßigen Quell Medien und Ziel Ziele in die Warteschlange stellen möchten, können Sie die [**setupqueuedefaultcopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya) -Funktion aufrufen.

Durch Aufrufen der Funktion [**setupqueuedelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) oder [**setupqueuerename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea) können Sie der geöffneten Datei Warteschlange einen einzelnen Vorgang zum Löschen oder Umbenennen einer Datei hinzufügen.

 

 



