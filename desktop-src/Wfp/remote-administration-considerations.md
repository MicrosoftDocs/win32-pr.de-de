---
description: Es gibt einige Überlegungen, die für Remote verwaltete Systeme eindeutig sind.
ms.assetid: bfdf121e-9b4e-4323-82ec-9bd32531caad
title: Überlegungen zur WFP-Remote Verwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57bb40776f6b727abb49d7e0685bb12b087ed2bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366085"
---
# <a name="wfp-remote-administration-considerations"></a><span data-ttu-id="aa82e-103">Überlegungen zur WFP-Remote Verwaltung</span><span class="sxs-lookup"><span data-stu-id="aa82e-103">WFP Remote Administration Considerations</span></span>

<span data-ttu-id="aa82e-104">Es gibt einige Überlegungen, die für Remote verwaltete Systeme eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="aa82e-104">There are some considerations that are unique to remotely administered systems.</span></span> <span data-ttu-id="aa82e-105">Zuerst werden bei der Remote Bereitstellung der Software Installation (mit SMS oder MSI) WFP-Fehler Dialogfelder auf dem Bildschirm eines lokal angemeldeten Administrators (sofern vorhanden) und nicht des Installations Diensts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aa82e-105">First, when software installation is remotely deployed (using SMS or MSI), WFP error dialog boxes are displayed on the screen of a locally logged on administrator (if present), not to the installation service.</span></span> <span data-ttu-id="aa82e-106">Zweitens: Wenn ein Administrator sich Remote bei einem Terminal Server anmeldet und eine Anwendung installiert, die Geschützte Systemdateien ersetzt, werden die WFP-Fehler Dialogfelder nur in der Hauptkonsole angezeigt, nicht im Remote Fenster des Administrators.</span><span class="sxs-lookup"><span data-stu-id="aa82e-106">Second, if an administrator logs into a terminal server remotely and installs an application that replaces protected system files, the WFP error dialog boxes are displayed only in the main console, not the administrator's remote window.</span></span>

<span data-ttu-id="aa82e-107">Aus diesen Gründen unterdrückt WFP die Fehler Dialogfelder, bis sich ein Administrator lokal anmeldet.</span><span class="sxs-lookup"><span data-stu-id="aa82e-107">For these reasons, WFP suppresses its error dialog boxes until an administrator logs on locally.</span></span> <span data-ttu-id="aa82e-108">Remote Administratoren können Datei Ersetzungs Fehler im System Ereignisprotokoll finden.</span><span class="sxs-lookup"><span data-stu-id="aa82e-108">Remote administrators can find file replacement errors in the system event log.</span></span>

<span data-ttu-id="aa82e-109">**Windows Vista und Windows Server 2008:** Die WFP-Remote Verwaltung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="aa82e-109">**Windows Vista and Windows Server 2008:** WFP remote administration is not supported.</span></span>

 

 



