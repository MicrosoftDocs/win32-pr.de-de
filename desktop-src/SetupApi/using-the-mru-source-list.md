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
# <a name="using-the-mru-source-list"></a><span data-ttu-id="b66c8-103">Verwenden der MRU-Quell Liste</span><span class="sxs-lookup"><span data-stu-id="b66c8-103">Using the MRU Source List</span></span>

<span data-ttu-id="b66c8-104">Mit der [**setupsetsourcelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetsourcelista) -Funktion wird eine Quell Liste im System des Benutzers geöffnet oder erstellt.</span><span class="sxs-lookup"><span data-stu-id="b66c8-104">The [**SetupSetSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetsourcelista) function will open or create a source list on the user's system.</span></span> <span data-ttu-id="b66c8-105">Sie können angeben, um die Benutzerliste, die System Liste, eine Kombination aus Benutzer-und System Listen oder eine temporäre Liste als MRU-Quell Liste festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b66c8-105">You can specify to set the user list, the system list, a combination of the user and system lists, or a temporary list as the MRU source list.</span></span> <span data-ttu-id="b66c8-106">Wenn eine temporäre Liste verwendet wird, ist dies die einzige Liste, die für die Setup Anwendung verfügbar ist, bis [**setupcanceltemporarysourcelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupcanceltemporarysourcelist) aufgerufen wird, oder **setupsetsourcelist** ein zweites Mal aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b66c8-106">If a temporary list is used, it will be the only list available to the setup application until [**SetupCancelTemporarySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcanceltemporarysourcelist) is called, or **SetupSetSourceList** is called a second time.</span></span>

<span data-ttu-id="b66c8-107">Nachdem eine Liste festgelegt wurde, können Sie die Quell Liste mithilfe von [**setupquerysourcelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista) Abfragen, um ein Array der Quell Pfade abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b66c8-107">After a list is set, you can query the source list by using [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista) to obtain an array of the source paths.</span></span> <span data-ttu-id="b66c8-108">Wenn das Quell Listen Array nicht mehr benötigt wird, müssen Sie die [**setupfreesourcelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupfreesourcelista) -Funktion aufrufen, um die von [**setupquerysourcelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista)zugeordneten Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="b66c8-108">When the source list array is no longer needed, you must call the [**SetupFreeSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupfreesourcelista) function to free the resources allocated by [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista).</span></span>

<span data-ttu-id="b66c8-109">Zum Hinzufügen eines Pfads zu einer Quell Liste, entweder im System des Benutzers oder in einer temporären Liste, rufen Sie [**setupaddto SourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtosourcelista)auf.</span><span class="sxs-lookup"><span data-stu-id="b66c8-109">To add a path to a source list, either one that is resident on the user's system, or a temporary list, call [**SetupAddToSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtosourcelista).</span></span> <span data-ttu-id="b66c8-110">Wenn die angegebene Quell Liste nicht temporär ist, verbleibt diese Quelle im System des Benutzers und kann für nachfolgende Installationen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b66c8-110">If the source list specified is not temporary, that source will remain on the user's system and is accessible to subsequent installations.</span></span>

<span data-ttu-id="b66c8-111">Um einen Pfad aus dem Quellpfad zu entfernen, rufen Sie die [**setupremuvefromsourcelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromsourcelista) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="b66c8-111">To remove a path from the source path, call the [**SetupRemoveFromSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromsourcelista) function.</span></span>

 

 



