---
title: Verbunddateien
description: Obwohl Sie eigene strukturierte Speicher Objekte und Schnittstellen implementieren können, stellt com eine Standard Implementierung namens Verbund Dateien bereit.
ms.assetid: 23b425e6-dfe5-403b-8f43-de6843a03dcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62be79f09afd23e53a569b76ad3e0af46cae2f9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206374"
---
# <a name="compound-files"></a><span data-ttu-id="761f3-103">Verbunddateien</span><span class="sxs-lookup"><span data-stu-id="761f3-103">Compound Files</span></span>

<span data-ttu-id="761f3-104">Obwohl Sie eigene strukturierte Speicher Objekte und Schnittstellen implementieren können, stellt com eine Standard Implementierung namens Verbund Dateien bereit.</span><span class="sxs-lookup"><span data-stu-id="761f3-104">Although you can implement your own structured storage objects and interfaces, COM provides a standard implementation called Compound Files.</span></span> <span data-ttu-id="761f3-105">Durch die Verwendung von Verbund Dateien können Sie Ihre eigene Implementierung von strukturiertem Speicher codieren und einige zusätzliche Vorteile nutzen, die von der Einhaltung eines definierten Standards abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="761f3-105">Using Compound Files saves you the work of coding your own implementation of structured storage and confers several additional benefits derived from adhering to a defined standard.</span></span> <span data-ttu-id="761f3-106">Dazu gehören folgende Vorteile:</span><span class="sxs-lookup"><span data-stu-id="761f3-106">These benefits include the following:</span></span>

-   <span data-ttu-id="761f3-107">**Dateisystem-und Plattformunabhängigkeit**.</span><span class="sxs-lookup"><span data-stu-id="761f3-107">**File-system and platform independence**.</span></span> <span data-ttu-id="761f3-108">Da die Implementierung der Verbund Dateien von com auf vorhandenen Flatfile-Systemen ausgeführt wird, können Verbund Dateien, die im FAT-Dateisystem, im NTFS-Dateisystem oder im Macintosh-Dateisystem gespeichert sind, von Anwendungen geöffnet werden, die eines der anderen Dateisysteme verwenden.</span><span class="sxs-lookup"><span data-stu-id="761f3-108">Because COM's Compound Files implementation runs on top of existing flat-file systems, compound files stored in the FAT file system, NTFS file system, or Macintosh file systems can be opened by applications using any one of the other file systems.</span></span>
-   <span data-ttu-id="761f3-109">Durch **suchbar**.</span><span class="sxs-lookup"><span data-stu-id="761f3-109">**Searchable**.</span></span> <span data-ttu-id="761f3-110">Da die separaten Objekte in einer Verbund Datei in einem Standardformat gespeichert werden und über Standard-COM-Schnittstellen und APIs auf Sie zugegriffen werden kann, können alle Browser Dienstprogrammen, die diese Schnittstellen und APIs verwenden, die Objekte in der Datei auflisten, auch wenn die Daten in einem bestimmten Objekt ein proprietäres Format aufweisen können.</span><span class="sxs-lookup"><span data-stu-id="761f3-110">Because the separate objects in a compound file are saved in a standard format and can be accessed using standard COM interfaces and APIs, any browser utility using these interfaces and APIs can list the objects in the file, even though data within a given object may be in a proprietary format.</span></span>
-   <span data-ttu-id="761f3-111">**Zugriff auf bestimmte interne Daten**.</span><span class="sxs-lookup"><span data-stu-id="761f3-111">**Access to certain internal data**.</span></span> <span data-ttu-id="761f3-112">Da die Implementierung von Verbund Dateien Standardmethoden zum Schreiben bestimmter Datentypen bietet – zusammenfassende Informationen, z. –. Anwendungen können diese Daten mithilfe von COM-Schnittstellen und APIs lesen.</span><span class="sxs-lookup"><span data-stu-id="761f3-112">Because the Compound Files implementation provides standard ways of writing certain types of data—summary information, for example—applications can read this data using COM interfaces and APIs.</span></span>

 

 




