---
description: ICE64 prüft, ob neue Verzeichnisse im Benutzerprofil in roamingszenarios ordnungsgemäß entfernt werden.
ms.assetid: d878bf4a-33c4-4c68-bd74-b7884d6680a5
title: ICE64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d103498a56bea26415f4f841d5ec78b5dfe370f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529585"
---
# <a name="ice64"></a><span data-ttu-id="d60e0-103">ICE64</span><span class="sxs-lookup"><span data-stu-id="d60e0-103">ICE64</span></span>

<span data-ttu-id="d60e0-104">ICE64 prüft, ob neue Verzeichnisse im Benutzerprofil in roamingszenarios ordnungsgemäß entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="d60e0-104">ICE64 checks that new directories in the user profile are removed correctly in roaming scenarios.</span></span>

<span data-ttu-id="d60e0-105">Wenn eine Warnung oder ein Fehler, der von ICE64 gemeldet wird, nicht behoben wird, führt dies im Allgemeinen zu Problemen bei der vollständigen Bereinigung des Computers während einer</span><span class="sxs-lookup"><span data-stu-id="d60e0-105">Failure to fix a warning or error reported by ICE64 generally leads to problems in completely cleaning the computer during an uninstallation.</span></span> <span data-ttu-id="d60e0-106">Wenn ein Roamingbenutzer, der die Anwendung installiert hat, sich zum ersten Mal bei einem Computer anmeldet, wird das gesamte Profil auf den Computer kopiert.</span><span class="sxs-lookup"><span data-stu-id="d60e0-106">When a roaming user who has installed the application logs on to a computer for the first time, all of the profile is copied down onto the computer.</span></span> <span data-ttu-id="d60e0-107">Bei einer Ankündigung (die nach dem Download des roamingprofils erfolgt) überprüft das Installationsprogramm, ob das Verzeichnis bereits vorhanden ist, und löscht es daher bei der Installation nicht.</span><span class="sxs-lookup"><span data-stu-id="d60e0-107">On advertisement (which takes place after the roaming profile download), the Installer verifies that the directory is already there and therefore does not delete it on uninstallation.</span></span> <span data-ttu-id="d60e0-108">Dadurch bleibt das Verzeichnis dauerhaft auf dem Computer des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="d60e0-108">This leaves the directory on the user's computer permanently.</span></span>

## <a name="result"></a><span data-ttu-id="d60e0-109">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="d60e0-109">Result</span></span>

<span data-ttu-id="d60e0-110">ICE64 gibt eine Warnung oder einen Fehler in einer roamingsituation aus, wenn ein neues Verzeichnis im Benutzerprofil, das entfernt werden soll, nicht entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d60e0-110">ICE64 posts a warning or an error in a roaming situation if a new directory in the user profile that should be removed is not removed.</span></span>

## <a name="example"></a><span data-ttu-id="d60e0-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d60e0-111">Example</span></span>

<span data-ttu-id="d60e0-112">ICE64 meldet den folgenden Fehler für das gezeigte Beispiel.</span><span class="sxs-lookup"><span data-stu-id="d60e0-112">ICE64 reports the following error for the example shown.</span></span>

``` syntax
The directory 'MyOtherFolder' is in the user profile but is not listed in the RemoveFile table.
```

<span data-ttu-id="d60e0-113">Der Ordner "myotherfolder" ist ein benutzerdefinierter Profilordner.</span><span class="sxs-lookup"><span data-stu-id="d60e0-113">The folder 'MyOtherFolder' is a custom profile folder.</span></span> <span data-ttu-id="d60e0-114">Da es nicht in der Tabelle "RemoveFile" aufgeführt ist, wird es in einigen Szenarios nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="d60e0-114">Because it is not listed in the RemoveFile table, it is not removed in some scenarios.</span></span>

<span data-ttu-id="d60e0-115">Um diesen Fehler zu beheben, erstellen Sie eine Zeile für den Ordner in der Tabelle "RemoveFile".</span><span class="sxs-lookup"><span data-stu-id="d60e0-115">To fix this error, create a row for the folder in the RemoveFile table.</span></span>

[<span data-ttu-id="d60e0-116">Verzeichnis Tabelle</span><span class="sxs-lookup"><span data-stu-id="d60e0-116">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="d60e0-117">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="d60e0-117">Directory</span></span>     | <span data-ttu-id="d60e0-118">Über \_ geordnetes Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="d60e0-118">Directory\_Parent</span></span> | <span data-ttu-id="d60e0-119">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="d60e0-119">DefaultDir</span></span>  |
|---------------|-------------------|-------------|
| <span data-ttu-id="d60e0-120">AppDataFolder</span><span class="sxs-lookup"><span data-stu-id="d60e0-120">AppDataFolder</span></span> | <span data-ttu-id="d60e0-121">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="d60e0-121">TARGETDIR</span></span>         |             |
| <span data-ttu-id="d60e0-122">MyFolder</span><span class="sxs-lookup"><span data-stu-id="d60e0-122">MyFolder</span></span>      | <span data-ttu-id="d60e0-123">AppDataFolder</span><span class="sxs-lookup"><span data-stu-id="d60e0-123">AppDataFolder</span></span>     | <span data-ttu-id="d60e0-124">DataFolder</span><span class="sxs-lookup"><span data-stu-id="d60e0-124">DataFolder</span></span>  |
| <span data-ttu-id="d60e0-125">Myotherfolder</span><span class="sxs-lookup"><span data-stu-id="d60e0-125">MyOtherFolder</span></span> | <span data-ttu-id="d60e0-126">AppDataFolder</span><span class="sxs-lookup"><span data-stu-id="d60e0-126">AppDataFolder</span></span>     | <span data-ttu-id="d60e0-127">DataFolder2</span><span class="sxs-lookup"><span data-stu-id="d60e0-127">DataFolder2</span></span> |



 

[<span data-ttu-id="d60e0-128">RemoveFile-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d60e0-128">RemoveFile Table</span></span>](removefile-table.md)



| <span data-ttu-id="d60e0-129">Filekey</span><span class="sxs-lookup"><span data-stu-id="d60e0-129">FileKey</span></span> | <span data-ttu-id="d60e0-130">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="d60e0-130">Component\_</span></span> | <span data-ttu-id="d60e0-131">FileName</span><span class="sxs-lookup"><span data-stu-id="d60e0-131">FileName</span></span> | <span data-ttu-id="d60e0-132">Dirproperty</span><span class="sxs-lookup"><span data-stu-id="d60e0-132">DirProperty</span></span> | <span data-ttu-id="d60e0-133">InstallMode</span><span class="sxs-lookup"><span data-stu-id="d60e0-133">InstallMode</span></span> |
|---------|-------------|----------|-------------|-------------|
| <span data-ttu-id="d60e0-134">Key1</span><span class="sxs-lookup"><span data-stu-id="d60e0-134">Key1</span></span>    | <span data-ttu-id="d60e0-135">Component1</span><span class="sxs-lookup"><span data-stu-id="d60e0-135">Component1</span></span>  |          | <span data-ttu-id="d60e0-136">MyFolder</span><span class="sxs-lookup"><span data-stu-id="d60e0-136">MyFolder</span></span>    | <span data-ttu-id="d60e0-137">2</span><span class="sxs-lookup"><span data-stu-id="d60e0-137">2</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="d60e0-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d60e0-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d60e0-139">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="d60e0-139">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



