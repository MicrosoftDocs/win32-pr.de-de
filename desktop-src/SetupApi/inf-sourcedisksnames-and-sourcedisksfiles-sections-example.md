---
description: Im Abschnitt "SourceDisksNames" einer INF-Datei werden die Datenträger identifiziert, die die zu installierenden Quelldateien enthalten.
ms.assetid: af4bc466-f0a3-4f83-adb7-6bfc276f7764
title: INF SourceDisksNames-und SourceDisksFiles-Abschnitte (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f991727a8a2ca9cce2bd2d7161dfbf27b62ce74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349986"
---
# <a name="inf-sourcedisksnames-and-sourcedisksfiles-sections-example"></a><span data-ttu-id="0161d-103">INF SourceDisksNames-und SourceDisksFiles-Abschnitte (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="0161d-103">INF SourceDisksNames and SourceDisksFiles Sections Example</span></span>

<span data-ttu-id="0161d-104">Im Abschnitt " **SourceDisksNames** " einer INF-Datei werden die Datenträger identifiziert, die die zu installierenden Quelldateien enthalten.</span><span class="sxs-lookup"><span data-stu-id="0161d-104">The **SourceDisksNames** section of an INF file identifies the disks that contain the source files being installed.</span></span> <span data-ttu-id="0161d-105">Der Abschnitt **SourceDisksFiles** identifiziert die Quelldateien und die Quell Datenträger, die Sie enthalten.</span><span class="sxs-lookup"><span data-stu-id="0161d-105">The **SourceDisksFiles** section identifies the source files and the source disks that contain them.</span></span> <span data-ttu-id="0161d-106">Beachten Sie, dass die Plattformen mips, Alpha und PPC von Windows 2000 oder Windows XP nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="0161d-106">Note that MIPS, Alpha, and PPC platforms are not supported by Windows 2000 or Windows XP.</span></span>

<span data-ttu-id="0161d-107">Ab Windows XP kann ein **SourceDisksNames** -Abschnitt ein Tag und eine CAB-Datei angeben.</span><span class="sxs-lookup"><span data-stu-id="0161d-107">Beginning with Windows XP, a **SourceDisksNames** section may specify a tag as well as cabinet file.</span></span> <span data-ttu-id="0161d-108">Der folgende **SourceDisksNames** -Abschnitt kann z. b. für Wechsel Datenträger oder ein festes Medium verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0161d-108">For example, the following **SourceDisksNames** section may be used with removable or fixed media.</span></span> <span data-ttu-id="0161d-109">Wenn Sie Wechselmedien verwenden, überprüft der Beispiel Abschnitt, ob das Medium vorhanden ist, indem zuerst überprüft wird, ob das-Tag vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0161d-109">If using removable media, the example section verifies the presence of the media by first checking for the presence of the tag.</span></span> <span data-ttu-id="0161d-110">Wenn Sie ein festes Medium verwenden, überprüft der Beispiel Abschnitt, ob die Medien vorhanden sind, indem zuerst überprüft wird, ob die CAB-Anwendung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0161d-110">If using fixed media, the example section verifies the presence of the media by first checking for the presence of the cabinet.</span></span> <span data-ttu-id="0161d-111">Nachdem das vorhanden sein einer CAB-Datei überprüft wurde, versucht das System, Dateien aus der CAB-Datei zu kopieren, und fordert Sie zur Eingabe von Dateien auf, die nicht kopiert werden konnten.</span><span class="sxs-lookup"><span data-stu-id="0161d-111">After verifying the presence of a cabinet, the system attempts to copy files out of the cabinet and prompts for any files it was unable to copy.</span></span>

``` syntax
[SourceDisksNames]
1="Dajava" , "Dajava.cab",,, 0x10,"Dajava.tag"
```

<span data-ttu-id="0161d-112">Weitere Informationen zu **SourceDisksNames** oder **SourceDisksFiles** finden Sie in den Abschnitten "allgemeine Richtlinien für INF-Datei" und "INF-Datei Abschnitte und-Direktiven" des Microsoft Windows 2000 Driver Development Kit.</span><span class="sxs-lookup"><span data-stu-id="0161d-112">For more information about **SourceDisksNames** or **SourceDisksFiles**, see the "General Guidelines for INF File" and "INF File Sections and Directives" sections of the Microsoft Windows 2000 Driver Development Kit.</span></span>

 

 



