---
description: Wenn ein Prozess ein Verzeichnis Objekt erstellt oder öffnet, empfängt es ein Handle für das Objekt.
ms.assetid: 841c7daa-360c-4d96-8a14-6dcfa159a875
title: Verzeichnis Handles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4215a75622a7fa35ee36d45e769736bf1224a66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366301"
---
# <a name="directory-handles"></a><span data-ttu-id="796a8-103">Verzeichnis Handles</span><span class="sxs-lookup"><span data-stu-id="796a8-103">Directory Handles</span></span>

<span data-ttu-id="796a8-104">Wenn ein Prozess ein Verzeichnis Objekt erstellt oder öffnet, empfängt es ein Handle für das Objekt.</span><span class="sxs-lookup"><span data-stu-id="796a8-104">Whenever a process creates or opens a directory object, it receives a handle to the object.</span></span>

<span data-ttu-id="796a8-105">Um ein Handle für ein vorhandenes Verzeichnis zu erhalten, rufen Sie [**die Funktion "**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) Funktion" mit dem **Dateiflag für die \_ \_ Sicherungs \_ Semantik** auf.</span><span class="sxs-lookup"><span data-stu-id="796a8-105">To obtain a handle to an existing directory, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function with the **FILE\_FLAG\_BACKUP\_SEMANTICS** flag.</span></span>

<span data-ttu-id="796a8-106">Sie können ein Verzeichnis Handle an die folgenden Funktionen übergeben.</span><span class="sxs-lookup"><span data-stu-id="796a8-106">You can pass a directory handle to the following functions.</span></span>



| <span data-ttu-id="796a8-107">Funktion</span><span class="sxs-lookup"><span data-stu-id="796a8-107">Function</span></span>                                                         | <span data-ttu-id="796a8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="796a8-108">Description</span></span>                                                                                                                                                      |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="796a8-109">**BackupRead**</span><span class="sxs-lookup"><span data-stu-id="796a8-109">**BackupRead**</span></span>](/windows/desktop/api/winbase/nf-winbase-backupread)                              | <span data-ttu-id="796a8-110">Sichern Sie eine Datei oder ein Verzeichnis, einschließlich der Sicherheitsinformationen.</span><span class="sxs-lookup"><span data-stu-id="796a8-110">Back up a file or directory, including the security information.</span></span><br/>                                                                                      |
| [<span data-ttu-id="796a8-111">**BackupSeek**</span><span class="sxs-lookup"><span data-stu-id="796a8-111">**BackupSeek**</span></span>](/windows/desktop/api/winbase/nf-winbase-backupseek)                              | <span data-ttu-id="796a8-112">Forward-Forward in einem Datenstrom, auf den zunächst mithilfe der [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread) -Funktion oder der [**Backup Write**](/windows/desktop/api/winbase/nf-winbase-backupwrite) -Funktion zugegriffen wurde.</span><span class="sxs-lookup"><span data-stu-id="796a8-112">Seeks forward in a data stream initially accessed by using the [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread) or [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite) function.</span></span><br/> |
| [<span data-ttu-id="796a8-113">**BackupWrite**</span><span class="sxs-lookup"><span data-stu-id="796a8-113">**BackupWrite**</span></span>](/windows/desktop/api/winbase/nf-winbase-backupwrite)                            | <span data-ttu-id="796a8-114">Stellen Sie eine mit [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread)gesicherte Datei oder ein Verzeichnis wieder her.</span><span class="sxs-lookup"><span data-stu-id="796a8-114">Restore a file or directory that was backed up using [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread).</span></span><br/>                                                             |
| [<span data-ttu-id="796a8-115">**Getfileingeformationbyhandle**</span><span class="sxs-lookup"><span data-stu-id="796a8-115">**GetFileInformationByHandle**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle) | <span data-ttu-id="796a8-116">Ruft Dateiinformationen für die angegebene Datei ab.</span><span class="sxs-lookup"><span data-stu-id="796a8-116">Retrieves file information for the specified file.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="796a8-117">**GetFileSize**</span><span class="sxs-lookup"><span data-stu-id="796a8-117">**GetFileSize**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize)                               | <span data-ttu-id="796a8-118">Ruft die Größe der angegebenen Datei in Bytes ab.</span><span class="sxs-lookup"><span data-stu-id="796a8-118">Retrieves the size of the specified file, in bytes.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="796a8-119">**' GetFileTime '**</span><span class="sxs-lookup"><span data-stu-id="796a8-119">**GetFileTime**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | <span data-ttu-id="796a8-120">Ruft das Datum und die Uhrzeit der Erstellung einer Datei oder eines Verzeichnisses, des letzten Zugriffs und der letzten Änderung ab.</span><span class="sxs-lookup"><span data-stu-id="796a8-120">Retrieves the date and time that a file or directory was created, last accessed, and last modified.</span></span><br/>                                                   |
| [<span data-ttu-id="796a8-121">**Getfiletype**</span><span class="sxs-lookup"><span data-stu-id="796a8-121">**GetFileType**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfiletype)                               | <span data-ttu-id="796a8-122">Ruft den Dateityp der angegebenen Datei ab.</span><span class="sxs-lookup"><span data-stu-id="796a8-122">Retrieves the file type of the specified file.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="796a8-123">**"Read directoriychangesw"**</span><span class="sxs-lookup"><span data-stu-id="796a8-123">**ReadDirectoryChangesW**</span></span>](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)           | <span data-ttu-id="796a8-124">Ruft Informationen ab, die die Änderungen im angegebenen Verzeichnis beschreiben.</span><span class="sxs-lookup"><span data-stu-id="796a8-124">Retrieves information that describes the changes within the specified directory.</span></span><br/>                                                                      |
| [<span data-ttu-id="796a8-125">**SetFileTime**</span><span class="sxs-lookup"><span data-stu-id="796a8-125">**SetFileTime**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | <span data-ttu-id="796a8-126">Legt das Datum und die Uhrzeit fest, zu der die angegebene Datei bzw. das angegebene Verzeichnis erstellt, auf den zuletzt zugegriffen wurde, oder zuletzt geändert</span><span class="sxs-lookup"><span data-stu-id="796a8-126">Sets the date and time that the specified file or directory was created, last accessed, or last modified.</span></span><br/>                                             |



 

 

