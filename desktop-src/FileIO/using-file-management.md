---
description: In den folgenden Beispielen werden die Dateiverwaltungsfunktionen verwendet.
ms.assetid: 0879898b-b661-48b3-af94-9ba24811503f
title: Verwenden der Dateiverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88838ee99dde16c5c2288c00e2e2f3b35747dae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050364"
---
# <a name="using-file-management"></a><span data-ttu-id="c49b3-103">Verwenden der Dateiverwaltung</span><span class="sxs-lookup"><span data-stu-id="c49b3-103">Using File Management</span></span>

<span data-ttu-id="c49b3-104">In den folgenden Beispielen werden die Dateiverwaltungsfunktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="c49b3-104">The following samples use the file management functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c49b3-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c49b3-105">In this section</span></span>



| <span data-ttu-id="c49b3-106">Thema</span><span class="sxs-lookup"><span data-stu-id="c49b3-106">Topic</span></span>                                                                                                   | <span data-ttu-id="c49b3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c49b3-107">Description</span></span>                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c49b3-108">Hinzufügen von Benutzern zu einer verschlüsselten Datei</span><span class="sxs-lookup"><span data-stu-id="c49b3-108">Adding Users to an Encrypted File</span></span>](adding-users-to-an-encrypted-file.md)<br/>                   | <span data-ttu-id="c49b3-109">Beispielcode, der zeigt, wie Sie einer vorhandenen verschlüsselten Datei mithilfe der Funktion " [**adduserstoverschlüsseltedfile**](/windows/desktop/api/Winefs/nf-winefs-adduserstoencryptedfile) " einen neuen Benutzer hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="c49b3-109">Example code that shows how to add a new user to an existing encrypted file by using the [**AddUsersToEncryptedFile**](/windows/desktop/api/Winefs/nf-winefs-adduserstoencryptedfile) function.</span></span><br/>                         |
| [<span data-ttu-id="c49b3-110">Anhängen einer Datei an eine andere Datei</span><span class="sxs-lookup"><span data-stu-id="c49b3-110">Appending One File to Another File</span></span>](appending-one-file-to-another-file.md)<br/>                 | <span data-ttu-id="c49b3-111">Beispielcode, der zeigt, wie eine Anwendung eine Datei am Ende einer anderen Datei anfügen kann, einschließlich der Vorgehensweise zum Öffnen und Schließen von Dateien, lesen und Schreiben in Dateien und Sperren und Entsperren von Dateien.</span><span class="sxs-lookup"><span data-stu-id="c49b3-111">Example code that shows how an application can append one file to the end of another file, including how to open and close files, read and write to files, and lock and unlock files.</span></span><br/> |
| [<span data-ttu-id="c49b3-112">Erstellen und Verwenden einer temporären Datei</span><span class="sxs-lookup"><span data-stu-id="c49b3-112">Creating and Using a Temporary File</span></span>](creating-and-using-a-temporary-file.md)<br/>               | <span data-ttu-id="c49b3-113">Beispielcode, der zeigt, wie eine temporäre Datei für Daten Bearbeitungs Zwecke mithilfe der Funktionen GetTempFileName und GetTempPath erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c49b3-113">Example code that shows how to create a temporary file for data manipulation purposes by using the GetTempFileName and GetTempPath functions.</span></span><br/>                                         |
| [<span data-ttu-id="c49b3-114">Sperren und Entsperren von Byte Bereichen in Dateien</span><span class="sxs-lookup"><span data-stu-id="c49b3-114">Locking and Unlocking Byte Ranges in Files</span></span>](locking-and-unlocking-byte-ranges-in-files.md)<br/> | <span data-ttu-id="c49b3-115">Beispielcode, der das Sperren und Entsperren von Byte Bereichen mithilfe der Funktionen "lockfileex" und "unlockfileex" anzeigt.</span><span class="sxs-lookup"><span data-stu-id="c49b3-115">Example code that shows byte range locking and unlocking by using the LockFileEx and UnlockFileEx functions.</span></span><br/>                                                                          |
| [<span data-ttu-id="c49b3-116">Öffnen einer Datei zum Lesen oder Schreiben</span><span class="sxs-lookup"><span data-stu-id="c49b3-116">Opening a File for Reading or Writing</span></span>](opening-a-file-for-reading-or-writing.md)<br/>           | <span data-ttu-id="c49b3-117">Beispielcode, der zeigt, wie Sie mit der Funktion "kreatefile" eine neue Datei erstellen oder eine vorhandene Datei öffnen.</span><span class="sxs-lookup"><span data-stu-id="c49b3-117">Example code that shows how to use the CreateFile function to create a new file or open an existing file.</span></span><br/>                                                                             |
| [<span data-ttu-id="c49b3-118">Abrufen und Ändern von Dateiattributen</span><span class="sxs-lookup"><span data-stu-id="c49b3-118">Retrieving and Changing File Attributes</span></span>](retrieving-and-changing-file-attributes.md)<br/>       | <span data-ttu-id="c49b3-119">Beispielcode, der zeigt, wie die Funktion getfileattributesex zum Abrufen von Dateiattributen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c49b3-119">Example code that shows how to use the GetFileAttributesEx function to retrieve file attributes.</span></span><br/>                                                                                      |
| [<span data-ttu-id="c49b3-120">Testen für das Ende einer Datei</span><span class="sxs-lookup"><span data-stu-id="c49b3-120">Testing for the End of a File</span></span>](testing-for-the-end-of-a-file.md)<br/>                           | <span data-ttu-id="c49b3-121">Beispielcode, der zeigt, wie das Dateiende während eines synchronen Lesevorgangs und während eines asynchronen Lesevorgangs getestet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c49b3-121">Example code that shows how to test for the end of file during a synchronous read operation and during an asynchronous read operation.</span></span><br/>                                                |
| [<span data-ttu-id="c49b3-122">Verwenden von Streams</span><span class="sxs-lookup"><span data-stu-id="c49b3-122">Using Streams</span></span>](using-streams.md)<br/>                                                           | <span data-ttu-id="c49b3-123">Beispielcode, der zeigt, wie grundlegende NTFS-Dateisystem Datenströme verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c49b3-123">Example code that shows how to use basic NTFS file system streams.</span></span><br/>                                                                                                                    |



 

 

 




