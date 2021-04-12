---
description: Windows Installer wird als Dienst auf Computern mit 32-Bit-oder 64-Bit-Windows ausgeführt.
ms.assetid: c02fc401-0c9c-49f6-adcc-ed36bdb18fca
title: Informationen zu Windows Installer auf 64-Bit-Betriebssystemen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11fe9969a3fc1ccd9b63f6bd75b145f9dbc7d8c4
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/21/2021
ms.locfileid: "104218865"
---
# <a name="about-windows-installer-on-64-bit-operating-systems"></a><span data-ttu-id="cfe1f-103">Informationen zu Windows Installer auf 64-Bit-Betriebssystemen</span><span class="sxs-lookup"><span data-stu-id="cfe1f-103">About Windows Installer on 64-Bit Operating Systems</span></span>

<span data-ttu-id="cfe1f-104">Windows Installer wird als Dienst auf Computern mit 32-Bit-oder 64-Bit-Windows ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cfe1f-104">Windows Installer runs as a service on computers using 32-bit or 64-bit Windows.</span></span> <span data-ttu-id="cfe1f-105">Versionen des Installationsprogramms vor Version 2,0 können 32-Bit-Windows Installer Pakete nur unter 32-Bit-Betriebssystemen installieren und verwalten.</span><span class="sxs-lookup"><span data-stu-id="cfe1f-105">Versions of the installer earlier than version 2.0 can install and manage 32-bit Windows Installer Packages only on 32-bit operating systems.</span></span> <span data-ttu-id="cfe1f-106">Beachten Sie, dass Sie eine 64-Bit-Anwendung auf einem 32-Bit-Betriebssystem nicht ankündigen oder installieren können.</span><span class="sxs-lookup"><span data-stu-id="cfe1f-106">Note that you cannot advertise or install a 64-bit application on a 32-bit operating system.</span></span>

<span data-ttu-id="cfe1f-107">Ein Windows Installer Paket muss entweder als 32-Bit-oder als 64-Bit-Paket angegeben werden. Er kann nicht als neutral angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cfe1f-107">A Windows Installer package must be specified as either a 32-bit or a 64-bit package; it cannot be specified as neutral.</span></span> <span data-ttu-id="cfe1f-108">Auf einem Computer, der ein 64-Bit-Betriebssystem verwendet, wird der Windows Installer-Dienst in einem 64-Bit-Prozess gehostet, der sowohl 32-Bit-als auch 64-Bit-Pakete installiert.</span><span class="sxs-lookup"><span data-stu-id="cfe1f-108">On a computer using a 64-bit operating system, the Windows Installer service is hosted in a 64-bit process that installs both 32-bit and 64-bit packages.</span></span> <span data-ttu-id="cfe1f-109">Von Windows Installer werden drei Typen von Windows Installer-Paketen auf einem Computer installiert, auf dem ein 64-Bit-Betriebssystem ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="cfe1f-109">Windows Installer installs three types of Windows installer packages on a computer running a 64-bit operating system:</span></span>

-   <span data-ttu-id="cfe1f-110">32-Bit-Pakete, die nur 32-Bit-Komponenten enthalten.</span><span class="sxs-lookup"><span data-stu-id="cfe1f-110">32-bit packages that contain only 32-bit components.</span></span>
-   <span data-ttu-id="cfe1f-111">64-Bit-Pakete, die einige 32-Bit-Komponenten enthalten.</span><span class="sxs-lookup"><span data-stu-id="cfe1f-111">64-bit packages containing some 32-bit components.</span></span>
-   <span data-ttu-id="cfe1f-112">64-Bit-Pakete, die nur 64-Bit-Komponenten enthalten.</span><span class="sxs-lookup"><span data-stu-id="cfe1f-112">64-bit packages containing only 64-bit components.</span></span>

<span data-ttu-id="cfe1f-113">In den folgenden Abschnitten werden die beiden Typen von Windows Installer Paketen und die neuen Installer-Eigenschaften beschrieben, die von Windows Installer für 64-Bit-Pakete bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="cfe1f-113">The follow sections describe the two types of Windows Installer packages and the new installer properties provided by Windows Installer for 64-bit packages.</span></span>

[<span data-ttu-id="cfe1f-114">32-Bit-Windows Installer Pakete</span><span class="sxs-lookup"><span data-stu-id="cfe1f-114">32-bit Windows Installer Packages</span></span>](32-bit-windows-installer-packages.md)

[<span data-ttu-id="cfe1f-115">64-Bit-Windows Installer Pakete</span><span class="sxs-lookup"><span data-stu-id="cfe1f-115">64-bit Windows Installer Packages</span></span>](64-bit-windows-installer-packages.md)

## <a name="related-topics"></a><span data-ttu-id="cfe1f-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cfe1f-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cfe1f-117">Verwenden von 64-Bit-Windows Installer Paketen</span><span class="sxs-lookup"><span data-stu-id="cfe1f-117">Using 64-Bit Windows Installer Packages</span></span>](using-64-bit-windows-installer-packages.md)
</dt> </dl>

 

 



