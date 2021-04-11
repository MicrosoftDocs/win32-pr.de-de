---
description: Konfiguration
ms.assetid: aba21473-07cc-4de9-a310-ad9b43c133eb
title: Konfiguration (Windows und Meldungen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bac66d2ba25e81582734eb13148d2651b276ea01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217822"
---
# <a name="configuration-windows-and-messages"></a><span data-ttu-id="1e857-103">Konfiguration (Windows und Meldungen)</span><span class="sxs-lookup"><span data-stu-id="1e857-103">Configuration (Windows and Messages)</span></span>

<span data-ttu-id="1e857-104">*Anzeigeelemente* sind die Teile eines Fensters und die Anzeige, die auf dem Bildschirm System Anzeige angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1e857-104">*Display elements* are the parts of a window and the display that appear on the system display screen.</span></span> <span data-ttu-id="1e857-105">*Systemmetriken* sind die Dimensionen verschiedener Anzeigeelemente.</span><span class="sxs-lookup"><span data-stu-id="1e857-105">*System metrics* are the dimensions of various display elements.</span></span> <span data-ttu-id="1e857-106">Typische Systemmetriken umfassen die Fensterrahmen Breite, die Symbol Höhe usw.</span><span class="sxs-lookup"><span data-stu-id="1e857-106">Typical system metrics include the window border width, icon height, and so on.</span></span> <span data-ttu-id="1e857-107">Systemmetriken beschreiben auch andere Aspekte des Systems, z. b. ob eine Maus installiert ist, Doppelbyte Zeichen unterstützt werden oder eine Debugversion des Betriebssystems installiert ist.</span><span class="sxs-lookup"><span data-stu-id="1e857-107">System metrics also describe other aspects of the system, such as whether a mouse is installed, double-byte characters are supported, or a debugging version of the operating system is installed.</span></span> <span data-ttu-id="1e857-108">Die [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) -Funktion Ruft die angegebene Systemmetrik ab.</span><span class="sxs-lookup"><span data-stu-id="1e857-108">The [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function retrieves the specified system metric.</span></span>

<span data-ttu-id="1e857-109">Anwendungen können auch die Farbe von Fensterelementen, z. b. Menüs, Bild Lauf leisten und Schaltflächen, mithilfe der Funktionen " [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) " und " [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) " abrufen und festlegen.</span><span class="sxs-lookup"><span data-stu-id="1e857-109">Applications can also retrieve and set the color of window elements such as menus, scroll bars, and buttons by using the [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) and [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) functions, respectively.</span></span>

<span data-ttu-id="1e857-110">Die [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) -Funktion Ruft verschiedene Systemattribute ab oder legt Sie fest, z. b. Doppelklick Zeit, Bildschirmschoner-Timeout, Fensterrahmen Breite und Desktop Muster.</span><span class="sxs-lookup"><span data-stu-id="1e857-110">The [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function retrieves or sets various system attributes, such as double-click time, screen saver time-out, window border width, and desktop pattern.</span></span> <span data-ttu-id="1e857-111">Wenn eine Anwendung **SystemParametersInfo** verwendet, um einen Parameter festzulegen, erfolgt die Änderung sofort.</span><span class="sxs-lookup"><span data-stu-id="1e857-111">When an application uses **SystemParametersInfo** to set a parameter, the change takes place immediately.</span></span> <span data-ttu-id="1e857-112">Diese Funktion ermöglicht es Anwendungen auch, das Benutzerprofil zu aktualisieren, sodass Änderungen am System beim Neustart des Systems beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="1e857-112">This function also enables applications to update the user profile, so changes to the system will be preserved when the system is restarted.</span></span>

 

 
