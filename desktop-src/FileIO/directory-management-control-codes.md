---
description: Steuerungs Codes, die mit Dateikomprimierung und Dekomprimierung und mit Analyse Punkten verwendet werden.
ms.assetid: e2e671c7-ef65-4401-8016-649e86f84fec
title: Steuerungs Codes für die Verzeichnis Verwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ef0463860e3c899178ec5b8f9d44bd05cf4278e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867695"
---
# <a name="directory-management-control-codes"></a><span data-ttu-id="8cbf6-103">Steuerungs Codes für die Verzeichnis Verwaltung</span><span class="sxs-lookup"><span data-stu-id="8cbf6-103">Directory Management Control Codes</span></span>

<span data-ttu-id="8cbf6-104">Die folgenden Steuerungs Codes werden bei der [Dateikomprimierung und-Dekomprimierung](file-compression-and-decompression.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="8cbf6-104">The following control codes are used with [file compression and decompression](file-compression-and-decompression.md).</span></span>



| <span data-ttu-id="8cbf6-105">Steuerungscode</span><span class="sxs-lookup"><span data-stu-id="8cbf6-105">Control Code</span></span>                                             | <span data-ttu-id="8cbf6-106">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8cbf6-106">Meaning</span></span>                                                                                                                                     |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8cbf6-107">**Komprimierung von "f" \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8cbf6-107">**FSCTL\_GET\_COMPRESSION**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) | <span data-ttu-id="8cbf6-108">Ruft den aktuellen Komprimierungs Status einer Datei oder eines Verzeichnisses auf einem Volume ab, dessen Dateisystem die Komprimierung pro Stream unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8cbf6-108">Retrieves the current compression state of a file or directory on a volume whose file system supports per-stream compression.</span></span><br/>    |
| [<span data-ttu-id="8cbf6-109">**Komprimierung von ssctl- \_ Satz \_**</span><span class="sxs-lookup"><span data-stu-id="8cbf6-109">**FSCTL\_SET\_COMPRESSION**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) | <span data-ttu-id="8cbf6-110">Legt den Komprimierungs Status einer Datei oder eines Verzeichnisses auf einem Volume fest, dessen Dateisystem die Komprimierung pro Datei und pro Verzeichnis unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8cbf6-110">Sets the compression state of a file or directory on a volume whose file system supports per-file and per-directory compression.</span></span><br/> |



 

<span data-ttu-id="8cbf6-111">Die folgenden Steuerungs Codes werden mit Analyse [Punkten](reparse-points.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="8cbf6-111">The following control codes are used with [reparse points](reparse-points.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8cbf6-112">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="8cbf6-112">In this section</span></span>



| <span data-ttu-id="8cbf6-113">Steuerungscode</span><span class="sxs-lookup"><span data-stu-id="8cbf6-113">Control Code</span></span>                                                                   | <span data-ttu-id="8cbf6-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8cbf6-114">Description</span></span>                                                                                                           |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8cbf6-115">**Lösch Analyse Punkt für den \_ Löschvorgang \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8cbf6-115">**FSCTL\_DELETE\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_reparse_point)<br/> | <span data-ttu-id="8cbf6-116">Löscht einen Analyse Punkt aus der angegebenen Datei bzw. dem angegebenen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="8cbf6-116">Deletes a reparse point from the specified file or directory.</span></span><br/>                                              |
| [<span data-ttu-id="8cbf6-117">**Sicherungspunkt für "f" \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8cbf6-117">**FSCTL\_GET\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_reparse_point)<br/>       | <span data-ttu-id="8cbf6-118">Ruft die Analyse Punktdaten ab, die der Datei oder dem Verzeichnis zugeordnet sind, die durch das angegebene Handle identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="8cbf6-118">Retrieves the reparse point data associated with the file or directory identified by the specified handle.</span></span><br/> |
| [<span data-ttu-id="8cbf6-119">**Analyse Punkt für die ssctl- \_ Gruppe \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8cbf6-119">**FSCTL\_SET\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_reparse_point)<br/>       | <span data-ttu-id="8cbf6-120">Legt einen Analyse Punkt für eine Datei oder ein Verzeichnis fest.</span><span class="sxs-lookup"><span data-stu-id="8cbf6-120">Sets a reparse point on a file or directory.</span></span><br/>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="8cbf6-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8cbf6-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cbf6-122">Dateiverwaltungs-Steuerungscodes</span><span class="sxs-lookup"><span data-stu-id="8cbf6-122">File Management Control Codes</span></span>](file-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="8cbf6-123">Volumeverwaltungs-Steuerungscodes</span><span class="sxs-lookup"><span data-stu-id="8cbf6-123">Volume Management Control Codes</span></span>](volume-management-control-codes.md)
</dt> </dl>

 

