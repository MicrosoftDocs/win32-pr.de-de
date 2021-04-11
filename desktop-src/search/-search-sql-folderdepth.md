---
description: Ordner Tiefe-Prädikate steuern den Bereich einer Suche, indem Sie einen Pfad angeben und angeben, ob eine Tiefe oder eine flache Durchquerung durchlaufen werden soll.
ms.assetid: 8eadbd42-3538-412e-9bf8-b2355d23437e
title: Bereichs-und Verzeichnis Prädikate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2418b2149a5bf05bd000460c787b7f967856c5c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128548"
---
# <a name="scope-and-directory-predicates"></a><span data-ttu-id="bc122-103">Bereichs-und Verzeichnis Prädikate</span><span class="sxs-lookup"><span data-stu-id="bc122-103">SCOPE and DIRECTORY Predicates</span></span>

<span data-ttu-id="bc122-104">Ordner Tiefe-Prädikate steuern den Bereich einer Suche, indem Sie einen Pfad angeben und angeben, ob eine Tiefe oder eine flache Durchquerung durchlaufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="bc122-104">Folder depth predicates control the scope of a search by specifying a path and whether to perform a deep or shallow traversal.</span></span> <span data-ttu-id="bc122-105">Das folgende Beispiel zeigt die Syntax der Ordner Tiefe-Prädikate:</span><span class="sxs-lookup"><span data-stu-id="bc122-105">The following shows the syntax of the folder depth predicates:</span></span>


```
... WHERE [{SCOPE | DIRECTORY}='<protocol>:[{SID}]<path>']
```



<span data-ttu-id="bc122-106">Auf das Prädikat folgt ein Gleichheitszeichen.</span><span class="sxs-lookup"><span data-stu-id="bc122-106">The predicate is followed by an equal sign.</span></span> <span data-ttu-id="bc122-107">Der Pfad wird in einfache Anführungszeichen eingeschlossen und muss mit einem Protokoll und einem Doppelpunkt beginnen (z `file:` . b `mapi:` ., oder `csc:` ).</span><span class="sxs-lookup"><span data-stu-id="bc122-107">The path is exclosed in single quotes and must begin with a protocol and a colon (for example, `file:`, `mapi:`, or `csc:`).</span></span> <span data-ttu-id="bc122-108">Das Bereichs Prädikat führt einen tiefen Durchlauf des Pfads aus, einschließlich aller Unterordner, während das Verzeichnis Prädikat nur einen flachen Durchlauf des angegebenen Ordners ausführt.</span><span class="sxs-lookup"><span data-stu-id="bc122-108">The SCOPE predicate performs a deep traversal of the path, including all subfolders, while the DIRECTORY predicate does a shallow traversal of only the folder specified.</span></span> <span data-ttu-id="bc122-109">Wie andere Structured Query Language (SQL)-Einschränkungen können Sie mehr als eine Ordner tiefen Einschränkung in einer einzelnen Abfrage angeben.</span><span class="sxs-lookup"><span data-stu-id="bc122-109">Like other Structured Query Language (SQL) restrictions, you can specify more than one folder depth restriction in a single query.</span></span>

<span data-ttu-id="bc122-110">Um den lokalen Katalog eines Remote Computers abzufragen, müssen Sie den Computernamen vor dem Katalog und einen Universal Naming Convention (UNC)-Pfad auf dem Remote Computer in der Scope-oder Directory-Klausel einschließen.</span><span class="sxs-lookup"><span data-stu-id="bc122-110">To query the local catalog of a remote computer, include the computer name before the catalog and a Universal Naming Convention (UNC) path on the remote computer in the SCOPE or DIRECTORY clause.</span></span>

## <a name="examples"></a><span data-ttu-id="bc122-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bc122-111">Examples</span></span>


```
SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Reports'

SELECT System.ItemName FROM SystemIndex WHERE DIRECTORY='file:C:/Files/Reports' 

SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Published' OR SCOPE='file:C:/Files/Reports' AND NOT SCOPE='file:C:/Files/Reports/Confidential'

SELECT System.ItemName FROM zarasmachine.SystemIndex WHERE SCOPE='file://zarasmachine/C:/Files/Reports'

SELECT System.ItemURL FROM SystemIndex WHERE SCOPE='mapi://{S-1-5-21-2117521111-1604012920-1887927527-2285604}/Mailbox user/' AND CONTAINS('Microsoft')
```



<span data-ttu-id="bc122-112">Im ersten Bereichs Beispiel wird der Ordner "C: \\ Dateien \\ Berichte" und alle zugehörigen Unterordner durchsucht.</span><span class="sxs-lookup"><span data-stu-id="bc122-112">The first SCOPE example searches the C:\\Files\\Reports folder and all its subfolders.</span></span> <span data-ttu-id="bc122-113">Im Verzeichnis Beispiel werden nur der Stamm Ordner C: \\ Files-Berichte durchsucht \\ .</span><span class="sxs-lookup"><span data-stu-id="bc122-113">The DIRECTORY example searches only the root folder C:\\Files\\Reports.</span></span>

> [!Note]  
> <span data-ttu-id="bc122-114">Die umgekehrten Schrägstriche () des Dateisystems \\ werden zu einem URL-Schrägstrich (manchmal auch als Schrägstriche bezeichnet) (/).</span><span class="sxs-lookup"><span data-stu-id="bc122-114">The file system backslashes (\\) become a URL-style slash marks (sometimes called forward slashes) (/).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="bc122-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bc122-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="bc122-116">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="bc122-116">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bc122-117">FROM-Klausel</span><span class="sxs-lookup"><span data-stu-id="bc122-117">FROM Clause</span></span>](-search-sql-from.md)
</dt> <dt>

[<span data-ttu-id="bc122-118">WHERE-Klausel</span><span class="sxs-lookup"><span data-stu-id="bc122-118">WHERE Clause</span></span>](-search-sql-where.md)
</dt> </dl>

 

 



