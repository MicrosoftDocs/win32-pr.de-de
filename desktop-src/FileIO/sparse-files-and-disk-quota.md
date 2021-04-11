---
description: Eine sparsedatei wirkt sich auf Benutzerkontingente durch die nominale Größe der Datei und nicht die tatsächlich zugeordnete Menge an Speicherplatz aus.
ms.assetid: 7dbe1133-f5cb-4925-9448-5d40f1c553ff
title: Sparsesdateien und Datenträger Kontingente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 326780e2b2c5119256272c0d297613d2c32e6e6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129757"
---
# <a name="sparse-files-and-disk-quotas"></a><span data-ttu-id="8e194-103">Sparsesdateien und Datenträger Kontingente</span><span class="sxs-lookup"><span data-stu-id="8e194-103">Sparse Files and Disk Quotas</span></span>

<span data-ttu-id="8e194-104">Eine sparsedatei wirkt sich auf Benutzerkontingente durch die nominale Größe der Datei und nicht die tatsächlich zugeordnete Menge an Speicherplatz aus.</span><span class="sxs-lookup"><span data-stu-id="8e194-104">A sparse file affects user quotas by the nominal size of the file, not the actual allocated amount of disk space.</span></span> <span data-ttu-id="8e194-105">Das heißt, dass das Erstellen einer 50-MB-Datei mit allen 0 Bytes 50 MB dieses Benutzer Kontingents beansprucht.</span><span class="sxs-lookup"><span data-stu-id="8e194-105">That is, creating a 50-MB file with all zero bytes consumes 50 MB of that user's quota.</span></span> <span data-ttu-id="8e194-106">Dies bedeutet, dass der Benutzer beim Schreiben von Daten in die sparsedatei keine Gedanken mehr über die Überschreitung seines festen Kontingent Limits machen muss, da ihm bereits der Platz in Rechnung gestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="8e194-106">This means that as the user writes data to the sparse file, he need not worry about exceeding his hard quota limit, because he has already been charged for the space.</span></span> <span data-ttu-id="8e194-107">System Administratoren sollten nicht die Größe einer kleinen sparsedatei zählen, die kleiner ist.</span><span class="sxs-lookup"><span data-stu-id="8e194-107">System administrators should not count on the size of a sparse file remaining small.</span></span> <span data-ttu-id="8e194-108">Daher sollten Sie nicht Ihren Benutzern feste Kontingent Limits gewähren, die den verfügbaren physischen Speicherplatz überschreiten, trotz der Verwendung von Dateien mit geringer Dichte.</span><span class="sxs-lookup"><span data-stu-id="8e194-108">Therefore they should not grant their users hard quota limits that exceed the physical space available, despite the use of sparse files.</span></span>

 

 



