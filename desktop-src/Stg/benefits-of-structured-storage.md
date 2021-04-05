---
title: Vorteile von strukturiertem Speicher
description: COM stellt eine Reihe von Diensten bereit, die kollektiv als strukturierte Speicherung bezeichnet werden.
ms.assetid: d05d2dbc-d1d2-4ef8-a773-5337e2746da3
keywords:
- Strukturierter Speicherplatz Halter, Vorteile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68b954fda33e18f654ccc0360f58ddb14e5d110
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708208"
---
# <a name="benefits-of-structured-storage"></a><span data-ttu-id="e71b3-104">Vorteile von strukturiertem Speicher</span><span class="sxs-lookup"><span data-stu-id="e71b3-104">Benefits of Structured Storage</span></span>

<span data-ttu-id="e71b3-105">COM stellt eine Reihe von Diensten bereit, die kollektiv als strukturierte Speicherung bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="e71b3-105">COM provides a set of services collectively called structured storage.</span></span> <span data-ttu-id="e71b3-106">Zu den Vorteilen dieser Dienste gehört die Verringerung der Leistungseinbußen und des Aufwands, die mit dem Speichern von separaten Objekten in einer Flatfile verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="e71b3-106">Among the benefits of these services is the reduction of performance penalties and overhead associated with storing separate objects in a flat file.</span></span> <span data-ttu-id="e71b3-107">Anstelle einer Flatfile speichert com die separaten Objekte in einer einzelnen, strukturierten Datei, die aus zwei Hauptelementen besteht: Speicher Objekte und Streamobjekte.</span><span class="sxs-lookup"><span data-stu-id="e71b3-107">Instead of a flat file, COM stores the separate objects in a single, structured file consisting of two main elements: storage objects and stream objects.</span></span> <span data-ttu-id="e71b3-108">In der gleichen Weise funktionieren Sie wie ein Dateisystem in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="e71b3-108">Together, they function like a file system within a file.</span></span>

<span data-ttu-id="e71b3-109">Durch die strukturierte Speicherung werden Leistungsprobleme gelöst, da eine Datei nicht vollständig in den Speicher geschrieben werden muss, wenn einer Verbund Datei ein neues Objekt hinzugefügt wird oder ein vorhandenes Objekt vergrößert wird.</span><span class="sxs-lookup"><span data-stu-id="e71b3-109">Structured storage solves performance problems by eliminating the need to totally rewrite a file to storage whenever a new object is added to a compound file, or an existing object increases in size.</span></span> <span data-ttu-id="e71b3-110">Die neuen Daten werden an den nächsten verfügbaren Speicherort im permanenten Speicher geschrieben, und das Speicher Objekt aktualisiert die Tabelle mit den Zeigern, die Sie verwaltet, um die Speicherorte der Speicher Objekte und Streamobjekte zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="e71b3-110">The new data is written to the next available location in permanent storage, and the storage object updates the table of pointers it maintains to track the locations of its storage objects and stream objects.</span></span> <span data-ttu-id="e71b3-111">Gleichzeitig ermöglicht die strukturierte Speicherung es Endbenutzern, eine Verbund Datei zu interagieren und zu verwalten, als ob es sich um eine einzelne Datei und nicht um eine geschachtelte Hierarchy von separaten Objekten handelt.</span><span class="sxs-lookup"><span data-stu-id="e71b3-111">At the same time, structured storage enables end users to interact and manage a compound file as if it were a single file rather than a nested hierarchy of separate objects.</span></span>

<span data-ttu-id="e71b3-112">Die strukturierte Speicherung bietet auch andere Vorteile:</span><span class="sxs-lookup"><span data-stu-id="e71b3-112">Structured storage also has other benefits:</span></span>

-   <span data-ttu-id="e71b3-113">**Inkrementeller Zugriff**</span><span class="sxs-lookup"><span data-stu-id="e71b3-113">**Incremental access**.</span></span> <span data-ttu-id="e71b3-114">Wenn ein Benutzer Zugriff auf ein Objekt innerhalb einer Verbund Datei benötigt, kann der Benutzer nur dieses Objekt laden und speichern, und nicht die gesamte Datei.</span><span class="sxs-lookup"><span data-stu-id="e71b3-114">If a user needs access to an object within a compound file, the user can load and save only that object, rather than the entire file.</span></span>
-   <span data-ttu-id="e71b3-115">**Mehrfache Verwendung**.</span><span class="sxs-lookup"><span data-stu-id="e71b3-115">**Multiple use**.</span></span> <span data-ttu-id="e71b3-116">Mehr als ein Endbenutzer oder eine Anwendung kann gleichzeitig Informationen in derselben Verbund Datei lesen und schreiben.</span><span class="sxs-lookup"><span data-stu-id="e71b3-116">More than one end user or application can concurrently read and write information in the same compound file.</span></span>
-   <span data-ttu-id="e71b3-117">**Transaktionsverarbeitung**.</span><span class="sxs-lookup"><span data-stu-id="e71b3-117">**Transaction processing**.</span></span> <span data-ttu-id="e71b3-118">Benutzer können com-Verbund Dateien im transaktiven Modus lesen oder schreiben, in dem die an der Datei vorgenommenen Änderungen gepuffert werden und anschließend entweder ein Commit in die Datei erfolgen oder umgekehrt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e71b3-118">Users can read or write to COM compound files in transacted mode, where changes made to the file are buffered and can subsequently either be committed to the file or reversed.</span></span>
-   <span data-ttu-id="e71b3-119">Speicherungen mit **geringem Arbeitsspeicher**.</span><span class="sxs-lookup"><span data-stu-id="e71b3-119">**Low-memory saves**.</span></span> <span data-ttu-id="e71b3-120">Strukturierter Speicher bietet Funktionen zum Speichern von Dateien in Situationen mit geringem Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="e71b3-120">Structured storage provides facilities for saving files in low-memory situations.</span></span>

 

 




