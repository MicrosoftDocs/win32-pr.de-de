---
description: Auf einem NTFS-Dateisystem Volume weist jede Datei und jedes Verzeichnis ein Komprimierungs Attribut auf.
ms.assetid: 8aca120c-22a7-4dc8-a921-dfcec1277452
title: Komprimierungs Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e8e86eebe919476851f35f77cf10d6a07035d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869092"
---
# <a name="compression-attribute"></a><span data-ttu-id="8c215-103">Komprimierungs Attribut</span><span class="sxs-lookup"><span data-stu-id="8c215-103">Compression Attribute</span></span>

<span data-ttu-id="8c215-104">Auf einem NTFS-Dateisystem Volume weist jede Datei und jedes Verzeichnis ein *Komprimierungs Attribut* auf.</span><span class="sxs-lookup"><span data-stu-id="8c215-104">On an NTFS file system volume, each file and directory has a *compression attribute*.</span></span> <span data-ttu-id="8c215-105">Andere Dateisysteme können auch ein Komprimierungs Attribut für einzelne Dateien und Verzeichnisse implementieren.</span><span class="sxs-lookup"><span data-stu-id="8c215-105">Other file systems may also implement a compression attribute for individual files and directories.</span></span>

<span data-ttu-id="8c215-106">Sie können bestimmen, ob ein Dateisystem ein Komprimierungs Attribut für Dateien und Verzeichnisse unterstützt, indem Sie die [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) -Funktion aufrufen und das Bitflag für die **\_ \_ Komprimierung der Datei Datei** untersuchen.</span><span class="sxs-lookup"><span data-stu-id="8c215-106">You can determine whether a file system supports a compression attribute for files and directories by calling the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examining the **FILE\_FILE\_COMPRESSION** bit flag.</span></span>

<span data-ttu-id="8c215-107">Verwenden Sie die Funktion [**getfileattribute**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) oder [**getfileattributesex**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) , um das Komprimierungs Attribut einer Datei oder eines Verzeichnisses zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="8c215-107">Use the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) or [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) function to determine the compression attribute of a file or directory.</span></span>

<span data-ttu-id="8c215-108">Wenn das Komprimierungs Attribut einer Datei festgelegt ist (**file- \_ Attribut \_ komprimiert**), werden alle Daten in der Datei komprimiert.</span><span class="sxs-lookup"><span data-stu-id="8c215-108">If a file's compression attribute is set (**FILE\_ATTRIBUTE\_COMPRESSED**), all data in the file is compressed.</span></span> <span data-ttu-id="8c215-109">Wenn das Attribut eindeutig ist, wird keine der Daten in der Datei komprimiert.</span><span class="sxs-lookup"><span data-stu-id="8c215-109">If the attribute is clear, none of the data in the file is compressed.</span></span> <span data-ttu-id="8c215-110">Es gibt keinen teilweise komprimierten Zustand aus einer Programmier Perspektive im Benutzermodus. Das Komprimierungs Attribut ist ein einfacher boolescher Indikator für den Komprimierungs Status.</span><span class="sxs-lookup"><span data-stu-id="8c215-110">There is no partially compressed state from a user-mode programming perspective; the compression attribute is a simple Boolean indicator of compression state.</span></span>

<span data-ttu-id="8c215-111">Das Komprimierungs Attribut eines Verzeichnisses stellt ein Standard Komprimierungs Attribut für neu erstellte Dateien und Unterverzeichnisse bereit.</span><span class="sxs-lookup"><span data-stu-id="8c215-111">A directory's compression attribute provides a default compression attribute for newly created files and subdirectories.</span></span> <span data-ttu-id="8c215-112">Wenn Sie zum Erstellen einer neuen Datei oder eines neuen Verzeichnisses " [**kreatefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) " oder " [**kreatedirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) " aufrufen, erbt die neue Datei bzw. das zugehörige Verzeichnis das Komprimierungs Attribut des übergeordneten Verzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="8c215-112">When you call [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) or [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) to create a new file or directory, the new file or directory inherits the compression attribute of its parent directory.</span></span>

<span data-ttu-id="8c215-113">Um das **\_ \_ komprimierte Attribut file Attribute** für eine Datei oder ein Verzeichnis zu ändern, müssen Sie die [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) -Funktion mit dem Code für die [**\_ \_ Komprimierung des FSCTL-Satzes**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) verwenden.</span><span class="sxs-lookup"><span data-stu-id="8c215-113">To modify the **FILE\_ATTRIBUTE\_COMPRESSED** attribute for a file or directory, you must use the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the [**FSCTL\_SET\_COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) control code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c215-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8c215-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c215-115">**Datei Attribut Konstanten**</span><span class="sxs-lookup"><span data-stu-id="8c215-115">**File Attribute Constants**</span></span>](file-attribute-constants.md)
</dt> </dl>

 

 
