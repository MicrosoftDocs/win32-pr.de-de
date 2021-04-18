---
description: Erstellt eine nicht signierte Katalog Datei, in der die Hashwerte eines Satzes von Dateien zusammen mit zugeordneten Attributen der einzelnen Dateien im Satz enthalten sind. Eine Katalog Datei ermöglicht dem Benutzer, eine Datei (den Katalog) zu signieren, anstatt zahlreiche einzelne Dateien zu signieren.
ms.assetid: 0a6ce2cd-db1f-4b47-990c-36fa87c28a60
title: Verwenden von MakeCat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e36c83531df38b95bde03edd719d98be325dbeac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345180"
---
# <a name="using-makecat"></a><span data-ttu-id="836f0-104">Verwenden von MakeCat</span><span class="sxs-lookup"><span data-stu-id="836f0-104">Using MakeCat</span></span>

<span data-ttu-id="836f0-105">Das [MakeCat](makecat.md) -Tool erstellt eine nicht signierte Katalog Datei, die [*die Hashwerte eines Satzes*](../secgloss/h-gly.md) von Dateien zusammen mit zugeordneten Attributen der einzelnen Dateien in der Gruppe enthält.</span><span class="sxs-lookup"><span data-stu-id="836f0-105">The [MakeCat](makecat.md) tool makes an unsigned catalog file, which contains the [*hashes*](../secgloss/h-gly.md) of a set of files along with associated attributes of each file in the set.</span></span> <span data-ttu-id="836f0-106">Eine Katalog Datei ermöglicht dem Benutzer, eine Datei (den Katalog) zu signieren, anstatt zahlreiche einzelne Dateien zu signieren.</span><span class="sxs-lookup"><span data-stu-id="836f0-106">A catalog file allows the user to sign one file (the catalog) instead of signing numerous individual files.</span></span>

<span data-ttu-id="836f0-107">Nachdem die nicht signierte Katalog Datei signiert und übertragen wurde, kann der Empfänger die Hashwerte der ursprünglichen Dateien mit den Hashes in der Katalog Datei vergleichen und sicherstellen, dass die Dateien nicht manipuliert sind.</span><span class="sxs-lookup"><span data-stu-id="836f0-107">After the unsigned catalog file is signed and transmitted, the receiver can compare the hashes of the original files to the hashes contained within the catalog file and verify that the files are free of tampering.</span></span>

<span data-ttu-id="836f0-108">Vor der Verwendung des [MakeCat](makecat.md) -Tools muss der Benutzer eine Katalog Definitionsdatei (. CDF) mithilfe eines beliebigen Text-Editors vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="836f0-108">Prior to using the [MakeCat](makecat.md) tool, the user must prepare a Catalog Definition File (.cdf), by using any text editor.</span></span> <span data-ttu-id="836f0-109">Die CDF-Datei enthält die Liste der Dateien und die Attribute der zu katalogigenden Dateien (die Spezifikationen sind unten aufgeführt).</span><span class="sxs-lookup"><span data-stu-id="836f0-109">The .cdf file contains the list of files and the attributes of the files to be cataloged (the specifications are listed below).</span></span> <span data-ttu-id="836f0-110">Das MakeCat-Tool scannt die CDF-Datei, überprüft die Liste der Attribute der einzelnen aufgelisteten Dateien, fügt die aufgelisteten Attribute dem Katalog selbst hinzu, erstellt Hashwerte für jede der aufgelisteten Dateien und speichert die Hashes der einzelnen Dateien in der Katalog Datei.</span><span class="sxs-lookup"><span data-stu-id="836f0-110">The MakeCat tool scans the .cdf file, verifies the list of attributes of each listed file, adds the listed attributes to the catalog itself, hashes each of the listed files, and stores the hashes of each file into the catalog file.</span></span> <span data-ttu-id="836f0-111">Jede Datei enthält den Hash und die Attribute, die separat im Katalog gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="836f0-111">Each file has its hash and attributes stored separately within the catalog.</span></span> <span data-ttu-id="836f0-112">Diese Katalog Datei kann dann signiert und übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="836f0-112">This catalog file can then be signed and transmitted.</span></span> <span data-ttu-id="836f0-113">Der Empfänger kann anschließend den Hash der einzelnen Dateien im Katalog mit dem Hash der ursprünglichen Dateien vergleichen, um zu beweisen, dass der ursprüngliche Inhalt nicht manipuliert werden kann.</span><span class="sxs-lookup"><span data-stu-id="836f0-113">The receiver can subsequently compare the hash of each file within the catalog with the hash of the original files to prove that the original content is free of tampering.</span></span> <span data-ttu-id="836f0-114">MakeCat ändert die CDF-Datei nicht.</span><span class="sxs-lookup"><span data-stu-id="836f0-114">MakeCat does not modify the .cdf file.</span></span>

<span data-ttu-id="836f0-115">In den folgenden Beispielen werden [MakeCat](makecat.md) -Befehle verwendet.</span><span class="sxs-lookup"><span data-stu-id="836f0-115">The following examples use [MakeCat](makecat.md) commands.</span></span>

-   <span data-ttu-id="836f0-116">Generieren Sie eine Katalog Datei aus der Datei Good. CDF.</span><span class="sxs-lookup"><span data-stu-id="836f0-116">Generate a catalog file from the file Good.cdf.</span></span>

    <span data-ttu-id="836f0-117">**MakeCat-v Good. CDF**</span><span class="sxs-lookup"><span data-stu-id="836f0-117">**MakeCat -v good.cdf**</span></span>

<span data-ttu-id="836f0-118">Eine Datei, "Good. CDF", erzeugt eine Katalog Datei (Good.cat), indem Sie die Dateien UnsignedPE.exe, UnsignedDOS.exe, Unsigned.cab, unsigned. Class und SignedPE.exe.</span><span class="sxs-lookup"><span data-stu-id="836f0-118">A file, Good.cdf, produces a catalog file, Good.cat, by parsing the files UnsignedPE.exe, UnsignedDOS.exe, Unsigned.cab, Unsigned.Class, and SignedPE.exe.</span></span> <span data-ttu-id="836f0-119">Die analysierten Dateien, zusammen mit "Good. CDF" und der neu generierten Good.cat, befinden sich alle im selben Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="836f0-119">The parsed files, along with Good.cdf and the newly generated Good.cat, are all in the same directory.</span></span>

``` syntax
[CatalogHeader]
Name=Good.cat
ResultDir=.\
PublicVersion=0x00000001
EncodingType=
CATATTR1=0x10010001:Movie1:FirstMovie
CATATTR2=0x10010001:Movie2:SecondMovie
CATATTR3=0x10010001:Movie3:ThirdMovie

[CatalogFiles]
UnsignedPE=.\UnsignedPE.EXE
UnsignedDOS=.\UnsignedDOS.EXE
<HASH>UnsignedCAB=.\Unsigned.CAB
UnsignedClass=.\Unsigned.Class
SignedPE=.\SignedPE.EXE
```

> [!Note]  
> <span data-ttu-id="836f0-120">Der letzte Eintrag in der CDF-Datei muss immer über ein explizites Zeilen Trennzeichen am Ende der Zeile verfügen.</span><span class="sxs-lookup"><span data-stu-id="836f0-120">The last entry in the .cdf file must always have an explicit newline character at the end of the line.</span></span>

 

 

 
