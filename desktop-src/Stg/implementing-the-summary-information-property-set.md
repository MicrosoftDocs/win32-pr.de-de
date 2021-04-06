---
title: Implementieren des Eigenschaften Satzes für Zusammenfassungs Informationen
description: Es gibt Richtlinien, die Sie beachten müssen, wenn Sie eine Zusammenfassungs Informations Eigenschaft für den strukturierten Speicher implementieren.
ms.assetid: e1204de5-b712-4bd5-bffb-6a12ec8d7052
keywords:
- Implementieren des Eigenschaften Satzes für Zusammenfassungs Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69e5ae6208aa5cb7a325d1cccf77f17e969c5b75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707301"
---
# <a name="implementing-the-summary-information-property-set"></a><span data-ttu-id="28a6d-104">Implementieren des Eigenschaften Satzes für Zusammenfassungs Informationen</span><span class="sxs-lookup"><span data-stu-id="28a6d-104">Implementing the Summary Information Property Set</span></span>

<span data-ttu-id="28a6d-105">Es gibt Richtlinien, die Sie beachten müssen, wenn Sie eine Zusammenfassungs Informations Eigenschaft für den strukturierten Speicher implementieren.</span><span class="sxs-lookup"><span data-stu-id="28a6d-105">There are guidelines to follow when implementing a summary information property set for Structured Storage.</span></span>

<span data-ttu-id="28a6d-106">Im folgenden sind die Richtlinien für die Implementierung [des Eigenschaften Satzes für Zusammenfassungs Informationen](the-summary-information-property-set.md)aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="28a6d-106">The following are the guidelines for implementing [The Summary Information Property Set](the-summary-information-property-set.md):</span></span>

-   <span data-ttu-id="28a6d-107">**PID \_ Die Vorlage** verweist auf ein externes Dokument, das Format-und Stil Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="28a6d-107">**PID\_TEMPLATE** refers to an external document containing format and style information.</span></span> <span data-ttu-id="28a6d-108">Der Prozess, mit dem sich die Vorlage befindet, ist Implementierungs definiert.</span><span class="sxs-lookup"><span data-stu-id="28a6d-108">The process by which the template is located is implementation-defined.</span></span>
-   <span data-ttu-id="28a6d-109">**PID \_ Lastauthor** ist der Name, der von der Anwendung in Benutzerinformationen gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="28a6d-109">**PID\_LASTAUTHOR** is the name stored in User Information by the application.</span></span> <span data-ttu-id="28a6d-110">Mary erstellt z. b. ein Dokument auf dem Computer und übergibt es John, das es dann ändert und speichert.</span><span class="sxs-lookup"><span data-stu-id="28a6d-110">For example, Mary creates a document on her computer and gives it to John, who then modifies and saves it.</span></span> <span data-ttu-id="28a6d-111">Mary ist Autor, John ist der letzte gespeicherte Wert.</span><span class="sxs-lookup"><span data-stu-id="28a6d-111">Mary is the author, John is the last saved by value.</span></span>
-   <span data-ttu-id="28a6d-112">**PID \_ "Revnumber** " gibt an, wie oft der Datei-/Speicherbefehl für dieses Dokument aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="28a6d-112">**PID\_REVNUMBER** is the number of times the File/Save command has been called on this document.</span></span>
-   <span data-ttu-id="28a6d-113">Alle Datums-/Uhrzeitwerte müssen in UTC (Universal koordinierte Time) gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="28a6d-113">Each of the date/time values must be stored in Universal Coordinated Time (UTC).</span></span>
-   <span data-ttu-id="28a6d-114">**PID \_ Create \_ DTM** ist eine schreibgeschützte Eigenschaft. Diese Eigenschaft sollte beim Erstellen eines Dokuments festgelegt werden, sollte jedoch nicht später geändert werden.</span><span class="sxs-lookup"><span data-stu-id="28a6d-114">**PID\_CREATE\_DTM** is a read-only property; this property should be set when a document is created, but should not be subsequently changed.</span></span>
-   <span data-ttu-id="28a6d-115">Für die **PID- \_ Miniaturansicht** sollten Anwendungen Daten im **CF- \_ DIB** -oder **CF- \_ MetafilePict** -Format speichern.</span><span class="sxs-lookup"><span data-stu-id="28a6d-115">For **PID\_THUMBNAIL**, applications should store data in **CF\_DIB** or **CF\_METAFILEPICT** format.</span></span> <span data-ttu-id="28a6d-116">**CF \_ MetafilePict** wird empfohlen.</span><span class="sxs-lookup"><span data-stu-id="28a6d-116">**CF\_METAFILEPICT** is recommended.</span></span>
-   <span data-ttu-id="28a6d-117">**PID \_ Sicherheit** ist die empfohlene Sicherheitsstufe für das Dokument.</span><span class="sxs-lookup"><span data-stu-id="28a6d-117">**PID\_SECURITY** is the suggested security level for the document.</span></span> <span data-ttu-id="28a6d-118">Durch die Angabe der Sicherheitsstufe für das Dokument kann eine andere Anwendung als der Absender des Dokuments die Benutzeroberfläche an die Eigenschaften anpassen.</span><span class="sxs-lookup"><span data-stu-id="28a6d-118">By noting the security level on the document, an application other than the originator of the document can adjust its user interface to the properties.</span></span> <span data-ttu-id="28a6d-119">In einer Anwendung sollten keine Informationen zu einem Kenn Wort geschützten Dokument angezeigt werden, oder es sollten keine Änderungen an den Erzwingung Read-Only oder auf Dokumente mit gesperrten Anmerkungen vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="28a6d-119">An application should not display any information about a password-protected document or enable modifications to enforced Read-Only or Locked-for-Annotations documents.</span></span> <span data-ttu-id="28a6d-120">Wenn der Benutzer versucht, Eigenschaften zu ändern, sollte die Anwendung den Benutzer über den Read-Only empfohlenen Status warnen.</span><span class="sxs-lookup"><span data-stu-id="28a6d-120">If the user attempts to modify properties, the application should warn the user about the Read-Only Recommended status.</span></span>



| <span data-ttu-id="28a6d-121">Sicherheitsstufe</span><span class="sxs-lookup"><span data-stu-id="28a6d-121">Security level</span></span>         | <span data-ttu-id="28a6d-122">Wert</span><span class="sxs-lookup"><span data-stu-id="28a6d-122">Value</span></span> |
|------------------------|-------|
| <span data-ttu-id="28a6d-123">Keine</span><span class="sxs-lookup"><span data-stu-id="28a6d-123">None</span></span>                   | <span data-ttu-id="28a6d-124">0</span><span class="sxs-lookup"><span data-stu-id="28a6d-124">0</span></span>     |
| <span data-ttu-id="28a6d-125">Kennwort geschützt</span><span class="sxs-lookup"><span data-stu-id="28a6d-125">Password protected</span></span>     | <span data-ttu-id="28a6d-126">1</span><span class="sxs-lookup"><span data-stu-id="28a6d-126">1</span></span>     |
| <span data-ttu-id="28a6d-127">Nur Lesen empfohlen</span><span class="sxs-lookup"><span data-stu-id="28a6d-127">Read-only recommended</span></span>  | <span data-ttu-id="28a6d-128">2</span><span class="sxs-lookup"><span data-stu-id="28a6d-128">2</span></span>     |
| <span data-ttu-id="28a6d-129">Schreibgeschützt erzwungen</span><span class="sxs-lookup"><span data-stu-id="28a6d-129">Read-only enforced</span></span>     | <span data-ttu-id="28a6d-130">4</span><span class="sxs-lookup"><span data-stu-id="28a6d-130">4</span></span>     |
| <span data-ttu-id="28a6d-131">Für Anmerkungen gesperrt</span><span class="sxs-lookup"><span data-stu-id="28a6d-131">Locked for annotations</span></span> | <span data-ttu-id="28a6d-132">8</span><span class="sxs-lookup"><span data-stu-id="28a6d-132">8</span></span>     |



 

 

 




