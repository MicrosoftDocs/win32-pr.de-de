---
description: Eine Ereignis Referenzseite (ERP) ist ein HTML-Dokument, das Netzwerkmonitor Informationen zu Ereignissen bereitstellt, die während des Experten-oder Monitor Vorgangs erkannt werden.
ms.assetid: 097bae90-5dab-4f79-a829-648033b38016
title: Informationen zu Ereignis Verweis Seiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81e989e3e1d4ab0c41dc78c567c662e8a3090906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865468"
---
# <a name="about-event-reference-pages"></a><span data-ttu-id="00fcc-103">Informationen zu Ereignis Verweis Seiten</span><span class="sxs-lookup"><span data-stu-id="00fcc-103">About Event Reference Pages</span></span>

<span data-ttu-id="00fcc-104">Eine Ereignis Referenzseite (ERP) ist ein HTML-Dokument, das Netzwerkmonitor Informationen zu Ereignissen bereitstellt, die während des Experten-oder Monitor Vorgangs erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="00fcc-104">An event reference page (ERP) is an HTML document that provides Network Monitor information about events detected during expert or monitor operation.</span></span>

<span data-ttu-id="00fcc-105">Sie können Erps in der Ereignisanzeige Netzwerkmonitor, im Überwachungs Steuerungs Tool oder in einem beliebigen Browser anzeigen, der die HTML-Features von Microsoft Internet Explorer Version 4,01 oder höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="00fcc-105">You can view ERPs in the Event Viewer of Network Monitor, Monitor Control Tool, or in any browser that supports the HTML features of Microsoft Internet Explorer Version 4.01 or later.</span></span> <span data-ttu-id="00fcc-106">Das heißt, Sie können Ihrer ERP unterstützte Steuerelemente oder Skriptsprachen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="00fcc-106">That is, you can add supported controls or scripted languages into your ERP.</span></span>

<span data-ttu-id="00fcc-107">Erps werden jedoch nur angezeigt, wenn der Experte das HTML-Dokument anhand des Namens bestimmt.</span><span class="sxs-lookup"><span data-stu-id="00fcc-107">However, ERPs appear only if the expert designates the HTML document by name.</span></span> <span data-ttu-id="00fcc-108">Bei ordnungsgemäßer Festschreibung wird das ERP im unteren Bereich angezeigt, wenn das Ereignis im Ereignisanzeige ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="00fcc-108">When properly designated, the ERP appears in the lower pane when the event in the Event Viewer is selected.</span></span> <span data-ttu-id="00fcc-109">Die folgende Abbildung zeigt eine ERP, die dem IP-Bereichs Monitor (Internet Protocol) zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="00fcc-109">The figure below shows an ERP associated with the Internet Protocol (IP) Range monitor.</span></span>

![ein ERP, das mit dem IP-Bereichs Monitor verknüpft ist](images/exview2.png)

## <a name="expert-events"></a><span data-ttu-id="00fcc-111">Expertenereignisse</span><span class="sxs-lookup"><span data-stu-id="00fcc-111">Expert Events</span></span>

<span data-ttu-id="00fcc-112">Expertenereignisse werden vom **eventident** -Member einer [**nmeventdata**](nmeventdata.md) -Struktur identifiziert.</span><span class="sxs-lookup"><span data-stu-id="00fcc-112">Expert events are identified by the **EventIdent** member of an [**NMEVENTDATA**](nmeventdata.md) structure.</span></span> <span data-ttu-id="00fcc-113">Wenn Sie einen Experten schreiben, bestimmen Sie die **eventident** -Werte, die in der Regel 1, 2, 3 usw. lauten.</span><span class="sxs-lookup"><span data-stu-id="00fcc-113">When you write an expert you determine the **EventIdent** values, which are typically numbered 1, 2, 3, and so on.</span></span> <span data-ttu-id="00fcc-114">Nehmen wir beispielsweise an, dass ein Experte zwei Ereignisse generiert (**EventIdent1** und **EventIdent2**).</span><span class="sxs-lookup"><span data-stu-id="00fcc-114">For example, suppose that an expert generates two events (**EventIdent1** and **EventIdent2**).</span></span> <span data-ttu-id="00fcc-115">Wenn das Ereignisanzeige die Ereignisse separat anzeigen soll, müssen Sie zwei separate ERP-Dokumente erstellen.</span><span class="sxs-lookup"><span data-stu-id="00fcc-115">If you want the Event Viewer to display the events separately, you must create two separate ERP documents.</span></span>

 

 



