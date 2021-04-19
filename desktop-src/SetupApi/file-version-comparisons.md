---
description: Wenn \_ \_ während eines Datei Kopiervorgangs das Flag für neuere SP-Kopien angegeben wird, überprüfen die Setup Funktionen eine vorhandene Kopie der Datei im Zielverzeichnis.
ms.assetid: fd493b5d-7bab-4450-a749-745c536902dc
title: Datei Versions Vergleiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9601dcef07afca81a3ffc64148b0c4f2492f935
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363294"
---
# <a name="file-version-comparisons"></a><span data-ttu-id="b3fae-103">Datei Versions Vergleiche</span><span class="sxs-lookup"><span data-stu-id="b3fae-103">File Version Comparisons</span></span>

<span data-ttu-id="b3fae-104">Wenn \_ \_ während eines Datei Kopiervorgangs das Flag für neuere SP-Kopien angegeben wird, überprüfen die Setup Funktionen eine vorhandene Kopie der Datei im Zielverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="b3fae-104">If the SP\_COPY\_NEWER flag is specified during a file copy operation, the setup functions check for an existing copy of the file in the target directory.</span></span> <span data-ttu-id="b3fae-105">Wenn eine vorhandene Kopie gefunden wird, vergleichen die Funktionen die Versionen der Ziel-und Quelldatei, um zu bestimmen, welche neuer ist.</span><span class="sxs-lookup"><span data-stu-id="b3fae-105">If an existing copy is found, the functions compare the versions of the target and source file to determine which is newer.</span></span>

<span data-ttu-id="b3fae-106">Die Datei Versionsinformationen, die bei Versions Prüfungen verwendet werden, sind die, die in den Elementen **dwfileversionms** und **dwfileversionls** einer [**vs \_ FixedFileInfo**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) -Struktur angegeben sind, die von den Versionsfunktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b3fae-106">The file version information used during version checks is that specified in the **dwFileVersionMS** and **dwFileVersionLS** members of a [**VS\_FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) structure, used by the version functions.</span></span> <span data-ttu-id="b3fae-107">Wenn für eine der Dateien keine Versions Ressourcen angegeben sind oder die gleichen Versionsinformationen vorliegen, wird die Quelldatei als neuere Datei behandelt.</span><span class="sxs-lookup"><span data-stu-id="b3fae-107">If one of the files does not have version resources specified or if they have the same version information, the source file is treated as the newer file.</span></span>

 

 
