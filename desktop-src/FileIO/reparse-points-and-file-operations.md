---
description: Beschreibt, wie Analyse Punkte das Verhalten von Dateisystemen ermöglichen, die von den meisten Windows-Entwicklern erwartet werden.
ms.assetid: 1aaebda9-0013-4282-9ae1-7c829e171942
title: Analyse Punkte und Datei Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be1132197cd689157cd9f219afa5bfc1474b587c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217474"
---
# <a name="reparse-points-and-file-operations"></a><span data-ttu-id="5b625-103">Analyse Punkte und Datei Vorgänge</span><span class="sxs-lookup"><span data-stu-id="5b625-103">Reparse Points and File Operations</span></span>

<span data-ttu-id="5b625-104">Analyse *Punkte* ermöglichen das Verhalten des Dateisystems, das von dem Verhalten abweicht, an das die meisten Windows-Entwickler gewöhnt sind. Daher sind diese Verhaltensweisen beim Schreiben von Anwendungen, die Dateien bearbeiten, wichtig für robuste und zuverlässige Anwendungen, die für den Zugriff auf Dateisysteme gedacht sind, die Analyse Punkte unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5b625-104">*Reparse points* enable file system behavior that departs from the behavior most Windows developers may be accustomed to, therefore being aware of these behaviors when writing applications that manipulate files is vital to robust and reliable applications intended to access file systems that support reparse points.</span></span> <span data-ttu-id="5b625-105">Der Umfang dieser Überlegungen hängt von der spezifischen Implementierung und dem zugehörigen Dateisystem Filter Verhalten eines bestimmten Analyse Punkts ab, der Benutzer definiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="5b625-105">The extent of these considerations will depend on the specific implementation and associated file system filter behavior of a particular reparse point, which can be user-defined.</span></span> <span data-ttu-id="5b625-106">Weitere Informationen finden Sie unter Analyse [Punkte](reparse-points.md).</span><span class="sxs-lookup"><span data-stu-id="5b625-106">For more information, see [Reparse Points](reparse-points.md).</span></span>

<span data-ttu-id="5b625-107">Betrachten Sie die folgenden Beispiele für Implementierungen von NTFS-Analyse Punkten, die bereitgestellte Ordner, verknüpfte Dateien und den Microsoft-Remote Speicher Server umfassen:</span><span class="sxs-lookup"><span data-stu-id="5b625-107">Consider the following examples regarding NTFS reparse point implementations, which include mounted folders, linked files, and the Microsoft Remote Storage Server:</span></span>

-   <span data-ttu-id="5b625-108">Sicherungs Anwendungen, die [Datei Datenströme](file-streams.md) verwenden, sollten beim Sichern von Dateien mit Analyse Punkten Sicherungs Analysedaten in der Win32- **\_ \_ Daten** [**Strom- \_ \_ ID**](/windows/desktop/api/winbase/ns-winbase-win32_stream_id) -Struktur angeben.</span><span class="sxs-lookup"><span data-stu-id="5b625-108">Backup applications that use [file streams](file-streams.md) should specify **BACKUP\_REPARSE\_DATA** in the [**WIN32\_STREAM\_ID**](/windows/desktop/api/winbase/ns-winbase-win32_stream_id) structure when backing up files with reparse points.</span></span>
-   <span data-ttu-id="5b625-109">Anwendungen, die die Funktion " [**deatefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) " verwenden, sollten beim Öffnen der Datei das Flag zum Öffnen des Analyse **\_ \_ \_ \_ Punkts für den Dateiflag** angeben, wenn es sich um einen Analyse Punkt handelt.</span><span class="sxs-lookup"><span data-stu-id="5b625-109">Applications that use the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function should specify the **FILE\_FLAG\_OPEN\_REPARSE\_POINT** flag when opening the file if it is a reparse point.</span></span> <span data-ttu-id="5b625-110">Weitere Informationen finden Sie unter [Erstellen und Öffnen von Dateien](creating-and-opening-files.md).</span><span class="sxs-lookup"><span data-stu-id="5b625-110">For more information, see [Creating and Opening Files](creating-and-opening-files.md).</span></span>
-   <span data-ttu-id="5b625-111">Für den Prozess der [Defragmentierung von Dateien](defragmenting-files.md) ist eine spezielle Behandlung von Analyse Punkten erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5b625-111">The process of [defragmenting files](defragmenting-files.md) requires special handling for reparse points.</span></span>
-   <span data-ttu-id="5b625-112">Viren Erkennungs Anwendungen sollten nach Analyse Punkten suchen, die auf verknüpfte Dateien hinweisen.</span><span class="sxs-lookup"><span data-stu-id="5b625-112">Virus detection applications should search for reparse points that indicate linked files.</span></span>
-   <span data-ttu-id="5b625-113">Die meisten Anwendungen sollten spezielle Aktionen für Dateien durchführen, die in den langfristigen Speicher verschoben wurden, wenn der Benutzer nur benachrichtigt wird, dass es eine Weile dauern kann, bis die Datei abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5b625-113">Most applications should take special actions for files that have been moved to long-term storage, if only to notify the user that it may take a while to retrieve the file.</span></span>
-   <span data-ttu-id="5b625-114">Die [**OpenFileById**](/windows/desktop/api/WinBase/nf-winbase-openfilebyid) -Funktion öffnet entweder die Datei oder den Analyse Punkt, abhängig von der Verwendung des **\_ Dateiflag zum \_ Öffnen \_ \_** des Analyse Punkts.</span><span class="sxs-lookup"><span data-stu-id="5b625-114">The [**OpenFileById**](/windows/desktop/api/WinBase/nf-winbase-openfilebyid) function will either open the file or the reparse point, depending on the use of the **FILE\_FLAG\_OPEN\_REPARSE\_POINT** flag.</span></span>
-   <span data-ttu-id="5b625-115">Symbolische Verknüpfungen, als Analyse Punkte, weisen bestimmte [Programmier Überlegungen](symbolic-link-programming-considerations.md) für Sie auf.</span><span class="sxs-lookup"><span data-stu-id="5b625-115">Symbolic links, as reparse points, have certain [programming considerations](symbolic-link-programming-considerations.md) specific to them.</span></span>
-   <span data-ttu-id="5b625-116">Die [**\_ \_ \_ Volumeverwaltungsaktivitäten**](/windows/desktop/api/WinIoCtl/ns-winioctl-read_usn_journal_data_v0) zum Lesen von Änderungs Journal Datensätzen der Update Sequenznummer (Update Sequence Number, Hern) erfordern eine besondere Behandlung für Analyse Punkte, wenn die Datenstrukturen des Datensatzes und des Daten [**\_ Satzes**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="5b625-116">Volume management activities for reading update sequence number (USN) change journal records require special handling for reparse points when using the [**USN\_RECORD**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) and [**READ\_USN\_JOURNAL\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-read_usn_journal_data_v0) structures.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b625-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5b625-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b625-118">Bestimmen, ob ein Verzeichnis ein bereitgestellter Ordner ist</span><span class="sxs-lookup"><span data-stu-id="5b625-118">Determining Whether a Directory Is a Mounted Folder</span></span>](determining-whether-a-directory-is-a-volume-mount-point.md)
</dt> <dt>

[<span data-ttu-id="5b625-119">Erstellen von bereitgestellten Ordnern</span><span class="sxs-lookup"><span data-stu-id="5b625-119">Creating Mounted Folders</span></span>](mounting-and-dismounting-a-volume.md)
</dt> <dt>

[<span data-ttu-id="5b625-120">Symbolische Verknüpfungs Effekte in Dateisystemfunktionen</span><span class="sxs-lookup"><span data-stu-id="5b625-120">Symbolic Link Effects on File Systems Functions</span></span>](symbolic-link-effects-on-file-systems-functions.md)
</dt> </dl>

 

 
