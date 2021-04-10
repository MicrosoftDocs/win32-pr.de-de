---
title: Über Benutzeroberflächen übermittelte Nachrichten
description: In diesem Thema werden die Nachrichten aufgelistet, die von einem Verzeichnisdienst von einer Benutzeroberfläche gesendet werden können.
ms.assetid: c81a3c44-c01d-4029-8a7d-6e0911d4f5ab
ms.tgt_platform: multiple
keywords:
- Über Benutzeroberflächen übermittelte Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab0d01717129db284f05b2361b2a067d611a33e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036356"
---
# <a name="messages-communicated-through-user-interfaces"></a><span data-ttu-id="a571d-104">Über Benutzeroberflächen übermittelte Nachrichten</span><span class="sxs-lookup"><span data-stu-id="a571d-104">Messages Communicated through User Interfaces</span></span>

<span data-ttu-id="a571d-105">In diesem Thema werden die Nachrichten aufgelistet, die von einem Verzeichnisdienst von einer Benutzeroberfläche gesendet werden können.</span><span class="sxs-lookup"><span data-stu-id="a571d-105">This topic lists messages that a directory service can send from a user interface.</span></span>

## <a name="common-query-page-messages"></a><span data-ttu-id="a571d-106">Allgemeine Meldungen der Abfrage Seite</span><span class="sxs-lookup"><span data-stu-id="a571d-106">Common Query Page Messages</span></span>

<span data-ttu-id="a571d-107">Die folgenden Meldungen werden an eine Seite der Verzeichnisdienst-Abfrageformular Erweiterung in der [**cqpageproc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) -Rückruffunktion gesendet:</span><span class="sxs-lookup"><span data-stu-id="a571d-107">The following messages are sent to a directory service query form extension page in the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function:</span></span>

-   [<span data-ttu-id="a571d-108">**cqpm- \_ ClearForm**</span><span class="sxs-lookup"><span data-stu-id="a571d-108">**CQPM\_CLEARFORM**</span></span>](cqpm-clearform.md)
-   [<span data-ttu-id="a571d-109">**cqpm \_ aktivieren**</span><span class="sxs-lookup"><span data-stu-id="a571d-109">**CQPM\_ENABLE**</span></span>](cqpm-enable.md)
-   [<span data-ttu-id="a571d-110">**cqpm \_ GetParameters**</span><span class="sxs-lookup"><span data-stu-id="a571d-110">**CQPM\_GETPARAMETERS**</span></span>](cqpm-getparameters.md)
-   [<span data-ttu-id="a571d-111">**cqpm \_ handlerspecific**</span><span class="sxs-lookup"><span data-stu-id="a571d-111">**CQPM\_HANDLERSPECIFIC**</span></span>](cqpm-handlerspecific.md)
-   [<span data-ttu-id="a571d-112">**cqpm- \_ Hilfe**</span><span class="sxs-lookup"><span data-stu-id="a571d-112">**CQPM\_HELP**</span></span>](cqpm-help.md)
-   [<span data-ttu-id="a571d-113">**cqpm \_ initialisieren**</span><span class="sxs-lookup"><span data-stu-id="a571d-113">**CQPM\_INITIALIZE**</span></span>](cqpm-initialize.md)
-   [<span data-ttu-id="a571d-114">**cqpm \_ persistent speichern**</span><span class="sxs-lookup"><span data-stu-id="a571d-114">**CQPM\_PERSIST**</span></span>](cqpm-persist.md)
-   [<span data-ttu-id="a571d-115">**cqpm- \_ Version**</span><span class="sxs-lookup"><span data-stu-id="a571d-115">**CQPM\_RELEASE**</span></span>](cqpm-release.md)
-   [<span data-ttu-id="a571d-116">**cqpm \_ setdefaultparameters**</span><span class="sxs-lookup"><span data-stu-id="a571d-116">**CQPM\_SETDEFAULTPARAMETERS**</span></span>](cqpm-setdefaultparameters.md)

## <a name="miscellaneous-messages"></a><span data-ttu-id="a571d-117">Verschiedene Nachrichten</span><span class="sxs-lookup"><span data-stu-id="a571d-117">Miscellaneous Messages</span></span>

<span data-ttu-id="a571d-118">In der folgenden Tabelle werden die Nachrichten aufgelistet, die ein Verzeichnisdienst senden kann.</span><span class="sxs-lookup"><span data-stu-id="a571d-118">The following table lists messages that a directory service can send.</span></span>



| <span data-ttu-id="a571d-119">`Message`</span><span class="sxs-lookup"><span data-stu-id="a571d-119">Message</span></span>                  | <span data-ttu-id="a571d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a571d-120">Value</span></span>                     | <span data-ttu-id="a571d-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a571d-121">Description</span></span>                                                                                                                                                                                                                                   |
|--------------------------|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a571d-122">Dsprop \_ attrchanged-Meldung \_</span><span class="sxs-lookup"><span data-stu-id="a571d-122">DSPROP\_ATTRCHANGED\_MSG</span></span> | <span data-ttu-id="a571d-123">"Dspropattrchanged"</span><span class="sxs-lookup"><span data-stu-id="a571d-123">"DsPropAttrChanged"</span></span>       | <span data-ttu-id="a571d-124">Eine Meldung, die zum Synchronisieren von Eigenschaften Seiten und der Verzeichnisdienst-Verwaltungs Tools gesendet wurde, die in "DSClient. h" deklariert sind.</span><span class="sxs-lookup"><span data-stu-id="a571d-124">A message sent for synchronizing property pages and the directory service administration tools, declared in Dsclient.h.</span></span>                                                                                                                       |
| <span data-ttu-id="a571d-125">dsqpm \_ getclasslist</span><span class="sxs-lookup"><span data-stu-id="a571d-125">DSQPM\_GETCLASSLIST</span></span>      | <span data-ttu-id="a571d-126">Cqpm \_ handlerspecific + 0</span><span class="sxs-lookup"><span data-stu-id="a571d-126">CQPM\_HANDLERSPECIFIC+0</span></span>   | <span data-ttu-id="a571d-127">Eine Seiten Nachricht, die an die Formular Seiten zum Abrufen einer Liste von Klassen für die Abfrage gesendet wird, die von der Feldauswahl und der Eigenschaften Quelle verwendet werden, um die Liste der Anzeige Klassen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a571d-127">A page message sent to the form pages for retrieving a list of classes for query, used by the field selector and property well to build its list of display classes.</span></span> <span data-ttu-id="a571d-128">wParam = Flags und lParam = lplpdsqueryclasslist, deklariert in "dsquery. h".</span><span class="sxs-lookup"><span data-stu-id="a571d-128">wParam = flags and lParam = LPLPDSQUERYCLASSLIST, declared in Dsquery.h.</span></span> |
| <span data-ttu-id="a571d-129">Hilfe Themen zu dsqpm \_</span><span class="sxs-lookup"><span data-stu-id="a571d-129">DSQPM\_HELPTOPICS</span></span>        | <span data-ttu-id="a571d-130">(Cqpm \_ Handlerspecific + 1)</span><span class="sxs-lookup"><span data-stu-id="a571d-130">(CQPM\_HANDLERSPECIFIC+1)</span></span> | <span data-ttu-id="a571d-131">Eine Seiten Nachricht, die an die Formular Seiten zur Bearbeitung der "Hilfe Themen"-Anforderung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="a571d-131">A page message sent to the form pages for handling the "Help Topics" request.</span></span> <span data-ttu-id="a571d-132">wParam = 0, LPARAM = hwndParent, deklariert in "dsquery. h".</span><span class="sxs-lookup"><span data-stu-id="a571d-132">wParam = 0, lParam = hWndParent, declared in Dsquery.h.</span></span>                                                                                                         |



 

 

 




