---
description: Eine Anwendung kann Verzeichnisse Programm gesteuert erstellen und löschen.
ms.assetid: 52d1d8a8-e5a7-44f5-9bf2-2a496ef79d32
title: Erstellen und Löschen von Verzeichnissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140547594271e13bc78bfa78336f167f228879a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130453"
---
# <a name="creating-and-deleting-directories"></a><span data-ttu-id="3f6ec-103">Erstellen und Löschen von Verzeichnissen</span><span class="sxs-lookup"><span data-stu-id="3f6ec-103">Creating and Deleting Directories</span></span>

<span data-ttu-id="3f6ec-104">Eine Anwendung kann Verzeichnisse Programm gesteuert erstellen und löschen.</span><span class="sxs-lookup"><span data-stu-id="3f6ec-104">An application can programmatically create and delete directories.</span></span>

<span data-ttu-id="3f6ec-105">Wenn Sie ein neues Verzeichnis erstellen möchten, verwenden Sie die Funktion " [**kreatedirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya)", " [**kreatedirectoryex**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa)" oder " [**kreatedirectorytransfailed**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda) ".</span><span class="sxs-lookup"><span data-stu-id="3f6ec-105">To create a new directory, use the [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya), [**CreateDirectoryEx**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa), or [**CreateDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda) function.</span></span> <span data-ttu-id="3f6ec-106">Ein Verzeichnis erhält den Namen, der beim Erstellen angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3f6ec-106">A directory is given the name specified when it is created.</span></span> <span data-ttu-id="3f6ec-107">Die Konventionen für die Benennung eines Verzeichnisses folgen den Konventionen zum Benennen einer Datei.</span><span class="sxs-lookup"><span data-stu-id="3f6ec-107">The conventions for naming a directory follow the conventions for naming a file.</span></span> <span data-ttu-id="3f6ec-108">Eine Beschreibung dieser Konventionen finden Sie unter [Benennen einer Datei](naming-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="3f6ec-108">For a description of these conventions, see [Naming a File](naming-a-file.md).</span></span>

<span data-ttu-id="3f6ec-109">Um ein vorhandenes Verzeichnis zu löschen, verwenden Sie die Funktion [**RemoveDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya) oder [**removedirectorytransktive**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda) .</span><span class="sxs-lookup"><span data-stu-id="3f6ec-109">To delete an existing directory, use the [**RemoveDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya) or [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda) function.</span></span> <span data-ttu-id="3f6ec-110">Bevor Sie ein Verzeichnis entfernen, müssen Sie sicherstellen, dass das Verzeichnis leer ist und dass Sie über die Berechtigung zum Löschen des Zugriffs für das Verzeichnis verfügen.</span><span class="sxs-lookup"><span data-stu-id="3f6ec-110">Before removing a directory, you must ensure that the directory is empty and that you have the delete access privilege for the directory.</span></span> <span data-ttu-id="3f6ec-111">Um Letzteres durchzuführen, müssen Sie die [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3f6ec-111">To do the latter, call the [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) function.</span></span>

 

 
