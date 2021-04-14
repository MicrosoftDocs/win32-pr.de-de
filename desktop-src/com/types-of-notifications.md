---
title: Benachrichtigungs Typen
description: Benachrichtigungs Typen
ms.assetid: 1e7f44ea-f4ac-457e-96a3-94036508d7b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21216ca99e1a606aaba793371ad6b8619d13f2a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388582"
---
# <a name="types-of-notifications"></a><span data-ttu-id="5cfc2-103">Benachrichtigungs Typen</span><span class="sxs-lookup"><span data-stu-id="5cfc2-103">Types of Notifications</span></span>

<span data-ttu-id="5cfc2-104">Benachrichtigungen werden in drei Gruppen unterteilt: Verbund Dokument, Daten und Ansicht.</span><span class="sxs-lookup"><span data-stu-id="5cfc2-104">Notifications fall into three groups: compound document, data, and view.</span></span> <span data-ttu-id="5cfc2-105">Ein-Objekt sendet Verbund Dokument Benachrichtigungen als Antwort auf die Umbenennung, Speicherung, Schließung oder im Fall eines Links, wenn die zugehörige Verknüpfungs Quelle umbenannt wurde.</span><span class="sxs-lookup"><span data-stu-id="5cfc2-105">An object sends compound document notifications in response to being renamed, saved, closed or, in the case of a link, having its link source renamed.</span></span> <span data-ttu-id="5cfc2-106">Wie Sie erwarten, senden-Objekte Daten Benachrichtigungen als Reaktion auf Änderungen in Ihren Daten und senden Anzeige Benachrichtigungen als Reaktion auf Änderungen in der Präsentation.</span><span class="sxs-lookup"><span data-stu-id="5cfc2-106">As you would expect, objects send data notifications in response to changes in their data and send view notifications in response to changes in their presentation.</span></span> <span data-ttu-id="5cfc2-107">Container Anwendungen müssen für jeden dieser Benachrichtigungs Typen separat registriert werden, aber alle können von einer einzelnen Beratungs Senke verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="5cfc2-107">Container applications must register separately for each of these notification types, but all can be handled by a single advisory sink.</span></span>

<span data-ttu-id="5cfc2-108">Alle Container, der Objekt Handler und das verknüpfte Objekt werden für Verbund Dokument Benachrichtigungen registriert.</span><span class="sxs-lookup"><span data-stu-id="5cfc2-108">All containers, the object handler, and the linked object register for compound document notifications.</span></span> <span data-ttu-id="5cfc2-109">Der typische Container wird auch für Anzeige Benachrichtigungen registriert.</span><span class="sxs-lookup"><span data-stu-id="5cfc2-109">The typical container also registers for view notifications.</span></span> <span data-ttu-id="5cfc2-110">Daten Benachrichtigungen werden normalerweise an das verknüpfte Objekt und den Objekt Handler gesendet.</span><span class="sxs-lookup"><span data-stu-id="5cfc2-110">Data notifications are usually sent to both the linked object and object handler.</span></span> <span data-ttu-id="5cfc2-111">Ein spezieller Container, z. b. ein Container, der die Daten selbst rendert, kann vom Empfang von Daten Benachrichtigungen anstelle von Anzeige Benachrichtigungen profitieren.</span><span class="sxs-lookup"><span data-stu-id="5cfc2-111">A special purpose container, such as one that renders the data itself, might benefit from receiving data notifications instead of view notifications.</span></span> <span data-ttu-id="5cfc2-112">Beispielsweise kann ein eingebetteter Diagramm Container mit einem Link zu einer Tabelle für Daten Benachrichtigungen registriert werden.</span><span class="sxs-lookup"><span data-stu-id="5cfc2-112">For example, an embedded chart container with a link to a table can register for data notifications.</span></span> <span data-ttu-id="5cfc2-113">Da sich eine Änderung an der Tabelle auf das Diagramm auswirkt, würde der Empfang einer Daten Benachrichtigung den Container dazu leiten, die neuen tabellarischen Daten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5cfc2-113">Because a change to the table affects the chart, the receipt of a data notification would direct the container to get the new tabular data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5cfc2-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5cfc2-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cfc2-115">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="5cfc2-115">Notifications</span></span>](notifications.md)
</dt> </dl>

 

 




