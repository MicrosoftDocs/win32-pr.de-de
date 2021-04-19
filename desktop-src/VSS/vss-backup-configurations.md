---
description: Es gibt eine Reihe von konventionell unterstützten Sicherungs Typen&\# 8212; inkrementell, differenziell und vollständig&\# 8212;, die VSS kennt, sowie eine für VSS besondere Sicherungs Konfiguration.
ms.assetid: eddf29bc-221b-4b10-9842-a893b62fa846
title: VSS-Sicherungs Konfigurationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4e4c4f383a208781722053b47ba9ae5bcbf1db7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346948"
---
# <a name="vss-backup-configurations"></a><span data-ttu-id="fed11-103">VSS-Sicherungs Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="fed11-103">VSS Backup Configurations</span></span>

<span data-ttu-id="fed11-104">Es gibt eine Reihe von konventionell unterstützten Sicherungs Typen – inkrementell, differenziell und voll –, die VSS kennt, sowie eine für VSS besondere Sicherungs Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="fed11-104">There are a number of conventionally supported backup types—incremental, differential, and full—that VSS is aware of, as well as a backup configuration peculiar to VSS.</span></span>

<span data-ttu-id="fed11-105">Beim Definieren einer Sicherungs Konfiguration geben eine Anforderer und die Writer auf einem System an, wie Daten auf ein Speichergerät geschrieben werden, wie der schattenkopiemechanismus bereitgestellt wird und welche Informationen gespeichert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="fed11-105">In defining a backup configuration, a requester and the writers on a system indicate how data will be written to a storage device, how the shadow copy mechanism will be deployed, and what information needs to be saved.</span></span> <span data-ttu-id="fed11-106">Die Interaktion zwischen Writern und Anforderern wird durch den Sicherungstyp bestimmt, der von einem Anforderer durchgeführt werden soll, und die Arten (oder Schemas), die jeder Writer unterstützen kann:</span><span class="sxs-lookup"><span data-stu-id="fed11-106">Interaction between writers and requesters is determined by the type of backup a requester wants to perform and the kinds (or schemas) that each writer can support:</span></span>

-   [<span data-ttu-id="fed11-107">VSS-Sicherungs Status</span><span class="sxs-lookup"><span data-stu-id="fed11-107">VSS Backup State</span></span>](vss-backup-state.md)
-   [<span data-ttu-id="fed11-108">Unterstützung für Writer-Sicherungs Schema</span><span class="sxs-lookup"><span data-stu-id="fed11-108">Writer Backup Schema Support</span></span>](writer-backup-schema-support.md)
-   [<span data-ttu-id="fed11-109">Schema Unterstützung auf Dateiebene</span><span class="sxs-lookup"><span data-stu-id="fed11-109">File Level Schema Support</span></span>](file-level-schema-support.md)

 

 



