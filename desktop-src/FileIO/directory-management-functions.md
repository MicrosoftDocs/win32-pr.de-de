---
description: Funktionen, die in der Verzeichnis Verwaltung verwendet werden.
ms.assetid: 5517b0e7-2264-4173-8e10-ff7626458bfa
title: Verzeichnisverwaltungsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00bc10d0f8d7caddc1ea821c397e16edf600d92c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217657"
---
# <a name="directory-management-functions"></a><span data-ttu-id="d60f3-103">Verzeichnisverwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="d60f3-103">Directory Management Functions</span></span>

<span data-ttu-id="d60f3-104">Die folgenden Funktionen werden in der Verzeichnis Verwaltung verwendet.</span><span class="sxs-lookup"><span data-stu-id="d60f3-104">The following functions are used in directory management.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d60f3-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="d60f3-105">In this section</span></span>



| <span data-ttu-id="d60f3-106">Funktion</span><span class="sxs-lookup"><span data-stu-id="d60f3-106">Function</span></span>                                                                      | <span data-ttu-id="d60f3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d60f3-107">Description</span></span>                                                                                                                                                               |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d60f3-108">**CreateDirectory**</span><span class="sxs-lookup"><span data-stu-id="d60f3-108">**CreateDirectory**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya)<br/>                         | <span data-ttu-id="d60f3-109">Erstellt ein neues Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="d60f3-109">Creates a new directory.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="d60f3-110">**"Kreatedirectoriyex"**</span><span class="sxs-lookup"><span data-stu-id="d60f3-110">**CreateDirectoryEx**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa)<br/>                     | <span data-ttu-id="d60f3-111">Erstellt ein neues Verzeichnis mit den Attributen eines angegebenen Vorlagen Verzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="d60f3-111">Creates a new directory with the attributes of a specified template directory.</span></span><br/>                                                                                 |
| [<span data-ttu-id="d60f3-112">**"Kreatedirectoriytransagiert"**</span><span class="sxs-lookup"><span data-stu-id="d60f3-112">**CreateDirectoryTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda)<br/>     | <span data-ttu-id="d60f3-113">Erstellt ein neues Verzeichnis als transaktionalen Vorgang mit den Attributen eines angegebenen Vorlagen Verzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="d60f3-113">Creates a new directory as a transacted operation, with the attributes of a specified template directory.</span></span><br/>                                                      |
| [<span data-ttu-id="d60f3-114">**Findclosechangenotifizierung**</span><span class="sxs-lookup"><span data-stu-id="d60f3-114">**FindCloseChangeNotification**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification)<br/> | <span data-ttu-id="d60f3-115">Beendet die Überwachung des Änderungs Benachrichtigungs Handles.</span><span class="sxs-lookup"><span data-stu-id="d60f3-115">Stops change notification handle monitoring.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="d60f3-116">**FindFirstChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="d60f3-116">**FindFirstChangeNotification**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa)<br/> | <span data-ttu-id="d60f3-117">Erstellt ein Änderungs Benachrichtigungs Handle und richtet anfängliche Filterbedingungen für die Änderungs Benachrichtigung ein.</span><span class="sxs-lookup"><span data-stu-id="d60f3-117">Creates a change notification handle and sets up initial change notification filter conditions.</span></span><br/>                                                                |
| [<span data-ttu-id="d60f3-118">**FindNextChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="d60f3-118">**FindNextChangeNotification**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findnextchangenotification)<br/>   | <span data-ttu-id="d60f3-119">Fordert an, dass das Betriebssystem ein Änderungs Benachrichtigungs Handle signalisiert, wenn es das nächste Mal eine entsprechende Änderung erkennt.</span><span class="sxs-lookup"><span data-stu-id="d60f3-119">Requests that the operating system signal a change notification handle the next time it detects an appropriate change.</span></span><br/>                                         |
| [<span data-ttu-id="d60f3-120">**GetCurrentDirectory**</span><span class="sxs-lookup"><span data-stu-id="d60f3-120">**GetCurrentDirectory**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory)<br/>                 | <span data-ttu-id="d60f3-121">Ruft das aktuelle Verzeichnis für den aktuellen Prozess ab.</span><span class="sxs-lookup"><span data-stu-id="d60f3-121">Retrieves the current directory for the current process.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="d60f3-122">**"Read directoriychangesexw"**</span><span class="sxs-lookup"><span data-stu-id="d60f3-122">**ReadDirectoryChangesExW**</span></span>](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesexw)<br/>         | <span data-ttu-id="d60f3-123">Ruft Informationen ab, die die Änderungen im angegebenen Verzeichnis beschreiben. Diese können erweiterte Informationen enthalten, wenn dieser Informationstyp angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d60f3-123">Retrieves information that describes the changes within the specified directory, which can include extended information if that information type is specified.</span></span><br/> |
| [<span data-ttu-id="d60f3-124">**"Read directoriychangesw"**</span><span class="sxs-lookup"><span data-stu-id="d60f3-124">**ReadDirectoryChangesW**</span></span>](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)<br/>             | <span data-ttu-id="d60f3-125">Ruft Informationen ab, die die Änderungen im angegebenen Verzeichnis beschreiben.</span><span class="sxs-lookup"><span data-stu-id="d60f3-125">Retrieves information that describes the changes within the specified directory.</span></span><br/>                                                                               |
| [<span data-ttu-id="d60f3-126">**RemoveDirectory**</span><span class="sxs-lookup"><span data-stu-id="d60f3-126">**RemoveDirectory**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya)<br/>                         | <span data-ttu-id="d60f3-127">Löscht ein vorhandenes leeres Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="d60f3-127">Deletes an existing empty directory.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="d60f3-128">**Removedirectoriytransagiert**</span><span class="sxs-lookup"><span data-stu-id="d60f3-128">**RemoveDirectoryTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda)<br/>     | <span data-ttu-id="d60f3-129">Löscht ein vorhandenes leeres Verzeichnis als transaktiven Vorgang.</span><span class="sxs-lookup"><span data-stu-id="d60f3-129">Deletes an existing empty directory as a transacted operation.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="d60f3-130">**SetCurrentDirectory**</span><span class="sxs-lookup"><span data-stu-id="d60f3-130">**SetCurrentDirectory**</span></span>](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory)<br/>                 | <span data-ttu-id="d60f3-131">Ändert das aktuelle Verzeichnis für den aktuellen Prozess.</span><span class="sxs-lookup"><span data-stu-id="d60f3-131">Changes the current directory for the current process.</span></span><br/>                                                                                                         |



 

 

 




