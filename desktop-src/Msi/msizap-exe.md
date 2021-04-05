---
description: Msizap.exe ist ein Befehlszeilenprogramm, das entweder alle Windows Installer Informationen für ein Produkt oder alle auf einem Computer installierten Produkte entfernt. Produkte, die vom Installationsprogramm installiert werden, funktionieren möglicherweise nicht mehr, nachdem msizap verwendet wurde.
ms.assetid: 0debb8ab-3ae7-447e-84fc-0466ec1b2f26
title: Msizap.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a89f2287443bc442ee767b01e975d6bcc118c1d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042072"
---
# <a name="msizapexe"></a><span data-ttu-id="3b75b-104">Msizap.exe</span><span class="sxs-lookup"><span data-stu-id="3b75b-104">Msizap.exe</span></span>

<span data-ttu-id="3b75b-105">Msizap.exe ist ein Befehlszeilenprogramm, das entweder alle Windows Installer Informationen für ein Produkt oder alle auf einem Computer installierten Produkte entfernt.</span><span class="sxs-lookup"><span data-stu-id="3b75b-105">Msizap.exe is a command line utility that removes either all Windows Installer information for a product or all products installed on a computer.</span></span> <span data-ttu-id="3b75b-106">Produkte, die vom Installationsprogramm installiert werden, funktionieren möglicherweise nicht mehr, nachdem msizap verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="3b75b-106">Products installed by the installer may fail to function after using Msizap.</span></span>

<span data-ttu-id="3b75b-107">Unter Windows 2000 und Windows XP sind Administratorrechte erforderlich, um Msizap.exe zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="3b75b-107">On Windows 2000 and Windows XP, administrative privileges are required to use Msizap.exe.</span></span>

<span data-ttu-id="3b75b-108">Dieses Tool ist nur in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md) verfügbar und sollte nicht weiter verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="3b75b-108">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md) and should not be redistributed.</span></span> <span data-ttu-id="3b75b-109">Verwenden Sie die aktuelle Version von Msizap.exe (Version 3.1.4000.2726 oder höher), die in den Windows SDK Komponenten für Windows Installer Entwickler für Windows Vista oder höher verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3b75b-109">Use the recent version of Msizap.exe (version 3.1.4000.2726 or greater) that is available in the Windows SDK Components for Windows Installer Developers for Windows Vista or greater.</span></span> <span data-ttu-id="3b75b-110">Kleinere Versionen von Msizap.exe können Informationen zu allen Updates entfernen, die auf andere Anwendungen auf dem Computer des Benutzers angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="3b75b-110">Lesser versions of Msizap.exe can remove information about all updates that have been applied to other applications on the user's computer.</span></span> <span data-ttu-id="3b75b-111">Wenn diese Informationen entfernt werden, müssen diese anderen Anwendungen möglicherweise entfernt und erneut installiert werden, um weitere Updates zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3b75b-111">If this information is removed, these other applications may need to be removed and reinstalled to receive additional updates.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b75b-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b75b-112">Syntax</span></span>

<span data-ttu-id="3b75b-113">**msizap T**_\[ WA! \] {Product Code}_</span><span class="sxs-lookup"><span data-stu-id="3b75b-113">**msizap T**_\[WA!\]{product code}_</span></span>

<span data-ttu-id="3b75b-114">**msizap T**_\[ WA! \] <msi package>_</span><span class="sxs-lookup"><span data-stu-id="3b75b-114">**msizap T**_\[WA!\]<msi package>_</span></span>

<span data-ttu-id="3b75b-115">\**msizap \* \*\*\* \[ WA! \]* **Allproducts**</span><span class="sxs-lookup"><span data-stu-id="3b75b-115">\**msizap \*\*\*\*\[WA!\]* **ALLPRODUCTS**</span></span>

<span data-ttu-id="3b75b-116">**msizap pwsa?**</span><span class="sxs-lookup"><span data-stu-id="3b75b-116">**msizap PWSA?!**</span></span>

## <a name="command-line-options"></a><span data-ttu-id="3b75b-117">Befehlszeilenoptionen</span><span class="sxs-lookup"><span data-stu-id="3b75b-117">Command Line Options</span></span>

<span data-ttu-id="3b75b-118">Msizap.exe verwendet die in der folgenden Tabelle aufgeführten Befehlszeilenoptionen ohne Beachtung der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="3b75b-118">Msizap.exe uses case-insensitive command line options shown in the following table.</span></span>



| <span data-ttu-id="3b75b-119">Option</span><span class="sxs-lookup"><span data-stu-id="3b75b-119">Option</span></span> | <span data-ttu-id="3b75b-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3b75b-120">Description</span></span>                                                                                                                                                                                                                                                   |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*     | <span data-ttu-id="3b75b-121">Entfernt alle Windows Installer Ordner und Registrierungsschlüssel, passt die Anzahl der freigegebenen DLL an und beendet Windows Installer Dienst.</span><span class="sxs-lookup"><span data-stu-id="3b75b-121">Removes all Windows Installer folders and registry keys, adjusts shared DLL counts, and stops Windows Installer service.</span></span> <span data-ttu-id="3b75b-122">Entfernt auch die In-Progress Key-und Rollback-Informationen.</span><span class="sxs-lookup"><span data-stu-id="3b75b-122">Also removes the In-Progress key and rollback information.</span></span>                                                                           |
| <span data-ttu-id="3b75b-123">a</span><span class="sxs-lookup"><span data-stu-id="3b75b-123">a</span></span>      | <span data-ttu-id="3b75b-124">Ändert die Zugriffs Steuerungs Liste für alle angegebenen Entfernungs Vorgänge nur in den Administrator.</span><span class="sxs-lookup"><span data-stu-id="3b75b-124">Only changes ACLs to Admin Full Control for any specified removal.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="3b75b-125">g</span><span class="sxs-lookup"><span data-stu-id="3b75b-125">g</span></span>      | <span data-ttu-id="3b75b-126">Entfernt alle zwischengespeicherten Windows Installer Datendateien, die verwaist sind, für alle Benutzer.</span><span class="sxs-lookup"><span data-stu-id="3b75b-126">For all users, removes any cached Windows Installer data files that have been orphaned.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="3b75b-127">p</span><span class="sxs-lookup"><span data-stu-id="3b75b-127">p</span></span>      | <span data-ttu-id="3b75b-128">Entfernt den In-Progress Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="3b75b-128">Removes the In-Progress key.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="3b75b-129">s</span><span class="sxs-lookup"><span data-stu-id="3b75b-129">s</span></span>      | <span data-ttu-id="3b75b-130">Entfernt Rollback-Informationen.</span><span class="sxs-lookup"><span data-stu-id="3b75b-130">Removes Rollback Information.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="3b75b-131">t</span><span class="sxs-lookup"><span data-stu-id="3b75b-131">t</span></span>      | <span data-ttu-id="3b75b-132">Entfernt alle Informationen für den angegebenen Produktcode.</span><span class="sxs-lookup"><span data-stu-id="3b75b-132">Removes all information for the specified product code.</span></span> <span data-ttu-id="3b75b-133">Wenn Sie diese Option verwenden, schließen Sie den Produkt Code in geschweiften Klammern ein.</span><span class="sxs-lookup"><span data-stu-id="3b75b-133">When using this option, enclose the Product Code in curly braces.</span></span> <span data-ttu-id="3b75b-134">Diese Option kann entweder mit dem vollständigen Pfad der MSI-Datei oder mit dem Produktcode verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3b75b-134">This option may be used with either the full path to the .msi file or with the product code.</span></span>                                        |
| <span data-ttu-id="3b75b-135">w</span><span class="sxs-lookup"><span data-stu-id="3b75b-135">w</span></span>      | <span data-ttu-id="3b75b-136">Entfernt Windows Installer Informationen für alle Benutzer.</span><span class="sxs-lookup"><span data-stu-id="3b75b-136">Removes Windows Installer information for all users.</span></span> <span data-ttu-id="3b75b-137">Wenn diese Option nicht festgelegt ist, werden nur die Informationen für den aktuellen Benutzer entfernt.</span><span class="sxs-lookup"><span data-stu-id="3b75b-137">When this option is not set, only the information for the current user is removed.</span></span> <span data-ttu-id="3b75b-138">Wenn Sie diese Option verwenden, muss das Profil des Benutzers geladen werden, damit die benutzerspezifische Registrierungs Struktur des Benutzers verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3b75b-138">Use of this option requires that the user's profile be loaded so that the user's per-user registry hive be available.</span></span> |
| <span data-ttu-id="3b75b-139">?</span><span class="sxs-lookup"><span data-stu-id="3b75b-139">?</span></span>      | <span data-ttu-id="3b75b-140">Ausführliche Hilfe.</span><span class="sxs-lookup"><span data-stu-id="3b75b-140">Verbose help.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="3b75b-141">!</span><span class="sxs-lookup"><span data-stu-id="3b75b-141">!</span></span>      | <span data-ttu-id="3b75b-142">Erzwingt eine "yes"-Antwort auf eine beliebige Eingabeaufforderung.</span><span class="sxs-lookup"><span data-stu-id="3b75b-142">Forces a 'yes' response to any prompt.</span></span>                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="3b75b-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3b75b-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b75b-144">Veröffentlichte Versionen, Tools und verteilbare Dateien</span><span class="sxs-lookup"><span data-stu-id="3b75b-144">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



