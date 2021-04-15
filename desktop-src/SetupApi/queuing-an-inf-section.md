---
description: Neben Datei Vorgängen in der Warteschlange können Sie auch alle Dateien in die Warteschlange stellen, die in einem INF-Abschnitt aufgeführt sind.
ms.assetid: 456e1a19-7e9b-40c8-9295-42bb8f740f58
title: Warteschlangen für einen INF-Abschnitt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5566931131885cf6f300b5a6386639bbd564e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529777"
---
# <a name="queuing-an-inf-section"></a><span data-ttu-id="37b89-103">Warteschlangen für einen INF-Abschnitt</span><span class="sxs-lookup"><span data-stu-id="37b89-103">Queuing an INF Section</span></span>

<span data-ttu-id="37b89-104">Neben Datei Vorgängen in der Warteschlange können Sie auch alle Dateien in die Warteschlange stellen, die in einem INF-Abschnitt aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="37b89-104">In addition to queuing file operations individually, you can also queue all the files listed in an INF section.</span></span>

<span data-ttu-id="37b89-105">Sie können alle Dateien, die im Abschnitt **Kopieren von Dateien** einer INF-Datei aufgelistet sind, durch Aufrufen von [**setupqueuecopysection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona)in die Warteschlange stellen.</span><span class="sxs-lookup"><span data-stu-id="37b89-105">You can queue all the files listed in a **Copy Files** section of an INF file by calling [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona).</span></span> <span data-ttu-id="37b89-106">Damit diese Funktion erfolgreich ist, muss der Abschnitt zum **Kopieren von Dateien** das richtige Format aufweisen, und die INF-Datei oder eine der angefügten Dateien muss die Abschnitte **SourceDisksFiles** und **SourceDisksNames** enthalten.</span><span class="sxs-lookup"><span data-stu-id="37b89-106">For this function to be successful, the **Copy Files** section must be in the proper format and the INF file, or one of its appended files, must contain the **SourceDisksFiles** and **SourceDisksNames** sections.</span></span>

<span data-ttu-id="37b89-107">Wenn Sie alle im Abschnitt **Löschen von Dateien** einer INF-Datei angegebenen Dateien löschen möchten, können Sie [**setupqueuedeletesection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)auch aufrufen.</span><span class="sxs-lookup"><span data-stu-id="37b89-107">Similarly, if you want to delete all the files specified in a **Delete Files** section of an INF file, you can call [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona).</span></span> <span data-ttu-id="37b89-108">Wenn Sie alle Dateien im Abschnitt **Umbenennen von Dateien** einer INF-Datei umbenennen möchten, verwenden Sie [**setupqueuerenamesection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona).</span><span class="sxs-lookup"><span data-stu-id="37b89-108">To rename all the files in a **Rename Files** section of an INF file use [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona).</span></span>

 

 



