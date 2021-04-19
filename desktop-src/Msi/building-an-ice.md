---
description: Wenn Sie die internen Konsistenzprüfungen, die Sie benötigen, in den in der ICE-Referenz aufgeführten, benutzerdefinierten Ice-Aktionen nicht finden können, müssen Sie Ihr eigenes Eis vorbereiten, um das Paket zu überprüfen.
ms.assetid: d9ff43ee-8e7a-4132-ac2f-232dc24606d8
title: Aufbauen eines Eis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2de8dab0284a612723461d11b420ed1f22b244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349165"
---
# <a name="building-an-ice"></a><span data-ttu-id="6d0b3-103">Aufbauen eines Eis</span><span class="sxs-lookup"><span data-stu-id="6d0b3-103">Building An ICE</span></span>

<span data-ttu-id="6d0b3-104">Wenn Sie die [internen Konsistenz](internal-consistency-evaluators-ices.md) Prüfungen, die Sie benötigen, in den in der [Ice-Referenz](ice-reference.md)aufgeführten, benutzerdefinierten Ice-Aktionen nicht finden können, müssen Sie Ihr eigenes Eis vorbereiten, um das Paket zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="6d0b3-104">If you are unable to find the [Internal Consistency Evaluators](internal-consistency-evaluators-ices.md) you need among the existing ICE custom actions listed in the [ICE Reference](ice-reference.md), you will need to prepare your own ICE to validate your package.</span></span>

<span data-ttu-id="6d0b3-105">Wenn Sie benutzerdefinierte Ice-Aktionen erstellen, sollten Sie folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="6d0b3-105">When authoring ICE custom actions you should do the following:</span></span>

-   <span data-ttu-id="6d0b3-106">Basieren Sie auf den ICES nur auf benutzerdefinierte Aktionen der Typen, die in der angezeigten Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="6d0b3-106">Base the ICEs only on custom actions of types listed in the table shown.</span></span>
-   <span data-ttu-id="6d0b3-107">[**Msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) anrufen und einen installmessage- \_ Benutzertyp von Message veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="6d0b3-107">Call [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) and post an INSTALLMESSAGE\_USER type of message.</span></span> <span data-ttu-id="6d0b3-108">Befolgen Sie beim Erstellen von Ice-Nachrichten das Nachrichtenformat in den [Richtlinien](ice-message-guidelines.md)für die Ice-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="6d0b3-108">When authoring your ICE messages follow the message format in the [ICE Message Guidelines](ice-message-guidelines.md).</span></span>
-   <span data-ttu-id="6d0b3-109">Schreiben Sie Ihr Eis so, dass alle API-Fehler erfasst werden und immer Fehler erfolgreich zurückgegeben werden \_ .</span><span class="sxs-lookup"><span data-stu-id="6d0b3-109">Write your ICE such that it captures any API errors and always returns ERROR\_SUCCESS.</span></span> <span data-ttu-id="6d0b3-110">Dies ist erforderlich, damit nachfolgende benutzerdefinierte Aktionen nach dem Ausfall eines ICE ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="6d0b3-110">This is necessary to allow subsequent custom actions to run following the failure of an ICE.</span></span>

<span data-ttu-id="6d0b3-111">Benutzerdefinierte Ice-Aktionen sind auf die folgenden benutzerdefinierten Aktions Typen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="6d0b3-111">ICE custom actions are limited to the following custom action types.</span></span>



| <span data-ttu-id="6d0b3-112">Benutzerdefinierter Aktionstyp</span><span class="sxs-lookup"><span data-stu-id="6d0b3-112">Custom action type</span></span>                                 | <span data-ttu-id="6d0b3-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6d0b3-113">Description</span></span>               |
|----------------------------------------------------|---------------------------|
| [<span data-ttu-id="6d0b3-114">Benutzerdefinierter Aktionstyp 1</span><span class="sxs-lookup"><span data-stu-id="6d0b3-114">Custom Action Type 1</span></span>](custom-action-type-1.md)   | <span data-ttu-id="6d0b3-115">DLL im binären Stream</span><span class="sxs-lookup"><span data-stu-id="6d0b3-115">DLL in binary stream</span></span>      |
| [<span data-ttu-id="6d0b3-116">Benutzerdefinierter Aktionstyp 2</span><span class="sxs-lookup"><span data-stu-id="6d0b3-116">Custom Action Type 2</span></span>](custom-action-type-2.md)   | <span data-ttu-id="6d0b3-117">EXE im binären Stream</span><span class="sxs-lookup"><span data-stu-id="6d0b3-117">EXE in binary stream</span></span>      |
| [<span data-ttu-id="6d0b3-118">Benutzerdefinierter Aktionstyp 5</span><span class="sxs-lookup"><span data-stu-id="6d0b3-118">Custom Action Type 5</span></span>](custom-action-type-5.md)   | <span data-ttu-id="6d0b3-119">JScript im binären Stream</span><span class="sxs-lookup"><span data-stu-id="6d0b3-119">JScript in binary stream</span></span>  |
| [<span data-ttu-id="6d0b3-120">Benutzerdefinierter Aktionstyp 6</span><span class="sxs-lookup"><span data-stu-id="6d0b3-120">Custom Action Type 6</span></span>](custom-action-type-6.md)   | <span data-ttu-id="6d0b3-121">VBScript im binären Stream</span><span class="sxs-lookup"><span data-stu-id="6d0b3-121">VBScript in binary stream</span></span> |
| [<span data-ttu-id="6d0b3-122">Benutzerdefinierter Aktionstyp 37</span><span class="sxs-lookup"><span data-stu-id="6d0b3-122">Custom Action Type 37</span></span>](custom-action-type-37.md) | <span data-ttu-id="6d0b3-123">JScript-Code als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6d0b3-123">JScript code as string</span></span>    |
| [<span data-ttu-id="6d0b3-124">Benutzerdefinierter Aktionstyp 38</span><span class="sxs-lookup"><span data-stu-id="6d0b3-124">Custom Action Type 38</span></span>](custom-action-type-38.md) | <span data-ttu-id="6d0b3-125">VBScript-Code als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6d0b3-125">VBScript code as string</span></span>   |



 

<span data-ttu-id="6d0b3-126">Wenn Sie eine benutzerdefinierte Ice-Aktion erstellen, gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="6d0b3-126">When authoring an ICE custom action, do not do the following:</span></span>

-   <span data-ttu-id="6d0b3-127">Gehen Sie nicht davon aus, dass das Handle für die Engine, das das Ice empfängt, eine Installations Instanz der Installer-Datenbank ist.</span><span class="sxs-lookup"><span data-stu-id="6d0b3-127">Do not assume that the handle to the engine that the ICE receives is an installation instance of the installer database.</span></span> <span data-ttu-id="6d0b3-128">Wenn es sich nicht um eine-Installations Instanz handelt, werden bestimmte Eigenschaften nicht definiert, die Quell-und Zielverzeichnisse werden nicht aufgelöst, und die aktuellen Funktions Zustände sind nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="6d0b3-128">If it is not a installation instance, certain properties are not defined, the source and target directories are not resolved, and current feature states are not defined.</span></span>
-   <span data-ttu-id="6d0b3-129">Verlassen Sie sich weder auf die vorherige Ausführung noch auf die Nichtausführung von Installationsprogramm Aktionen, benutzerdefinierten Aktionen oder anderen Eis.</span><span class="sxs-lookup"><span data-stu-id="6d0b3-129">Do not rely on the prior execution, or non-execution, of any installer action, custom action, or another ICE.</span></span> <span data-ttu-id="6d0b3-130">Da ein vorheriger Ice temporäre Spalten in einer beliebigen Tabelle erstellt hat, sollten Autoren nach Möglichkeit nach Möglichkeit auf Spalten verweisen.</span><span class="sxs-lookup"><span data-stu-id="6d0b3-130">Because a prior ICE may have created temporary columns in any table, authors should reference columns by name whenever possible.</span></span> <span data-ttu-id="6d0b3-131">Der ICES sollte alle temporären Spalten oder Tabellen bereinigen, bevor Sie beendet werden.</span><span class="sxs-lookup"><span data-stu-id="6d0b3-131">ICEs should cleanup any temporary columns or tables before they exit.</span></span>
-   <span data-ttu-id="6d0b3-132">Gehen Sie nicht davon aus, dass die Autoren auf ein Bild des Quell Verzeichnisses der Datenbank zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="6d0b3-132">Do not assume that authors have access to an image of the source directory of the database.</span></span>
-   <span data-ttu-id="6d0b3-133">Gehen Sie nicht davon aus, dass die an der Datenbank vorgenommenen Änderungen nicht beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="6d0b3-133">Do not assume that changes made to the database do not persist.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d0b3-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6d0b3-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d0b3-135">Sample Ice in C++</span><span class="sxs-lookup"><span data-stu-id="6d0b3-135">Sample ICE in C++</span></span>](sample-ice-in-c-.md)
</dt> <dt>

[<span data-ttu-id="6d0b3-136">Sample Ice in VBScript</span><span class="sxs-lookup"><span data-stu-id="6d0b3-136">Sample ICE in VBScript</span></span>](sample-ice-in-vbscript.md)
</dt> </dl>

 

 



