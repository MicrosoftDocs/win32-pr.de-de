---
description: Funktionen, die verwendet werden, um Dateiinformationen zu erhalten und festzulegen.
ms.assetid: 3b5fb709-c699-4651-8072-97210c8cf763
title: Abrufen und Festlegen von Dateiinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c6eb6abf2554e1945e0782c667245ea0eaa99be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868912"
---
# <a name="obtaining-and-setting-file-information"></a><span data-ttu-id="90d35-103">Abrufen und Festlegen von Dateiinformationen</span><span class="sxs-lookup"><span data-stu-id="90d35-103">Obtaining and Setting File Information</span></span>

<span data-ttu-id="90d35-104">In den folgenden Themen wird beschrieben, wie Sie Dateiinformationen erhalten und festlegen.</span><span class="sxs-lookup"><span data-stu-id="90d35-104">The following topics describe how to get and set file information.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="90d35-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="90d35-105">In this section</span></span>



| <span data-ttu-id="90d35-106">Thema</span><span class="sxs-lookup"><span data-stu-id="90d35-106">Topic</span></span>                                                                                                             | <span data-ttu-id="90d35-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="90d35-107">Description</span></span>                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90d35-108">Abrufen von Dateityp Informationen</span><span class="sxs-lookup"><span data-stu-id="90d35-108">Retrieving File Type Information</span></span>](retrieving-file-type-information.md)<br/>                               | <span data-ttu-id="90d35-109">Die [**getfiletype**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletype) -Funktion Ruft den Dateityp ab: Datenträger, Zeichen (z. b. eine Konsole), Pipe oder unbekannt.</span><span class="sxs-lookup"><span data-stu-id="90d35-109">The [**GetFileType**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletype) function retrieves the type of a file: disk, character (such as a console), pipe, or unknown.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="90d35-110">Bestimmen der Größe einer Datei</span><span class="sxs-lookup"><span data-stu-id="90d35-110">Determining the Size of a File</span></span>](determining-the-size-of-a-file.md)<br/>                                   | <span data-ttu-id="90d35-111">Die [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) -Funktion Ruft die Größe einer Datei ab.</span><span class="sxs-lookup"><span data-stu-id="90d35-111">The [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) function retrieves the size of a file.</span></span><br/>                                                                                                                                                                                                      |
| [<span data-ttu-id="90d35-112">Suchen nach einer oder mehreren Dateien</span><span class="sxs-lookup"><span data-stu-id="90d35-112">Searching for One or More Files</span></span>](searching-for-one-or-more-files.md)<br/>                                 | <span data-ttu-id="90d35-113">Eine Anwendung kann das aktuelle Verzeichnis nach allen Dateinamen durchsuchen, die einem bestimmten Muster entsprechen, indem die Funktionen [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**findfirstfileex**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)und [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="90d35-113">An application can search the current directory for all file names that match a given pattern by using the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea), and [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) functions.</span></span><br/> |
| [<span data-ttu-id="90d35-114">Festlegen und erhalten des Zeitstempels einer Datei</span><span class="sxs-lookup"><span data-stu-id="90d35-114">Setting and Getting the Timestamp of a File</span></span>](setting-and-getting-the-timestamp-of-a-file.md)<br/>         | <span data-ttu-id="90d35-115">Anwendungen können das Datum und die Uhrzeit der Erstellung, letzten Änderung oder des letzten Zugriffs auf eine Datei mithilfe der Funktionen [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) und [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) abrufen und festlegen.</span><span class="sxs-lookup"><span data-stu-id="90d35-115">Applications can retrieve and set the date and time a file is created, last modified, or last accessed by using the [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) and [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) functions.</span></span><br/>                                                                         |
| [<span data-ttu-id="90d35-116">Festlegen der Codepage für den aktuellen Zeichensatz</span><span class="sxs-lookup"><span data-stu-id="90d35-116">Determining the Current Character Set Code Page</span></span>](determining-the-current-character-set-code-page.md)<br/> | <span data-ttu-id="90d35-117">Die [**arefileapisansi**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) -Funktion bestimmt, ob die Datei-e/a-Funktionen die ANSI-oder OEM-Zeichensatz-Codepage verwenden.</span><span class="sxs-lookup"><span data-stu-id="90d35-117">The [**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) function determines whether the file I/O functions are using the ANSI or OEM character set code page.</span></span><br/>                                                                                                                               |



 

 

