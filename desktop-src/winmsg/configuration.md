---
description: In diesem Referenzabschnitt wird die Konfiguration für Windows und Meldungen beschrieben. Erfahren Sie mehr über Anzeigeelemente und Systemmetriken.
ms.assetid: aba21473-07cc-4de9-a310-ad9b43c133eb
title: Konfiguration (Windows und Meldungen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa516e87aa7d338d4e2fd46a160fcbd6dadb305
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406343"
---
# <a name="configuration-windows-and-messages"></a><span data-ttu-id="15744-104">Konfiguration (Windows und Meldungen)</span><span class="sxs-lookup"><span data-stu-id="15744-104">Configuration (Windows and Messages)</span></span>

<span data-ttu-id="15744-105">*Anzeigeelemente* sind die Teile eines Fensters und die Anzeige, die auf dem Systemanzeigebildschirm angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="15744-105">*Display elements* are the parts of a window and the display that appear on the system display screen.</span></span> <span data-ttu-id="15744-106">*Systemmetriken* sind die Dimensionen verschiedener Anzeigeelemente.</span><span class="sxs-lookup"><span data-stu-id="15744-106">*System metrics* are the dimensions of various display elements.</span></span> <span data-ttu-id="15744-107">Typische Systemmetriken sind die Fensterrahmenbreite, die Symbolhöhe usw.</span><span class="sxs-lookup"><span data-stu-id="15744-107">Typical system metrics include the window border width, icon height, and so on.</span></span> <span data-ttu-id="15744-108">Systemmetriken beschreiben auch andere Aspekte des Systems, z. B. ob eine Maus installiert ist, Doppel-Byte-Zeichen unterstützt werden oder eine Debugversion des Betriebssystems installiert ist.</span><span class="sxs-lookup"><span data-stu-id="15744-108">System metrics also describe other aspects of the system, such as whether a mouse is installed, double-byte characters are supported, or a debugging version of the operating system is installed.</span></span> <span data-ttu-id="15744-109">Die [**GetSystemMetrics-Funktion**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) ruft die angegebene Systemmetrik ab.</span><span class="sxs-lookup"><span data-stu-id="15744-109">The [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function retrieves the specified system metric.</span></span>

<span data-ttu-id="15744-110">Anwendungen können auch die Farbe von Fensterelementen wie Menüs, Scrollleisten und Schaltflächen abrufen und festlegen, indem sie die Funktionen [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) bzw. [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) verwenden.</span><span class="sxs-lookup"><span data-stu-id="15744-110">Applications can also retrieve and set the color of window elements such as menus, scroll bars, and buttons by using the [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) and [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) functions, respectively.</span></span>

<span data-ttu-id="15744-111">Die [**SystemParametersInfo-Funktion**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) ruft verschiedene Systemattribute ab oder legt diese fest, z. B. Doppelklickzeit, Time-Out für Bildschirmschoner, Fensterrahmenbreite und Desktopmuster.</span><span class="sxs-lookup"><span data-stu-id="15744-111">The [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function retrieves or sets various system attributes, such as double-click time, screen saver time-out, window border width, and desktop pattern.</span></span> <span data-ttu-id="15744-112">Wenn eine Anwendung **SystemParametersInfo** verwendet, um einen Parameter festzulegen, erfolgt die Änderung sofort.</span><span class="sxs-lookup"><span data-stu-id="15744-112">When an application uses **SystemParametersInfo** to set a parameter, the change takes place immediately.</span></span> <span data-ttu-id="15744-113">Mit dieser Funktion können Anwendungen auch das Benutzerprofil aktualisieren, sodass Änderungen am System beibehalten werden, wenn das System neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="15744-113">This function also enables applications to update the user profile, so changes to the system will be preserved when the system is restarted.</span></span>

 

 
