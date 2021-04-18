---
description: Volumes werden von einem Gerätetreiber implementiert, der als Volumemanager bezeichnet wird.
ms.assetid: 424ddbd9-5692-45ef-95fb-7b00b09e3205
title: Informationen zur Volumeverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0767d137eeecaa4ded060382b689b5ea3780dcbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351059"
---
# <a name="about-volume-management"></a><span data-ttu-id="6709e-103">Informationen zur Volumeverwaltung</span><span class="sxs-lookup"><span data-stu-id="6709e-103">About Volume Management</span></span>

<span data-ttu-id="6709e-104">Volumes werden von einem Gerätetreiber implementiert, der als Volumemanager bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="6709e-104">Volumes are implemented by a device driver called a volume manager.</span></span> <span data-ttu-id="6709e-105">Beispiele hierfür sind der Ftdisk-Manager, der Logical Disk Manager (LDM) und der Veritas Logical Volume Manager (LVM).</span><span class="sxs-lookup"><span data-stu-id="6709e-105">Examples include the FtDisk Manager, the Logical Disk Manager (LDM), and the VERITAS Logical Volume Manager (LVM).</span></span> <span data-ttu-id="6709e-106">Volumemanager bieten eine Schicht physischer Abstraktion, Datenschutz (mit einer Form von RAID) und Leistung.</span><span class="sxs-lookup"><span data-stu-id="6709e-106">Volume managers provide a layer of physical abstraction, data protection (using some form of RAID), and performance.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6709e-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="6709e-107">In this section</span></span>



| <span data-ttu-id="6709e-108">Thema</span><span class="sxs-lookup"><span data-stu-id="6709e-108">Topic</span></span>                                                                       | <span data-ttu-id="6709e-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6709e-109">Description</span></span>                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6709e-110">Datei System Erkennung</span><span class="sxs-lookup"><span data-stu-id="6709e-110">File System Recognition</span></span>](file-system-recognition.md)<br/>           | <span data-ttu-id="6709e-111">Das Ziel der Dateisystem Erkennung besteht darin, dass das Windows-Betriebssystem über eine zusätzliche Option für ein gültiges, aber unbekanntes Dateisystem als "RAW" verfügt.</span><span class="sxs-lookup"><span data-stu-id="6709e-111">The goal of file system recognition is to allow the Windows operating system to have an additional option for a valid but unrecognized file system other than "RAW".</span></span><br/>                                                                                                         |
| [<span data-ttu-id="6709e-112">Benennen eines Volumes</span><span class="sxs-lookup"><span data-stu-id="6709e-112">Naming a Volume</span></span>](naming-a-volume.md)<br/>                           | <span data-ttu-id="6709e-113">Eine Bezeichnung ist ein benutzerfreundlicher Name, der einem Volume zugewiesen wird, normalerweise von einem Endbenutzer, um die Erkennung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="6709e-113">A label is a user-friendly name that is assigned to a volume, usually by an end user, to make it easier to recognize.</span></span> <span data-ttu-id="6709e-114">Ein Volume kann eine Bezeichnung, einen Laufwerk Buchstaben, beides oder keines von beiden aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6709e-114">A volume can have a label, a drive letter, both, or neither.</span></span> <span data-ttu-id="6709e-115">Um die Bezeichnung für ein Volume festzulegen, verwenden Sie die Funktion [**setvolumelabel**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela) .</span><span class="sxs-lookup"><span data-stu-id="6709e-115">To set the label for a volume, use the [**SetVolumeLabel**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela) function.</span></span><br/> |
| [<span data-ttu-id="6709e-116">Auflisten von Volumes</span><span class="sxs-lookup"><span data-stu-id="6709e-116">Enumerating Volumes</span></span>](enumerating-volumes.md)<br/>                   | <span data-ttu-id="6709e-117">Zum Erstellen einer kompletten Liste der Volumes auf einem Computer oder zum Bearbeiten der einzelnen Volumes können Sie Volumes auflisten.</span><span class="sxs-lookup"><span data-stu-id="6709e-117">To make a complete list of the volumes on a computer, or to manipulate each volume in turn, you can enumerate volumes.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="6709e-118">Abrufen von Volumeinformationen</span><span class="sxs-lookup"><span data-stu-id="6709e-118">Obtaining Volume Information</span></span>](obtaining-volume-information.md)<br/> | <span data-ttu-id="6709e-119">Vor dem Zugriff auf Dateien und Verzeichnisse auf einem bestimmten Volume sollten Sie die Funktionen des Dateisystems mithilfe der [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) -Funktion ermitteln.</span><span class="sxs-lookup"><span data-stu-id="6709e-119">Before you access files and directories on a given volume, you should determine the capabilities of the file system by using the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function.</span></span><br/>                                                                              |
| [<span data-ttu-id="6709e-120">Ändern von Journalen</span><span class="sxs-lookup"><span data-stu-id="6709e-120">Change Journals</span></span>](change-journals.md)<br/>                           | <span data-ttu-id="6709e-121">Wenn eine Änderung an einer Datei oder einem Verzeichnis in einem Volume vorgenommen wird, wird das Änderungs Journal für die Aktualisierung des Volumes mit einer Beschreibung der Änderung und des Datei-oder Verzeichnis namens aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6709e-121">When any change is made to a file or directory in a volume, the USN change journal for that volume is updated with a description of the change and the name of the file or directory.</span></span><br/>                                                                                        |
| [<span data-ttu-id="6709e-122">Eingebundene Ordner</span><span class="sxs-lookup"><span data-stu-id="6709e-122">Mounted Folders</span></span>](volume-mount-points.md)<br/>                       | <span data-ttu-id="6709e-123">Mithilfe bereitgestellter Ordner können Sie unterschiedliche Dateisysteme wie das NTFS-Dateisystem, ein 16-Bit-FAT-Dateisystem und ein ISO-9660-Dateisystem auf einem CD-ROM-Laufwerk in einem logischen Dateisystem auf einem einzelnen NTFS-Volume vereinheitlichen.</span><span class="sxs-lookup"><span data-stu-id="6709e-123">Using mounted folders, you can unify disparate file systems such as the NTFS file system, a 16-bit FAT file system, and an ISO-9660 file system on a CD-ROM drive into one logical file system on a single NTFS volume.</span></span><br/>                                                      |
| [<span data-ttu-id="6709e-124">Master Dateitabelle</span><span class="sxs-lookup"><span data-stu-id="6709e-124">Master File Table</span></span>](master-file-table.md)<br/>                       | <span data-ttu-id="6709e-125">Alle Informationen zu einer Datei, einschließlich Größe, Zeit-und Datumsstempel, Berechtigungen und Dateninhalt, werden entweder in MFT-Einträgen (Master File Table) oder außerhalb des in der MFT-Einträge beschriebenen Speicherplatzes gespeichert.</span><span class="sxs-lookup"><span data-stu-id="6709e-125">All information about a file, including its size, time and date stamps, permissions, and data content, is stored either in master file table (MFT) entries, or in space outside the MFT that is described by MFT entries.</span></span><br/>                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="6709e-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6709e-126">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6709e-127">[Technische Referenz zu einfachen Datenträgern und Volumes](/previous-versions/windows/it-pro/windows-server-2003/cc784732(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="6709e-127">[Basic Disks and Volumes Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc784732(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="6709e-128">[Technische Referenz zu dynamischen Datenträgern und Volumes](/previous-versions/windows/it-pro/windows-server-2003/cc785638(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="6709e-128">[Dynamic Disks and Volumes Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc785638(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="6709e-129">Referenz zur Volumeverwaltung</span><span class="sxs-lookup"><span data-stu-id="6709e-129">Volume Management Reference</span></span>](volume-management-reference.md)
</dt> </dl>

 

