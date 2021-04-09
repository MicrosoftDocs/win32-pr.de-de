---
description: Mit der setupsetsourcelist-Funktion wird eine Quell Liste im Benutzersystem geöffnet oder erstellt.
ms.assetid: cda632cf-6c92-48fb-aef1-25b320affd3e
title: Verwenden der MRU-Quell Liste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dbecb9e32a554d1818661b1fd7f6e782744c16e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959424"
---
# <a name="using-the-mru-source-list"></a>Verwenden der MRU-Quell Liste

Mit der [**setupsetsourcelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetsourcelista) -Funktion wird eine Quell Liste im System des Benutzers geöffnet oder erstellt. Sie können angeben, um die Benutzerliste, die System Liste, eine Kombination aus Benutzer-und System Listen oder eine temporäre Liste als MRU-Quell Liste festzulegen. Wenn eine temporäre Liste verwendet wird, ist dies die einzige Liste, die für die Setup Anwendung verfügbar ist, bis [**setupcanceltemporarysourcelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupcanceltemporarysourcelist) aufgerufen wird, oder **setupsetsourcelist** ein zweites Mal aufgerufen wird.

Nachdem eine Liste festgelegt wurde, können Sie die Quell Liste mithilfe von [**setupquerysourcelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista) Abfragen, um ein Array der Quell Pfade abzurufen. Wenn das Quell Listen Array nicht mehr benötigt wird, müssen Sie die [**setupfreesourcelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupfreesourcelista) -Funktion aufrufen, um die von [**setupquerysourcelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista)zugeordneten Ressourcen freizugeben.

Zum Hinzufügen eines Pfads zu einer Quell Liste, entweder im System des Benutzers oder in einer temporären Liste, rufen Sie [**setupaddto SourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtosourcelista)auf. Wenn die angegebene Quell Liste nicht temporär ist, verbleibt diese Quelle im System des Benutzers und kann für nachfolgende Installationen aufgerufen werden.

Um einen Pfad aus dem Quellpfad zu entfernen, rufen Sie die [**setupremuvefromsourcelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromsourcelista) -Funktion auf.

 

 



