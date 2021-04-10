---
title: Cleanup des virtuellen Verzeichnisses
description: Bits erweitert virtuelle IIS-Verzeichnisse für die Unterstützung von Uploads.
ms.assetid: 8214904e-8a95-4c4b-a1c5-91e84031587f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83fb689bb3c797a311ec7c2ef8134eb51ffd6f1a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948909"
---
# <a name="virtual-directory-cleanup"></a><span data-ttu-id="52594-103">Cleanup des virtuellen Verzeichnisses</span><span class="sxs-lookup"><span data-stu-id="52594-103">Virtual Directory Cleanup</span></span>

<span data-ttu-id="52594-104">Bits erweitert virtuelle IIS-Verzeichnisse für die Unterstützung von Uploads.</span><span class="sxs-lookup"><span data-stu-id="52594-104">BITS extends IIS virtual directories to support uploads.</span></span> <span data-ttu-id="52594-105">Jedes virtuelle Verzeichnis verfügt über eine Sitzungs Timeout-Eigenschaft (die IIS-Eigenschaft " [bitssessiontimeout](bits-iis-extension-properties.md) Metabase"), die den Zeitraum angibt, in dem der BITS-Client beim Hochladen der Datei Fortschritte ausführen muss.</span><span class="sxs-lookup"><span data-stu-id="52594-105">Each virtual directory has a session time-out property (the IIS [BITSSessionTimeout](bits-iis-extension-properties.md) metabase property) that specifies the period of time in which the BITS client must make progress in uploading the file.</span></span> <span data-ttu-id="52594-106">Wenn während dieses Zeitraums kein Fortschritt erfolgt (der Zeitgeber wird zurückgesetzt, wenn der Fortschritt erfolgt), schließt Bits die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="52594-106">If no progress is made during that period (the timer is reset when progress is made), BITS closes the session.</span></span> <span data-ttu-id="52594-107">Der standardmäßige Sitzungs Timeout beträgt 14 Tage.</span><span class="sxs-lookup"><span data-stu-id="52594-107">The default session time-out is 14 days.</span></span>

<span data-ttu-id="52594-108">Mit Bits wird der [Taskplaner](/windows/desktop/TaskSchd/task-scheduler-start-page) für jedes virtuelle Verzeichnis, das Sie erstellen und aktivieren, ein Arbeits Element hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="52594-108">BITS adds a work item to the [Task Scheduler](/windows/desktop/TaskSchd/task-scheduler-start-page) for each virtual directory you create and enable.</span></span> <span data-ttu-id="52594-109">Mit dem Arbeits Element werden Ressourcen gelöscht, die den geschlossenen Sitzungen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="52594-109">The work item deletes resources associated with the closed sessions.</span></span> <span data-ttu-id="52594-110">Standardmäßig erfolgt die Bereinigung alle 12 Stunden.</span><span class="sxs-lookup"><span data-stu-id="52594-110">By default, the cleanup occurs every 12 hours.</span></span> <span data-ttu-id="52594-111">Wenn zwei virtuelle Verzeichnisse auf dasselbe physische Verzeichnis verweisen, löscht der Bereinigungs Prozess, der von einem der Verzeichnisse initiiert wurde, die Ressourcen, die allen geschlossenen Sitzungen im physischen Verzeichnis zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="52594-111">If two virtual directories point to the same physical directory, the cleanup process initiated by one of the directories deletes the resources associated with all closed sessions in the physical directory.</span></span>

<span data-ttu-id="52594-112">Verwenden Sie die Registerkarte Bits-Erweiterung oder die [Taskplaner](/windows/desktop/TaskSchd/task-scheduler-start-page) Schnittstellen, um den Bereinigungs Zeitplan entsprechend Ihrer Anwendung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="52594-112">Use the BITS Extension tab or the [Task Scheduler](/windows/desktop/TaskSchd/task-scheduler-start-page) interfaces to change the cleanup schedule as appropriate for your application.</span></span> <span data-ttu-id="52594-113">Sie können auch die [**ibitsextensionsetup:: getcleanuptask**](/windows/desktop/api/Bitscfg/nf-bitscfg-ibitsextensionsetup-getcleanuptask) -Methode aufrufen, um einen Schnittstellen Zeiger auf den Cleanuptask abzurufen, der dem virtuellen Verzeichnis zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="52594-113">You can also call the [**IBITSExtensionSetup::GetCleanupTask**](/windows/desktop/api/Bitscfg/nf-bitscfg-ibitsextensionsetup-getcleanuptask) method to retrieve an interface pointer to the cleanup task associated with the virtual directory.</span></span>

> [!Note]  
> <span data-ttu-id="52594-114">Wenn die Taskplaner nach dem Aktivieren des virtuellen Verzeichnisses deaktiviert ist, funktioniert der Cleanupprozess des virtuellen Verzeichnisses nicht.</span><span class="sxs-lookup"><span data-stu-id="52594-114">If the Task Scheduler is disabled after the virtual directory is enabled, the virtual directory cleanup process will not work.</span></span>

 

 

 