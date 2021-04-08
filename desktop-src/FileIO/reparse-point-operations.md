---
description: Beschreibt die Analyse Punkt Vorgänge, die Sie mithilfe von DeviceIoControl ausführen können.
ms.assetid: c7279203-2443-401e-b541-038954094266
title: Analyse Punkt Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0889120af50c8415ed255b8274b76f2d53e6a563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050290"
---
# <a name="reparse-point-operations"></a><span data-ttu-id="a8058-103">Analyse Punkt Vorgänge</span><span class="sxs-lookup"><span data-stu-id="a8058-103">Reparse Point Operations</span></span>

<span data-ttu-id="a8058-104">Um zu ermitteln, ob ein Dateisystem Analyse Punkte unterstützt, müssen Sie die [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) -Funktion aufrufen und die **Datei \_ unterstützt \_ \_** das Bitflag "Analyse Punkte" untersuchen.</span><span class="sxs-lookup"><span data-stu-id="a8058-104">To determine whether a file system supports reparse points, call the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examine the **FILE\_SUPPORTS\_REPARSE\_POINTS** bit flag.</span></span>

<span data-ttu-id="a8058-105">Mit der Funktion " [**de viceiocontrol**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) " können Sie Analyse Punkte festlegen, ändern, abrufen und entfernen.</span><span class="sxs-lookup"><span data-stu-id="a8058-105">The [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function enables you to set, modify, obtain, and remove reparse points.</span></span> <span data-ttu-id="a8058-106">In der folgenden Tabelle werden die Vorgänge für Analyse Punkte beschrieben, die Sie mithilfe von **DeviceIoControl** ausführen können.</span><span class="sxs-lookup"><span data-stu-id="a8058-106">The following table describes the reparse point operations that you can perform using **DeviceIoControl**.</span></span>



| <span data-ttu-id="a8058-107">Vorgang</span><span class="sxs-lookup"><span data-stu-id="a8058-107">Operation</span></span>                                                           | <span data-ttu-id="a8058-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a8058-108">Description</span></span>                                                                                     |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8058-109">**Analyse Punkt für die ssctl- \_ Gruppe \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a8058-109">**FSCTL\_SET\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_reparse_point)       | <span data-ttu-id="a8058-110">Ermöglicht dem aufrufenden Programm, einen neuen Analyse Punkt festzulegen oder eine vorhandene zu ändern.</span><span class="sxs-lookup"><span data-stu-id="a8058-110">Allows the calling program to set a new reparse point, or to modify an existing one.</span></span><br/> |
| [<span data-ttu-id="a8058-111">**Sicherungspunkt für "f" \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a8058-111">**FSCTL\_GET\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_reparse_point)       | <span data-ttu-id="a8058-112">Ruft die Informationen ab, die in einem vorhandenen Analyse Punkt gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="a8058-112">Obtains the information stored in an existing reparse point.</span></span><br/>                         |
| [<span data-ttu-id="a8058-113">**Lösch Analyse Punkt für den \_ Löschvorgang \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a8058-113">**FSCTL\_DELETE\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_reparse_point) | <span data-ttu-id="a8058-114">Entfernt einen vorhandenen Analyse Punkt.</span><span class="sxs-lookup"><span data-stu-id="a8058-114">Removes an existing reparse point.</span></span><br/>                                                   |



 

<span data-ttu-id="a8058-115">Wenn Sie einen Analyse Punkt ändern, Abrufen oder löschen, müssen Sie in dem Vorgang, der in der Datei enthalten ist, dasselbe Analyse Kennzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="a8058-115">If you are modifying, getting, or deleting a reparse point, you must specify the same reparse tag in the operation that is contained in the file.</span></span> <span data-ttu-id="a8058-116">Andernfalls schlägt der Vorgang mit dem Fehler Fehleranalyse **- \_ \_ tagkonflikt \_ fehl**.</span><span class="sxs-lookup"><span data-stu-id="a8058-116">Otherwise, the operation will fail with the error **ERROR\_REPARSE\_TAG\_MISMATCH**.</span></span> <span data-ttu-id="a8058-117">Wenn Sie einen Analyse Punkt ändern oder löschen, müssen Sie auch die Analyse- **GUID** in dem Vorgang angeben, der in der Datei enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="a8058-117">If you are modifying or deleting a reparse point, you must also specify the reparse **GUID** in the operation that is contained in the file.</span></span> <span data-ttu-id="a8058-118">Andernfalls schlägt der Vorgang mit dem Fehler Fehleranalyse **- \_ \_ Attribut \_ Konflikt** fehl.</span><span class="sxs-lookup"><span data-stu-id="a8058-118">Otherwise, the operation will fail with the error **ERROR\_REPARSE\_ATTRIBUTE\_CONFLICT**.</span></span>

<span data-ttu-id="a8058-119">Verwenden Sie die [**getfileattributfunktion**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) , um zu bestimmen, ob eine Datei oder ein Verzeichnis einen Analyse Punkt enthält.</span><span class="sxs-lookup"><span data-stu-id="a8058-119">To determine whether a file or directory contains a reparse point, use the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) function.</span></span> <span data-ttu-id="a8058-120">Wenn die Datei oder das Verzeichnis über einen zugeordneten Analyse Punkt verfügt, wird das Attribut " **file \_ Attribute Analyse \_ \_ Point** " festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a8058-120">If the file or directory has an associated reparse point, the **FILE\_ATTRIBUTE\_REPARSE\_POINT** attribute is set.</span></span>

<span data-ttu-id="a8058-121">Um einen vorhandenen Analyse Punkt zu überschreiben, ohne bereits über ein Handle für die Datei oder das Verzeichnis zu verfügen, müssen Sie [**die Datei mit**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) dem **Dateiflag zum Öffnen des Analyse \_ \_ \_ \_ Punkts** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a8058-121">To overwrite an existing reparse point without already having a handle to the file or directory, call [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) with **FILE\_FLAG\_OPEN\_REPARSE\_POINT**.</span></span> <span data-ttu-id="a8058-122">Mit diesem Flag können Sie die Datei öffnen, unabhängig davon, ob der entsprechende Dateisystem Filter installiert ist und ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="a8058-122">This flag allows you to open the file whether or not the corresponding file system filter is installed and working correctly.</span></span>

 

