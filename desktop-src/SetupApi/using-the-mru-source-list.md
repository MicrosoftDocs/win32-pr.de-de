---
description: Die SetupSetSourceList-Funktion öffnet oder erstellt eine Quellliste auf dem Benutzersystem.
ms.assetid: cda632cf-6c92-48fb-aef1-25b320affd3e
title: Verwenden der MRU-Quellliste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada1fa55a1c0defea2f344200eb331b8031dedfa66336510fb55b6fb77213a24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100630"
---
# <a name="using-the-mru-source-list"></a>Verwenden der MRU-Quellliste

Die [**SetupSetSourceList-Funktion**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetsourcelista) öffnet oder erstellt eine Quellliste auf dem System des Benutzers. Sie können angeben, dass die Benutzerliste, die Systemliste, eine Kombination aus Benutzer- und Systemlisten oder eine temporäre Liste als MRU-Quellliste festgelegt werden soll. Wenn eine temporäre Liste verwendet wird, ist sie die einzige Liste, die für die Setupanwendung verfügbar ist, bis [**SetupCancelTemporarySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcanceltemporarysourcelist) aufgerufen wird oder **SetupSetSourceList** ein zweites Mal aufgerufen wird.

Nachdem eine Liste festgelegt wurde, können Sie die Quellliste abfragen, indem Sie [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista) verwenden, um ein Array der Quellpfade abzurufen. Wenn das Quelllistenarray nicht mehr benötigt wird, müssen Sie die [**SetupFreeSourceList-Funktion**](/windows/desktop/api/Setupapi/nf-setupapi-setupfreesourcelista) aufrufen, um die von [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista)zugeordneten Ressourcen frei zu machen.

Rufen Sie [**SetupAddToSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtosourcelista)auf, um einer Quellliste entweder einen Pfad hinzuzufügen, der sich im System des Benutzers befindet, oder eine temporäre Liste. Wenn die angegebene Quellliste nicht temporär ist, verbleibt diese Quelle auf dem System des Benutzers und ist für nachfolgende Installationen zugänglich.

Um einen Pfad aus dem Quellpfad zu entfernen, rufen Sie die [**SetupRemoveFromSourceList-Funktion**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromsourcelista) auf.

 

 



