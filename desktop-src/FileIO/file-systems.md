---
description: Verzeichnisse mit Verzeichniseintrags Tabelle, Verzeichnis Handles, Analyse Punkten verwalten.
title: Lokale Dateisysteme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92f624ef1999b81adb63ba1d5b7e349259cabd53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755160"
---
# <a name="local-file-systems"></a><span data-ttu-id="c6de9-103">Lokale Dateisysteme</span><span class="sxs-lookup"><span data-stu-id="c6de9-103">Local File Systems</span></span>

<span data-ttu-id="c6de9-104">Ein *Dateisystem* ermöglicht Anwendungen das Speichern und Abrufen von Dateien auf Speichergeräten.</span><span class="sxs-lookup"><span data-stu-id="c6de9-104">A *file system* enables applications to store and retrieve files on storage devices.</span></span> <span data-ttu-id="c6de9-105">Dateien werden in einer hierarchischen Struktur abgelegt.</span><span class="sxs-lookup"><span data-stu-id="c6de9-105">Files are placed in a hierarchical structure.</span></span> <span data-ttu-id="c6de9-106">Das Dateisystem gibt Benennungs Konventionen für Dateien und das Format zum Angeben des Pfads zu einer Datei in der Baumstruktur an.</span><span class="sxs-lookup"><span data-stu-id="c6de9-106">The file system specifies naming conventions for files and the format for specifying the path to a file in the tree structure.</span></span>

<span data-ttu-id="c6de9-107">Jedes Dateisystem besteht aus einem oder mehreren Treibern und Dynamic-Link-Bibliotheken, die die Datenformate und Features des Dateisystems definieren.</span><span class="sxs-lookup"><span data-stu-id="c6de9-107">Each file system consists of one or more drivers and dynamic-link libraries that define the data formats and features of the file system.</span></span> <span data-ttu-id="c6de9-108">Dateisysteme können auf vielen unterschiedlichen Arten von Speichergeräten vorhanden sein, z. b. Festplatten, Jukeboxes, wechselbare optische Datenträger, Band Sicherungs Einheiten und Speicherkarten.</span><span class="sxs-lookup"><span data-stu-id="c6de9-108">File systems can exist on many different types of storage devices, including hard disks, jukeboxes, removable optical disks, tape back-up units, and memory cards.</span></span>

<span data-ttu-id="c6de9-109">Alle von Windows unterstützten Dateisysteme verfügen über die folgenden Speicherkomponenten:</span><span class="sxs-lookup"><span data-stu-id="c6de9-109">All file systems supported by Windows have the following storage components:</span></span>

-   <span data-ttu-id="c6de9-110">Volumes:</span><span class="sxs-lookup"><span data-stu-id="c6de9-110">Volumes.</span></span> <span data-ttu-id="c6de9-111">Ein *Volume* ist eine Sammlung von Verzeichnissen und Dateien.</span><span class="sxs-lookup"><span data-stu-id="c6de9-111">A *volume* is a collection of directories and files.</span></span>
-   <span data-ttu-id="c6de9-112">Verzeichnisse:</span><span class="sxs-lookup"><span data-stu-id="c6de9-112">Directories.</span></span> <span data-ttu-id="c6de9-113">Ein *Verzeichnis* ist eine hierarchische Sammlung von Verzeichnissen und Dateien.</span><span class="sxs-lookup"><span data-stu-id="c6de9-113">A *directory* is a hierarchical collection of directories and files.</span></span>
-   <span data-ttu-id="c6de9-114">Dateien.</span><span class="sxs-lookup"><span data-stu-id="c6de9-114">Files.</span></span> <span data-ttu-id="c6de9-115">Eine *Datei* ist eine logische Gruppierung verwandter Daten.</span><span class="sxs-lookup"><span data-stu-id="c6de9-115">A *file* is a logical grouping of related data.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c6de9-116">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c6de9-116">In this section</span></span>



| <span data-ttu-id="c6de9-117">Thema</span><span class="sxs-lookup"><span data-stu-id="c6de9-117">Topic</span></span>                                                                | <span data-ttu-id="c6de9-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6de9-118">Description</span></span>                                                                                                                                                                                                                                |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c6de9-119">Verzeichnisverwaltung</span><span class="sxs-lookup"><span data-stu-id="c6de9-119">Directory Management</span></span>](directory-management.md)<br/>          | <span data-ttu-id="c6de9-120">Ein *Verzeichnis* ist eine hierarchische Sammlung von Verzeichnissen und Dateien.</span><span class="sxs-lookup"><span data-stu-id="c6de9-120">A *directory* is a hierarchical collection of directories and files.</span></span> <span data-ttu-id="c6de9-121">Die einzige Einschränkung der Anzahl von Dateien, die in einem einzelnen Verzeichnis enthalten sein kann, ist die physische Größe des Datenträgers, auf dem sich das Verzeichnis befindet.</span><span class="sxs-lookup"><span data-stu-id="c6de9-121">The only constraint on the number of files that can be contained in a single directory is the physical size of the disk on which the directory is located.</span></span><br/> |
| [<span data-ttu-id="c6de9-122">Datenträgerverwaltung</span><span class="sxs-lookup"><span data-stu-id="c6de9-122">Disk Management</span></span>](disk-management.md)<br/>                    | <span data-ttu-id="c6de9-123">Eine *Festplatte* ist ein Festplatten Datenträger innerhalb eines Computers, der einen relativ schnellen Zugriff auf große Datenmengen speichert und ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="c6de9-123">A *hard disk* is a rigid disk inside a computer that stores and provides relatively quick access to large amounts of data.</span></span> <span data-ttu-id="c6de9-124">Dabei handelt es sich um den Typ des Speichers, der am häufigsten mit Windows verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c6de9-124">It is the type of storage most often used with Windows.</span></span> <span data-ttu-id="c6de9-125">Das System unterstützt auch Wechsel Datenträger.</span><span class="sxs-lookup"><span data-stu-id="c6de9-125">The system also supports removable media.</span></span><br/>    |
| [<span data-ttu-id="c6de9-126">Dateiverwaltung</span><span class="sxs-lookup"><span data-stu-id="c6de9-126">File Management</span></span>](file-management.md)<br/>                    | <span data-ttu-id="c6de9-127">Ein *Datei Objekt* bietet eine Darstellung einer Ressource (entweder ein physisches Gerät oder eine Ressource auf einem physischen Gerät), die vom e/a-System verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c6de9-127">A *file object* provides a representation of a resource (either a physical device or a resource located on a physical device) that can be managed by the I/O system.</span></span><br/>                                                            |
| [<span data-ttu-id="c6de9-128">Transaktionale NTFS (TxF)</span><span class="sxs-lookup"><span data-stu-id="c6de9-128">Transactional NTFS (TxF)</span></span>](transactional-ntfs-portal.md)<br/> | <span data-ttu-id="c6de9-129">Transaktionale NTFS (TxF) ermöglicht die Ausführung von Datei Vorgängen auf einem NTFS-Dateisystem Volume in einer Transaktion.</span><span class="sxs-lookup"><span data-stu-id="c6de9-129">Transactional NTFS (TxF) allows file operations on an NTFS file system volume to be performed in a transaction.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="c6de9-130">Volumeverwaltung</span><span class="sxs-lookup"><span data-stu-id="c6de9-130">Volume Management</span></span>](volume-management.md)<br/>                | <span data-ttu-id="c6de9-131">Die höchste Organisationsebene im Dateisystem ist das *Volume*.</span><span class="sxs-lookup"><span data-stu-id="c6de9-131">The highest level of organization in the file system is the *volume*.</span></span> <span data-ttu-id="c6de9-132">Ein Dateisystem befindet sich auf einem Volume.</span><span class="sxs-lookup"><span data-stu-id="c6de9-132">A file system resides on a volume.</span></span><br/>                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="c6de9-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c6de9-133">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c6de9-134">[Technische Referenz zu FAT](/previous-versions/windows/it-pro/windows-server-2003/cc758586(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="c6de9-134">[FAT Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc758586(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="c6de9-135">[Technologien für Dateisysteme](/previous-versions/windows/it-pro/windows-server-2003/cc778296(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="c6de9-135">[File Systems Technologies](/previous-versions/windows/it-pro/windows-server-2003/cc778296(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="c6de9-136">[Technische Referenz zu NTFS](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="c6de9-136">[NTFS Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))</span></span>
</dt> </dl>

 

