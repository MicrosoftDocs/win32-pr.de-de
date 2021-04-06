---
title: Zuordnen von WinSNMP-Speicher Objekten
description: Deskriptoren, Ressourcen Handles und Zeichen folgen im C-Stil sind die drei Typen von Speicher Objekten in der WinSNMP-Programmierumgebung.
ms.assetid: 7f51f02b-7c9f-4aa0-b0cf-83551a312e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d70ed4d9d52452b5067a6d1e51392b84f95ccce8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036288"
---
# <a name="allocating-winsnmp-memory-objects"></a><span data-ttu-id="8ff17-103">Zuordnen von WinSNMP-Speicher Objekten</span><span class="sxs-lookup"><span data-stu-id="8ff17-103">Allocating WinSNMP Memory Objects</span></span>

<span data-ttu-id="8ff17-104">Deskriptoren, Ressourcen Handles und Zeichen folgen im C-Stil sind die drei Typen von Speicher Objekten in der WinSNMP-Programmierumgebung.</span><span class="sxs-lookup"><span data-stu-id="8ff17-104">Descriptors, resource handles and C-style strings are the three types of memory objects in the WinSNMP programming environment.</span></span>

<span data-ttu-id="8ff17-105">Der Objekttyp bestimmt, ob die Microsoft WinSNMP-Implementierung oder die WinSNMP-Anwendung den Speicher für das-Objekt zuordnet und zuordnet.</span><span class="sxs-lookup"><span data-stu-id="8ff17-105">The type of object determines whether the Microsoft WinSNMP implementation or the WinSNMP application allocates and deallocates the memory for the object.</span></span> <span data-ttu-id="8ff17-106">Dadurch wird die unnötige Zuordnung von temporären Pufferspeicher und unnötigem Kopieren von Puffern reduziert.</span><span class="sxs-lookup"><span data-stu-id="8ff17-106">This reduces unnecessary allocation of temporary buffer space and unnecessary copying of buffers.</span></span>

<span data-ttu-id="8ff17-107">In der folgenden Tabelle werden die Zuordnung und Freigabe von Ressourcen für WinSNMP-Speicher Objekte zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="8ff17-107">The following table summarizes the allocation and deallocation of resources for WinSNMP memory objects.</span></span>



| <span data-ttu-id="8ff17-108">Objekttyp</span><span class="sxs-lookup"><span data-stu-id="8ff17-108">Object type</span></span>                                                                   | <span data-ttu-id="8ff17-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ff17-109">Description</span></span>                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ff17-110">[**smioid**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) -oder [**smioctets**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) -Deskriptor</span><span class="sxs-lookup"><span data-stu-id="8ff17-110">[**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) or [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) descriptor</span></span> | <span data-ttu-id="8ff17-111">Wenn die WinSNMP-Anwendung den Arbeitsspeicher zuordnet, muss Sie den Speicher mit einem aufzurufenden Befehl für eine entsprechende Funktion nicht mehr zuordnen.</span><span class="sxs-lookup"><span data-stu-id="8ff17-111">If the WinSNMP application allocates the memory, it must deallocate the memory with a call to an appropriate function.</span></span> <span data-ttu-id="8ff17-112">Wenn die-Implementierung den Arbeitsspeicher zuordnet, muss die Anwendung die [**snmpfredescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) -Funktion aufzurufen, um den Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="8ff17-112">If the implementation allocates the memory, the application must call the [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) function to deallocate the memory.</span></span> |
| <span data-ttu-id="8ff17-113">[**smivalue**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) -Struktur</span><span class="sxs-lookup"><span data-stu-id="8ff17-113">[**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) structure</span></span>                                    | <span data-ttu-id="8ff17-114">Wenn der **Wertmember** ein [**smioid**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) -oder [**smioctets**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) -Deskriptor ist, muss die Anwendung wie oben beschrieben für Deskriptoren fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="8ff17-114">If the **value** member is an [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) or an [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) descriptor, the application must proceed as indicated above for descriptors.</span></span>                                                                                                     |
| <span data-ttu-id="8ff17-115">Ressourcen handle</span><span class="sxs-lookup"><span data-stu-id="8ff17-115">Resource handle</span></span>                                                               | <span data-ttu-id="8ff17-116">Die-Implementierung ordnet den Speicher zu, verwaltet ihn und gibt ihn frei.</span><span class="sxs-lookup"><span data-stu-id="8ff17-116">The implementation allocates, manages, and frees the memory.</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="8ff17-117">Zeichenfolge im C-Stil</span><span class="sxs-lookup"><span data-stu-id="8ff17-117">C-style string</span></span>                                                                | <span data-ttu-id="8ff17-118">Die Anwendung WinSNMP muss den zugewiesenen Speicher verwalten und freigeben.</span><span class="sxs-lookup"><span data-stu-id="8ff17-118">The WinSNMP application must manage and free the memory it allocates.</span></span>                                                                                                                                                                                                                |



 

<span data-ttu-id="8ff17-119">Weitere Informationen finden Sie unter [Freigeben von WinSNMP-Deskriptoren](freeing-winsnmp-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="8ff17-119">For more information, see [Freeing WinSNMP Descriptors](freeing-winsnmp-descriptors.md).</span></span>

 

 




