---
title: Lizenzen
description: Lizenzen
ms.assetid: 74717519-bfd5-4a64-88eb-680d4bdfe74a
keywords:
- Windows Media-Format-SDK, Digital Rights Management (DRM)
- Windows Media-Format-SDK, DRM-Lizenzen
- Windows Media-Format-SDK, Lizenzen für DRM
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Digital Rights Management (DRM), geschützte Datei Lizenzierung
- DRM (Digital Rights Management), geschützte Datei Lizenzierung
- Lizenzen, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fbf2d7c0a25b2b19241d90743f43f46a71d7e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311261"
---
# <a name="licenses"></a><span data-ttu-id="5c759-111">Lizenzen</span><span class="sxs-lookup"><span data-stu-id="5c759-111">Licenses</span></span>

<span data-ttu-id="5c759-112">Eine Lizenz besteht aus einem Satz von Daten, die die Bedingungen beschreiben, unter denen Daten in geschützten Dateien gelesen werden können.</span><span class="sxs-lookup"><span data-stu-id="5c759-112">A license is a set of data that describes the conditions under which data in protected files can be read.</span></span> <span data-ttu-id="5c759-113">Jede Lizenz gilt für einen Schlüssel Bezeichner, der in der Regel einer einzelnen Mediendatei zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="5c759-113">Each license applies to a key identifier, which is typically assigned to a single media file.</span></span> <span data-ttu-id="5c759-114">Dieser Bezeichner wird verwendet, um den geschützten Inhalt in der Lizenz zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5c759-114">This identifier is what is used to identify the protected content in the license.</span></span>

<span data-ttu-id="5c759-115">Jede Lizenz gibt eine oder mehrere Aktionen an, die mit dem geschützten Inhalt ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="5c759-115">Each license specifies one or more actions that can be performed with the protected content.</span></span> <span data-ttu-id="5c759-116">Diese Aktionen, auch als Rechte bezeichnet, können auf verschiedene Weise eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="5c759-116">These actions, also called rights, can be limited in a number of ways.</span></span> <span data-ttu-id="5c759-117">Durch Kombinieren von Startdatums Angaben, Enddatums Angaben, Anzahlen und Zeitlimits kann der Aussteller der Lizenz nahezu jede vorstellbare Einschränkung auf der rechten Seite erstellen.</span><span class="sxs-lookup"><span data-stu-id="5c759-117">By combining start dates, end dates, counts, and time limits, the license issuer can create almost any imaginable limitation on a right.</span></span>

<span data-ttu-id="5c759-118">Lizenzen werden von einem Webdienst ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="5c759-118">Licenses are issued by a Web service.</span></span> <span data-ttu-id="5c759-119">Wenn eine Lizenz abgerufen wird, wird Sie auf dem Client Computer im lokalen Lizenz Speicher gespeichert. dabei handelt es sich um eine geschützte Datei, die Lizenzen und andere DRM-Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="5c759-119">When a license is acquired, it is stored on the client computer in the local license store, which is a protected file that contains licenses and other DRM data.</span></span> <span data-ttu-id="5c759-120">Wenn von einer Anwendung auf geschützte Inhalte zugegriffen wird, durchsucht das DRM-Subsystem den lokalen Lizenz Speicher nach einer Lizenz, die das entsprechende Recht erteilt.</span><span class="sxs-lookup"><span data-stu-id="5c759-120">When protected content is accessed by an application, the DRM subsystem searches the local license store for a license that grants the appropriate right.</span></span> <span data-ttu-id="5c759-121">Wenn keine Lizenz gefunden wird, kann die Anwendung eine auf der Grundlage von Informationen abrufen, die im DRM-Header der Datei gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="5c759-121">If no license is found, the application can acquire one based on information stored in the DRM header of the file.</span></span>

<span data-ttu-id="5c759-122">Für dieselbe geschützte Datei können mehrere Lizenzen ausgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5c759-122">Multiple licenses can be issued for the same protected file.</span></span> <span data-ttu-id="5c759-123">Wenn das DRM-Subsystem bestimmt, ob eine Aktion zulässig ist, aggregiert es die Rechte von allen zugewiesenen Lizenzen.</span><span class="sxs-lookup"><span data-stu-id="5c759-123">When the DRM subsystem determines whether an action is allowed, it aggregates the rights from all licenses that apply.</span></span> <span data-ttu-id="5c759-124">Jeder Lizenz kann eine Priorität zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="5c759-124">Each license can be assigned a priority.</span></span> <span data-ttu-id="5c759-125">Wenn mehr als eine Lizenz für eine Aktion gilt, wird die Lizenz mit der höchsten Priorität geprüft, um festzustellen, ob die Anzahl dekrementiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="5c759-125">If more than one license applies to an action, the highest priority license is checked to determine whether counts need to be decremented.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c759-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5c759-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c759-127">**Konzepte**</span><span class="sxs-lookup"><span data-stu-id="5c759-127">**Concepts**</span></span>](drmconcepts.md)
</dt> </dl>

 

 




