---
description: Eine Anwendung kann das aktuelle Verzeichnis nach allen Dateinamen durchsuchen, die einem bestimmten Muster entsprechen, indem die Funktionen FindFirstFile, findfirstfileex, FindNextFile und FindClose verwendet werden.
ms.assetid: 7edd6c6e-7e8a-415c-866b-2283e5596a62
title: Suchen nach einer oder mehreren Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c5825b418221b1af429c6c0a731446d627701c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357396"
---
# <a name="searching-for-one-or-more-files"></a><span data-ttu-id="44068-103">Suchen nach einer oder mehreren Dateien</span><span class="sxs-lookup"><span data-stu-id="44068-103">Searching for One or More Files</span></span>

<span data-ttu-id="44068-104">Eine Anwendung kann das aktuelle Verzeichnis nach allen Dateinamen durchsuchen, die einem bestimmten Muster entsprechen, indem die Funktionen [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**findfirstfileex**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)und [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="44068-104">An application can search the current directory for all file names that match a given pattern by using the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea), and [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) functions.</span></span> <span data-ttu-id="44068-105">Das Muster muss ein gültiger Dateiname sein und darf Platzhalter Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="44068-105">The pattern must be a valid file name and can include wildcard characters.</span></span>

<span data-ttu-id="44068-106">Die Funktionen " [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) " und " [**findfirstfileex**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) " erstellen Handles, die von **findfirstfileex** verwendet werden, um nach anderen Dateien mit demselben Muster zu suchen.</span><span class="sxs-lookup"><span data-stu-id="44068-106">The [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) and [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) functions create handles that **FindFirstFileEx** uses to search for other files with the same pattern.</span></span> <span data-ttu-id="44068-107">Alle Funktionen geben Informationen über die gefundene Datei zurück.</span><span class="sxs-lookup"><span data-stu-id="44068-107">All functions return information about the file that was found.</span></span> <span data-ttu-id="44068-108">Zu diesen Informationen gehören der Dateiname, die Größe, die Attribute und die Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="44068-108">This information includes the file name, size, attributes, and time.</span></span>

<span data-ttu-id="44068-109">Die Funktion " [**findfirstfileex**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) " ermöglicht einer Anwendung auch das Suchen nach Dateien basierend auf zusätzlichen Suchkriterien.</span><span class="sxs-lookup"><span data-stu-id="44068-109">The [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) function also allows an application to search for files based on additional search criteria.</span></span> <span data-ttu-id="44068-110">Mit der-Funktion können Suchvorgänge auf Gerätenamen oder Verzeichnisnamen beschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="44068-110">The function can limit searches to device names or directory names.</span></span>

<span data-ttu-id="44068-111">Die [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) -Funktion zerstört Handles, die von " [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) " und " [**findfirstfileex**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)" erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="44068-111">The [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) function destroys handles created by [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) and [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa).</span></span>

<span data-ttu-id="44068-112">Eine Anwendung kann mithilfe der [**SearchPath**](/windows/win32/api/processenv/nf-processenv-searchpatha) -Funktion nach einer einzelnen Datei in einem bestimmten Pfad suchen.</span><span class="sxs-lookup"><span data-stu-id="44068-112">An application can search for a single file on a specific path by using the [**SearchPath**](/windows/win32/api/processenv/nf-processenv-searchpatha) function.</span></span>

 

 
