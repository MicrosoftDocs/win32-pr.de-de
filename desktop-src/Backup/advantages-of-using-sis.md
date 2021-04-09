---
title: Vorteile der Verwendung von SIS
description: 'Die Verwendung von SIS und der SIS-Sicherungs Architektur bietet folgende Vorteile:'
ms.assetid: c72a14a1-92ae-4875-ae73-e277ed2b0c0d
keywords:
- SIS-Sicherung (Single Instance Store), Vorteile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcd1856ce54e817c25830f15f133c7d76c6a80fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036417"
---
# <a name="advantages-of-using-sis"></a><span data-ttu-id="b4ce6-104">Vorteile der Verwendung von SIS</span><span class="sxs-lookup"><span data-stu-id="b4ce6-104">Advantages of Using SIS</span></span>

<span data-ttu-id="b4ce6-105">Die Verwendung von SIS und der SIS-Sicherungs Architektur bietet folgende Vorteile:</span><span class="sxs-lookup"><span data-stu-id="b4ce6-105">The advantages of using SIS and the SIS backup architecture are the following:</span></span>

-   <span data-ttu-id="b4ce6-106">Die Verbindungen zwischen den SIS-Links und den Unterstützungs Dateien werden automatisch von der SIS-Architektur verwaltet, wenn die Sicherungs Anwendungen die SIS Backup-API-Funktionen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="b4ce6-106">The connections between the SIS links and the backing files are automatically maintained by the SIS architecture as your backup applications call the SIS backup API functions.</span></span>
-   <span data-ttu-id="b4ce6-107">Der Inhalt der SIS-Analyse Punkte ist für Ihre Sicherungs-und Wiederherstellungs Anwendungen nicht transparent. Dadurch wird sichergestellt, dass Upgrades auf die SIS-internale keine Änderungen an der SIS-API oder Ihren Sicherungs-und Wiederherstellungs Anwendungen erfordern, die SIS-API-Funktionen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="b4ce6-107">The contents of the SIS reparse points are opaque to your backup and restore applications, ensuring that upgrades to the SIS internals will not require a change in the SIS API or your backup and restore applications that call SIS API functions.</span></span> <span data-ttu-id="b4ce6-108">Sie müssen Ihre Anwendung nur mit einer neuen Version der SIS-dll mit dem Namen Sisbkup.dll neu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="b4ce6-108">You need only recompile your application with a new version of the SIS DLL, named Sisbkup.dll.</span></span>
-   <span data-ttu-id="b4ce6-109">Da SIS als Dateisystem-Filtertreiber implementiert ist, werden die Verbindungen zwischen den SIS-Links und den Unterstützungs Dateien permanent nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="b4ce6-109">Because SIS is implemented as a file system filter driver, it constantly tracks the connections between the SIS links and the backing files.</span></span> <span data-ttu-id="b4ce6-110">Wenn die Dateien gesichert und wieder hergestellt werden, stellt die SIS-Sicherung sicher, dass nur eine Instanz der Sicherungsdatei gesichert und wieder hergestellt wird, unabhängig von der Anzahl von SIS-Links, die darauf zeigen.</span><span class="sxs-lookup"><span data-stu-id="b4ce6-110">When the files are backed up and restored, SIS backup ensures that only one instance of the backing file will be backed up and restored, regardless of the number of SIS links that point to it.</span></span>

 

 




