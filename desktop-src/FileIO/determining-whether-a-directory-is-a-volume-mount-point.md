---
description: Bestimmen, ob ein angegebenes Verzeichnis ein bereitgestellter Ordner ist.
ms.assetid: b4a2c3d7-8805-41de-b316-592e77076570
title: Bestimmen, ob ein Verzeichnis ein bereitgestellter Ordner ist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca7492a3114ff0c9c9ce0685c6d3e2b94724457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867696"
---
# <a name="determining-whether-a-directory-is-a-mounted-folder"></a><span data-ttu-id="526d9-103">Bestimmen, ob ein Verzeichnis ein bereitgestellter Ordner ist</span><span class="sxs-lookup"><span data-stu-id="526d9-103">Determining Whether a Directory Is a Mounted Folder</span></span>

<span data-ttu-id="526d9-104">Es ist hilfreich, zu bestimmen, ob ein Verzeichnis ein bereitgestellter Ordner ist, wenn Sie z. b. eine Sicherungs-oder Suchanwendung verwenden, die auf ein Volume beschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="526d9-104">It is useful to determine whether a directory is a mounted folder when, for example, you are using a backup or search application that is limited to one volume.</span></span> <span data-ttu-id="526d9-105">Eine solche Anwendung kann Informationen auf mehreren Volumes erreichen, wenn Sie Funktionen wie [**setvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) verwenden, um bereitgestellte Ordner für die anderen Volumes auf dem Volume zu erstellen, auf das die Anwendung beschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="526d9-105">Such an application can reach information on multiple volumes if you use functions such as [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) to create mounted folders for the other volumes on the volume that the application is limited to.</span></span> <span data-ttu-id="526d9-106">Weitere Informationen finden Sie unter [Erstellen eingebundenes Ordner](mounting-and-dismounting-a-volume.md).</span><span class="sxs-lookup"><span data-stu-id="526d9-106">For more information, see [Creating Mounted Folders](mounting-and-dismounting-a-volume.md).</span></span>

<span data-ttu-id="526d9-107">Um zu ermitteln, ob ein angegebenes Verzeichnis ein bereitgestellter Ordner ist, müssen Sie zuerst die [**getfileattribute**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) -Funktion aufrufen und das File Attribute-Flag für den Analyse **\_ \_ \_ Punkt** im Rückgabewert überprüfen, um festzustellen, ob dem Verzeichnis ein Analyse Punkt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="526d9-107">To determine if a specified directory is a mounted folder, first call the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) function and inspect the **FILE\_ATTRIBUTE\_REPARSE\_POINT** flag in the return value to see if the directory has an associated reparse point.</span></span> <span data-ttu-id="526d9-108">Wenn dies der Fall ist, verwenden Sie die Funktionen " [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) " und " [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) ", um das Analyse-Tag im **dwReserved0** -Member der [**Win32- \_ \_ Datenstruktur suchen**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="526d9-108">If it does, use the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) and [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) functions to obtain the reparse tag in the **dwReserved0** member of the [**WIN32\_FIND\_DATA**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) structure.</span></span> <span data-ttu-id="526d9-109">Um zu ermitteln, ob der Analyse Punkt ein bereitgestellter Ordner (und nicht eine andere Form des Analyse Punkts) ist, überprüfen Sie, ob der Tagwert dem Wert-e/a- **\_ \_ tageinstellungspunkt \_ \_** entspricht.</span><span class="sxs-lookup"><span data-stu-id="526d9-109">To determine if the reparse point is a mounted folder (and not some other form of reparse point), test whether the tag value equals the value **IO\_REPARSE\_TAG\_MOUNT\_POINT**.</span></span> <span data-ttu-id="526d9-110">Weitere Informationen finden Sie unter Analyse [Punkte](reparse-points.md).</span><span class="sxs-lookup"><span data-stu-id="526d9-110">For more information, see [Reparse Points](reparse-points.md).</span></span>

<span data-ttu-id="526d9-111">Verwenden Sie die [**getvolumenameforvolumemountpoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) -Funktion, um das Ziel Volume eines eingebundenen Ordners abzurufen.</span><span class="sxs-lookup"><span data-stu-id="526d9-111">To obtain the target volume of a mounted folder, use the [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) function.</span></span>

<span data-ttu-id="526d9-112">Auf ähnliche Weise können Sie ermitteln, ob ein Analyse Punkt eine symbolische Verknüpfung ist, indem Sie überprüfen, ob der Tagwert e/a-Analyse **\_ Tags- \_ \_ symlink** ist.</span><span class="sxs-lookup"><span data-stu-id="526d9-112">In a similar manner, you can determine if a reparse point is a symbolic link by testing whether the tag value is **IO\_REPARSE\_TAG\_SYMLINK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="526d9-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="526d9-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="526d9-114">**Datei Attribut Konstanten**</span><span class="sxs-lookup"><span data-stu-id="526d9-114">**File Attribute Constants**</span></span>](file-attribute-constants.md)
</dt> </dl>

 

 



