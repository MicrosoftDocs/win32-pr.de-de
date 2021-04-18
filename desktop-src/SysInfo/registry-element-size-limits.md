---
description: In der folgenden Tabelle sind die Größenbeschränkungen für die verschiedenen Registrierungs Elemente aufgeführt.
ms.assetid: a6d3a884-f181-46a5-b655-226c68792e08
title: Größenbeschränkungen für das Registrierungs Element
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 262609a64e60536dcfc41f29e5d94ea499158861
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358520"
---
# <a name="registry-element-size-limits"></a><span data-ttu-id="60a7a-103">Größenbeschränkungen für das Registrierungs Element</span><span class="sxs-lookup"><span data-stu-id="60a7a-103">Registry Element Size Limits</span></span>

<span data-ttu-id="60a7a-104">In der folgenden Tabelle sind die Größenbeschränkungen für die verschiedenen Registrierungs Elemente aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="60a7a-104">The following table identifies the size limits for the various registry elements.</span></span>



| <span data-ttu-id="60a7a-105">Registry-Element</span><span class="sxs-lookup"><span data-stu-id="60a7a-105">Registry Element</span></span> | <span data-ttu-id="60a7a-106">Größenlimit</span><span class="sxs-lookup"><span data-stu-id="60a7a-106">Size Limit</span></span>                                                                                                                                            |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60a7a-107">Schlüsselname</span><span class="sxs-lookup"><span data-stu-id="60a7a-107">Key name</span></span>         | <span data-ttu-id="60a7a-108">255 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="60a7a-108">255 characters.</span></span> <span data-ttu-id="60a7a-109">Der Schlüssel Name enthält den absoluten Pfad des Schlüssels in der Registrierung, der immer mit einem Basis Schlüssel beginnt, z. b. HKEY \_ local \_ Machine.</span><span class="sxs-lookup"><span data-stu-id="60a7a-109">The key name includes the absolute path of the key in the registry, always starting at a base key, for example, HKEY\_LOCAL\_MACHINE.</span></span> |
| <span data-ttu-id="60a7a-110">Wertname</span><span class="sxs-lookup"><span data-stu-id="60a7a-110">Value name</span></span>       | <span data-ttu-id="60a7a-111">16.383 Zeichen **Windows 2000:** 260 ANSI-Zeichen oder 16.383 Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="60a7a-111">16,383 characters **Windows 2000:** 260 ANSI characters or 16,383 Unicode characters.</span></span><br/>                                                       |
| <span data-ttu-id="60a7a-112">Wert</span><span class="sxs-lookup"><span data-stu-id="60a7a-112">Value</span></span>            | <span data-ttu-id="60a7a-113">Verfügbarer Arbeitsspeicher (Aktuelles Format) 1 MB (Standardformat)</span><span class="sxs-lookup"><span data-stu-id="60a7a-113">Available memory (latest format)1 MB (standard format)</span></span><br/>                                                                                     |
| <span data-ttu-id="60a7a-114">Struktur</span><span class="sxs-lookup"><span data-stu-id="60a7a-114">Tree</span></span>             | <span data-ttu-id="60a7a-115">Eine Registrierungs Struktur kann 512 Ebenen tief sein.</span><span class="sxs-lookup"><span data-stu-id="60a7a-115">A registry tree can be 512 levels deep.</span></span> <span data-ttu-id="60a7a-116">Sie können bis zu 32 Ebenen gleichzeitig über einen einzigen Registrierungs-API-Aufruf erstellen.</span><span class="sxs-lookup"><span data-stu-id="60a7a-116">You can create up to 32 levels at a time through a single registry API call.</span></span>                                  |



 

<span data-ttu-id="60a7a-117">Lange Werte (mehr als 2.048 bytes) sollten in einer Datei gespeichert werden, und der Speicherort der Datei sollte in der Registrierung gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="60a7a-117">Long values (more than 2,048 bytes) should be stored in a file, and the location of the file should be stored in the registry.</span></span> <span data-ttu-id="60a7a-118">Dadurch kann die Registrierung effizient durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="60a7a-118">This helps the registry perform efficiently.</span></span>

<span data-ttu-id="60a7a-119">Der Speicherort der Datei kann der Name eines Werts oder die Daten eines Werts sein.</span><span class="sxs-lookup"><span data-stu-id="60a7a-119">The file location can be the name of a value or the data of a value.</span></span> <span data-ttu-id="60a7a-120">Jedem umgekehrten Schrägstrich in der Zeichenfolge muss ein anderer umgekehrter Schrägstrich als Escapezeichen vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="60a7a-120">Each backslash in the location string must be preceded by another backslash as an escape character.</span></span> <span data-ttu-id="60a7a-121">Geben Sie z. b. "c: \\ \\ " MyDir " \\ \\ MyFile" an, um die Zeichenfolge "c: \\ " MyDir " \\ MyFile" zu speichern.</span><span class="sxs-lookup"><span data-stu-id="60a7a-121">For example, specify "C:\\\\mydir\\\\myfile" to store the string "C:\\mydir\\myfile".</span></span> <span data-ttu-id="60a7a-122">Bei einem Datei Speicherort kann es sich auch um den Namen eines Schlüssels handeln, wenn er sich innerhalb der 255-Zeichen Beschränkung für Schlüsselnamen befindet und keine umgekehrten Schrägstriche enthält, die in Schlüsselnamen nicht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="60a7a-122">A file location can also be the name of a key if it is within the 255-character limit for key names and does not contain backslashes, which are not allowed in key names.</span></span>

 

 




