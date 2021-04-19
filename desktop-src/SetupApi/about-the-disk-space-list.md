---
description: Mithilfe der Speicherplatz Liste können Sie den Speicherplatz berechnen, der zum Abschluss der Installations Vorgänge erforderlich ist.
ms.assetid: 6514cbdd-2f23-4ab8-9e34-86d3837503dc
title: Informationen zur Disk-Space Liste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b092d73c00f426fe5c0ab298e4b6a53c19131c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348375"
---
# <a name="about-the-disk-space-list"></a><span data-ttu-id="85c09-103">Informationen zur Disk-Space Liste</span><span class="sxs-lookup"><span data-stu-id="85c09-103">About the Disk-Space List</span></span>

<span data-ttu-id="85c09-104">Mithilfe der Speicherplatz Liste können Sie den Speicherplatz berechnen, der zum Abschluss der Installations Vorgänge erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="85c09-104">The disk-space list enables you to calculate the disk space required to complete the installation operations.</span></span> <span data-ttu-id="85c09-105">Nachdem Sie eine Speicherplatz Liste erstellt und Ihr Dateien hinzugefügt haben, können Sie die Liste Abfragen, um die Ziel Laufwerke zu ermitteln, die von den Datei Vorgängen angegeben werden, und den Speicherplatz, der auf jedem Laufwerk erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="85c09-105">After you create a disk-space list and add file operations to it, you can query the list to determine the target drives specified by the file operations, and the disk space required on each drive.</span></span>

<span data-ttu-id="85c09-106">Wenn Sie den erforderlichen Speicherplatz mit dem auf den Ziel Datenträgern verfügbaren Speicherplatz vergleichen, können Sie Programm gesteuert ermitteln, ob genügend Speicherplatz für die aktuelle Installation verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="85c09-106">By comparing the space required to the space available on the target disks, you can programmatically determine whether sufficient space is available for the current installation.</span></span>

<span data-ttu-id="85c09-107">Sie können der Speicherplatz Liste Datei Vorgänge hinzufügen oder aus ihr entfernen und den erforderlichen Speicherplatz neu berechnen.</span><span class="sxs-lookup"><span data-stu-id="85c09-107">You can add or remove file operations to the disk-space list and recalculate the disk space required.</span></span> <span data-ttu-id="85c09-108">Diese Funktion ermöglicht es Ihnen beispielsweise, ein Programm zu schreiben, das mit dem Benutzer interagiert, sodass Sie die zu installierenden Komponenten basierend auf dem benötigten Speicherplatz auswählen können.</span><span class="sxs-lookup"><span data-stu-id="85c09-108">This functionality enables you to, for example, write a program that interacts with the user, allowing him or her to choose what components they want to install based on the disk space required.</span></span>

<span data-ttu-id="85c09-109">Die Speicherplatz Listen-Funktionen suchen automatisch nach bereits vorhandenen Kopien von Dateien auf dem Ziel Datenträger.</span><span class="sxs-lookup"><span data-stu-id="85c09-109">The disk-space list functions automatically check for preexisting copies of files on the target disk.</span></span> <span data-ttu-id="85c09-110">Wenn eine frühere Version der Datei gefunden wird, berechnen die Speicherplatz Listen Funktionen den zusätzlichen Speicherplatz, der zum Durchführen der Datei Vorgänge erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="85c09-110">If a previous version of the file is found, the disk-space list functions calculate the additional space required to complete the file operations.</span></span>

<span data-ttu-id="85c09-111">Wenn ein Kopiervorgang z. b. angibt, dass eine 6000-Byte-Datei auf Laufwerk c kopiert werden soll und eine 2000-Byte-Version dieser Datei bereits auf dem Laufwerk c vorhanden ist, geben die Speicherplatz Funktionen einen erforderlichen Speicherplatz von 4000 Bytes zurück.</span><span class="sxs-lookup"><span data-stu-id="85c09-111">For example, if a copy operation specifies that a 6000-byte file be copied to drive C, and a 2000-byte version of that file already exists on the drive C, the disk space functions would return a required space of 4000 bytes.</span></span> <span data-ttu-id="85c09-112">Der zusätzliche Speicherplatz wird verwendet, um die ältere Version der Datei durch die neuere Version zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="85c09-112">The additional space is used to replace the older version of the file with the newer version.</span></span>

<span data-ttu-id="85c09-113">Die Datenträger-Speicherplatz Liste dient zum Runden der Dateigrößen auf die Datenträger Cluster Grenzen.</span><span class="sxs-lookup"><span data-stu-id="85c09-113">The disk-space list functions round file sizes to the disk cluster boundaries.</span></span>

 

 



