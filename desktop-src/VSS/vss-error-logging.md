---
description: 'Die folgenden VSS-Fehler-und-Zustandsinformationen werden in das Anwendungs Ereignisprotokoll geschrieben:'
ms.assetid: d0b0f012-ad4f-4bd8-bb97-98f212bcbe81
title: VSS-Fehler Protokollierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9822035f36f56162fb6836bf7ad4c09cdd31b777
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129297"
---
# <a name="vss-error-logging"></a><span data-ttu-id="5c7e4-103">VSS-Fehler Protokollierung</span><span class="sxs-lookup"><span data-stu-id="5c7e4-103">VSS Error Logging</span></span>

<span data-ttu-id="5c7e4-104">Die folgenden VSS-Fehler-und-Zustandsinformationen werden in das Anwendungs Ereignisprotokoll geschrieben:</span><span class="sxs-lookup"><span data-stu-id="5c7e4-104">The following VSS error and state information is written to the Application Event Log:</span></span>

-   <span data-ttu-id="5c7e4-105">Requestfehler, die mithilfe der [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Schnittstelle erzeugt wurden</span><span class="sxs-lookup"><span data-stu-id="5c7e4-105">Requester errors produced using the [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) interface</span></span>
-   <span data-ttu-id="5c7e4-106">Writer-Fehler, die in mithilfe der [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) -Klasse erzeugt werden</span><span class="sxs-lookup"><span data-stu-id="5c7e4-106">Writer errors produced in using the [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) class, including overriding methods</span></span>
-   <span data-ttu-id="5c7e4-107">Vom Standardanbieter generierte Fehler</span><span class="sxs-lookup"><span data-stu-id="5c7e4-107">Default-provider-generated errors</span></span>
-   <span data-ttu-id="5c7e4-108">VSS-Dienst Fehler, die beim koordinieren der Anbieter-, Writer-und requestaktivität generiert wurden (z. b. die Generierung von Ereignissen)</span><span class="sxs-lookup"><span data-stu-id="5c7e4-108">VSS service errors generated in coordinating provider, writer, and requester activity (such as the generation of events)</span></span>

<span data-ttu-id="5c7e4-109">Diese Fehler können eine Reihe von Gründen haben, einschließlich eines Programmierfehlers in Code von Drittanbietern oder von VSS-bezogenen Konfigurationsfehlern.</span><span class="sxs-lookup"><span data-stu-id="5c7e4-109">These errors might have a number of causes, including a programming error in third-party code or VSS-related configuration errors.</span></span>

<span data-ttu-id="5c7e4-110">VSS-Treiber und Implementierungs Funktionen auf niedrigerer Ebene schreiben Fehler in das System Protokoll.</span><span class="sxs-lookup"><span data-stu-id="5c7e4-110">VSS drivers and lower-level implementation functionality write errors to the System Log.</span></span> <span data-ttu-id="5c7e4-111">Drittanbieter Software (requster, Anbieter, Writer) kann das Anwendungsprotokoll, das System Protokoll oder beides auswählen, um Fehlerprotokoll Einträge zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="5c7e4-111">Third-party software (requester, provider, writer) can choose the Application Log, the System Log, or both, to write error log entries.</span></span>

<span data-ttu-id="5c7e4-112">Es wird empfohlen, dass Anwendungen auf hoher Ebene (z. b. Code im Benutzermodus) das Anwendungsprotokoll verwenden.</span><span class="sxs-lookup"><span data-stu-id="5c7e4-112">It is recommended that high-level applications (such as user-mode code) use the Application Log.</span></span> <span data-ttu-id="5c7e4-113">Anwendungen auf niedrigerer Ebene, z. b. Hardwareschnittstellen und Treiber, sollten das System Protokoll verwenden.</span><span class="sxs-lookup"><span data-stu-id="5c7e4-113">Lower-level applications, such as hardware interfaces and drivers, should use the System Log.</span></span>

 

 



