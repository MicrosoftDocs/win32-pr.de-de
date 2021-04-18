---
description: Eine symbolische Verknüpfung ist ein Dateisystem Objekt, das auf ein anderes Dateisystem Objekt zeigt. Das Objekt, auf das verwiesen wird, wird als Ziel bezeichnet.
ms.assetid: d6bf5df7-bc12-4dec-b116-95d9109f5eb4
title: Symbolische Links
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f051beb7de0280ba42df782264cef385f8d01a20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352260"
---
# <a name="symbolic-links"></a><span data-ttu-id="48d05-104">Symbolische Links</span><span class="sxs-lookup"><span data-stu-id="48d05-104">Symbolic Links</span></span>

<span data-ttu-id="48d05-105">Eine symbolische Verknüpfung ist ein Dateisystem Objekt, das auf ein anderes Dateisystem Objekt zeigt.</span><span class="sxs-lookup"><span data-stu-id="48d05-105">A symbolic link is a file-system object that points to another file system object.</span></span> <span data-ttu-id="48d05-106">Das Objekt, auf das verwiesen wird, wird als Ziel bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="48d05-106">The object being pointed to is called the target.</span></span>

<span data-ttu-id="48d05-107">Symbolische Verknüpfungen sind für Benutzer transparent. die Links werden als normale Dateien oder Verzeichnisse angezeigt und können vom Benutzer oder der Anwendung auf die gleiche Weise bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="48d05-107">Symbolic links are transparent to users; the links appear as normal files or directories, and can be acted upon by the user or application in exactly the same manner.</span></span>

<span data-ttu-id="48d05-108">Symbolische Verknüpfungen sollen die Migration und Anwendungskompatibilität mit UNIX-Betriebssystemen erleichtern.</span><span class="sxs-lookup"><span data-stu-id="48d05-108">Symbolic links are designed to aid in migration and application compatibility with UNIX operating systems.</span></span> <span data-ttu-id="48d05-109">Microsoft hat seine symbolischen Verknüpfungen so implementiert, dass Sie genau wie Unix-Links funktionieren.</span><span class="sxs-lookup"><span data-stu-id="48d05-109">Microsoft has implemented its symbolic links to function just like UNIX links.</span></span>

<span data-ttu-id="48d05-110">Weitere Informationen finden Sie in den nachfolgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="48d05-110">For more information, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="48d05-111">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="48d05-111">In this section</span></span>



| <span data-ttu-id="48d05-112">Thema</span><span class="sxs-lookup"><span data-stu-id="48d05-112">Topic</span></span>                                                                                                             | <span data-ttu-id="48d05-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48d05-113">Description</span></span>                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48d05-114">Symbolische Verknüpfungs Effekte in Dateisystemfunktionen</span><span class="sxs-lookup"><span data-stu-id="48d05-114">Symbolic Link Effects on File Systems Functions</span></span>](symbolic-link-effects-on-file-systems-functions.md)<br/> | <span data-ttu-id="48d05-115">Funktionsweise von symbolischen Verknüpfungen auf Standarddatei Funktionen, die Pfadnamen verwenden, um eine oder mehrere Dateien anzugeben.</span><span class="sxs-lookup"><span data-stu-id="48d05-115">How symbolic links affect standard file functions that use path names to specify one or more files.</span></span><br/>                                        |
| [<span data-ttu-id="48d05-116">Überlegungen zur Programmierung</span><span class="sxs-lookup"><span data-stu-id="48d05-116">Programming Considerations</span></span>](symbolic-link-programming-considerations.md)<br/>                             | <span data-ttu-id="48d05-117">Programmier Überlegungen für die Arbeit mit symbolischen Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="48d05-117">Programming considerations for working with symbolic links.</span></span><br/>                                                                                |
| [<span data-ttu-id="48d05-118">Erstellen von symbolischen Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="48d05-118">Creating Symbolic Links</span></span>](creating-symbolic-links.md)<br/>                                                 | <span data-ttu-id="48d05-119">Erstellen Sie symbolische Verknüpfungen, die einen absoluten oder relativen Pfad verwenden, indem Sie die Funktion " [**kreatesymboliclink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) " verwenden.</span><span class="sxs-lookup"><span data-stu-id="48d05-119">Create symbolic links that use either an absolute or relative path by using the [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) function.</span></span><br/> |



 

## <a name="supported-operating-systems"></a><span data-ttu-id="48d05-120">Unterstützte Betriebssysteme</span><span class="sxs-lookup"><span data-stu-id="48d05-120">Supported Operating Systems</span></span>

<span data-ttu-id="48d05-121">Symbolische Verknüpfungen stehen in NTFS ab Windows Vista zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="48d05-121">Symbolic links are available in NTFS starting with Windows Vista.</span></span>

 

 




