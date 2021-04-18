---
description: Mit Windows 7 werden Bibliotheken eingeführt, die Benutzern eine einheitliche Ansicht Ihrer Dateien bereitstellen, auch wenn diese Dateien an unterschiedlichen Speicherorten gespeichert werden.
title: Windows-Bibliotheken
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 19DA68B2-FCB6-443d-A3CD-0BF2F429B149
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ddb21b4678005d3def5812258a75f2e4fec4b9f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980936"
---
# <a name="windows-libraries"></a><span data-ttu-id="c0650-103">Windows-Bibliotheken</span><span class="sxs-lookup"><span data-stu-id="c0650-103">Windows Libraries</span></span>

<span data-ttu-id="c0650-104">Mit Windows 7 werden Bibliotheken eingeführt, die Benutzern eine einheitliche Ansicht Ihrer Dateien bereitstellen, auch wenn diese Dateien an unterschiedlichen Speicherorten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="c0650-104">Windows 7 introduces libraries, which provide users with a single, coherent view of their files even when those files are stored in different locations.</span></span> <span data-ttu-id="c0650-105">Bibliotheken können von einem Benutzer konfiguriert und organisiert werden, und eine Bibliothek kann Ordner enthalten, die sich auf dem Computer des Benutzers und auch Ordner befinden, die über ein Netzwerk freigegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="c0650-105">Libraries can be configured and organized by a user and a library can contain folders that are found on the user's computer and also folders that have been shared over a network.</span></span> <span data-ttu-id="c0650-106">Bibliotheken stellen eine einfachere Ansicht des zugrunde liegenden Speichersystems dar, denn für den Benutzer werden die Dateien und Ordner in einer Bibliothek in der einzelnen Ansicht angezeigt, unabhängig davon, wo Sie physisch gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="c0650-106">Libraries present a simpler view of the underlying storage system because, to the user, the files and folders in a library are displayed in single view, no matter where they are physically stored.</span></span>

<span data-ttu-id="c0650-107">Entwickler, die neue Programme in Windows 7 schreiben, werden empfohlen, Bibliotheken als Mittel zu verwenden, mit denen die Benutzer mit den Dateien interagieren, die vom Programm verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c0650-107">Developers writing new programs in Windows 7 are encouraged to use libraries as the means through which the users interact with the files used by the program.</span></span> <span data-ttu-id="c0650-108">Die Verwendung von Bibliotheken in Ihrem Programm bietet Benutzern eine saubere, einfachere und einheitlichere Benutzerfreundlichkeit in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c0650-108">Using libraries in your program will provide users with a cleaner, easier, and more consistent experience in Windows 7.</span></span>

<span data-ttu-id="c0650-109">Entwickler sollten auch Ihre vorhandenen Programme überprüfen und ggf. aktualisieren, um mit Bibliotheken zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="c0650-109">Developers should also review their existing programs, and update them if necessary, to work with libraries.</span></span> <span data-ttu-id="c0650-110">Da Bibliotheken nicht Teil des Dateisystems sind, haben Dateisystem basierte APIs keinen Zugriff auf Bibliotheken, die der Benutzer möglicherweise konfiguriert hat.</span><span class="sxs-lookup"><span data-stu-id="c0650-110">Because libraries are not a part of the file system, file system-based APIs will not have access to any libraries that the user might have configured.</span></span>

<span data-ttu-id="c0650-111">Programme, die derzeit zulassen, dass Benutzer ihre Inhalte in anderen Ordnern oder auf unterschiedlichen Computern speichern, werden am meisten davon profitieren, wenn Sie Bibliotheks Unterstützung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c0650-111">Programs that currently allow users to store their content in different folders or on different computers will benefit most when they add library support.</span></span> <span data-ttu-id="c0650-112">Bibliotheken vereinfachen die Verwaltung von Inhalten an verschiedenen Speicherorten für den Entwickler und den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="c0650-112">Libraries simplify the management of content in diverse storage locations for the developer and the user.</span></span>

<span data-ttu-id="c0650-113">In dieser Anleitung wird beschrieben, was Bibliotheken sind, wie Programme zum Arbeiten mit Bibliotheken erstellt werden können und wie ein Programmbibliotheken verwenden kann, um die Benutzeroberflächen zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="c0650-113">This guide describes more about what libraries are, how programs can be made to work with libraries, and some of the ways a program can use libraries to improve the user's experience.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0650-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c0650-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0650-115">Informationen zu Bibliotheken</span><span class="sxs-lookup"><span data-stu-id="c0650-115">About Libraries</span></span>](library-leverage-to-manage-folders.md)
</dt> <dt>

[<span data-ttu-id="c0650-116">Verwenden von Bibliotheken in Ihrem Programm</span><span class="sxs-lookup"><span data-stu-id="c0650-116">Using Libraries in your Program</span></span>](library-be-library-aware.md)
</dt> <dt>

[<span data-ttu-id="c0650-117">**Ishelllibrary**</span><span class="sxs-lookup"><span data-stu-id="c0650-117">**IShellLibrary**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[<span data-ttu-id="c0650-118">Shelllinks</span><span class="sxs-lookup"><span data-stu-id="c0650-118">Shell Links</span></span>](./links.md)
</dt> <dt>

[<span data-ttu-id="c0650-119">Bekannte Ordner</span><span class="sxs-lookup"><span data-stu-id="c0650-119">Known Folders</span></span>](known-folders.md)
</dt> <dt>

[<span data-ttu-id="c0650-120">Bibliotheks Beschreibungs Schema</span><span class="sxs-lookup"><span data-stu-id="c0650-120">Library Description Schema</span></span>](library-schema-entry.md)
</dt> </dl>

 

 
