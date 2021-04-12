---
title: Extrahieren der Code Beispiele
description: Obwohl die Codebeispiele in eine Reihe von Tutorial-Lektionen aufgeteilt sind, können die entsprechenden Beispiel Gruppierungen problemlos aus der Auflistung extrahiert werden.
ms.assetid: f8e20e40-cfef-4844-8b28-5a11fdcd691a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a593cf36b2fa235813c291eb35307153b28a2aa4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388176"
---
# <a name="extracting-the-code-samples"></a><span data-ttu-id="d032a-103">Extrahieren der Code Beispiele</span><span class="sxs-lookup"><span data-stu-id="d032a-103">Extracting the Code Samples</span></span>

<span data-ttu-id="d032a-104">Obwohl die Codebeispiele in eine Reihe von Tutorial-Lektionen aufgeteilt sind, können die entsprechenden Beispiel Gruppierungen problemlos aus der Auflistung extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="d032a-104">Though the code samples are divided into a series of tutorial lessons, the appropriate sample groupings can easily be extracted from the collection.</span></span> <span data-ttu-id="d032a-105">Die meisten der einzelnen Beispiel Verzeichnisse sind so konzipiert, dass Sie in Verbindung mit mindestens einem anderen Beispiel Verzeichnis funktionieren.</span><span class="sxs-lookup"><span data-stu-id="d032a-105">Most of the individual sample directories are meant to work in conjunction with at least one other sample directory.</span></span> <span data-ttu-id="d032a-106">Die Komponenten bezogenen Beispiele bestehen aus einem Client-und einem Server Paar, wobei der Server die Verwendung des Register Sample Utility erfordert.</span><span class="sxs-lookup"><span data-stu-id="d032a-106">The component-related samples consist of a client and server pair, with the server requiring the use of the REGISTER sample utility.</span></span> <span data-ttu-id="d032a-107">Im folgenden finden Sie eine Zusammenfassung der Beispiel Gruppierungen und die Vorgehensweise zum Extrahieren der einzelnen Gruppen als Erstell Bare Einheit.</span><span class="sxs-lookup"><span data-stu-id="d032a-107">Here is a summary of the sample groupings and how to extract each group as a buildable unit.</span></span> <span data-ttu-id="d032a-108">Kopieren Sie für jede Beispiel Gruppierung den Inhalt der angezeigten Verzeichnisse.</span><span class="sxs-lookup"><span data-stu-id="d032a-108">For each sample grouping, copy the content of the directories shown.</span></span> <span data-ttu-id="d032a-109">Das \[ angezeigte übergeordnete Ziel \] Verzeichnis erfordert keinen Inhalt aus der Samples-Verzweigung.</span><span class="sxs-lookup"><span data-stu-id="d032a-109">The parent \[destination\] directory shown requires no content from the samples branch.</span></span> <span data-ttu-id="d032a-110">In den Menüs "Hilfe" in den laufenden Beispielen wird jedoch davon ausgegangen, dass das entsprechende Lernprogramm ausgeführt wird. HTM-Hilfedateien befinden sich in diesem übergeordneten \[ Ziel \] Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="d032a-110">However, the help menus in the running samples do assume that the appropriate tutorial .HTM help files are located in this parent \[destination\] directory.</span></span>

<span data-ttu-id="d032a-111">Für die Win32-Anwendung "Read tut":</span><span class="sxs-lookup"><span data-stu-id="d032a-111">For the Win32 READTUT application:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    READTUT
```

<span data-ttu-id="d032a-112">Für die Win32-exe-Skeleton-Anwendung:</span><span class="sxs-lookup"><span data-stu-id="d032a-112">For the Win32 EXE skeleton application:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    EXESKEL
```

<span data-ttu-id="d032a-113">Für das Win32-DLL-Skelett:</span><span class="sxs-lookup"><span data-stu-id="d032a-113">For the Win32 DLL skeleton:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    DLLSKEL
    DLLUSER
```

<span data-ttu-id="d032a-114">Für die grundlegenden com-Objekt Beispiele:</span><span class="sxs-lookup"><span data-stu-id="d032a-114">For the basic COM object samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    COMOBJ
    COMUSER
```

<span data-ttu-id="d032a-115">Für die grundlegenden Client/Server-Beispiele für die Prozess interne dll-Komponente:</span><span class="sxs-lookup"><span data-stu-id="d032a-115">For the basic in-process DLL component client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    DLLSERVE
    DLLCLIEN
```

<span data-ttu-id="d032a-116">Für die Client-/Serverbeispiele für lizenzierte Komponenten:</span><span class="sxs-lookup"><span data-stu-id="d032a-116">For the licensed component client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    LICSERVE
    LICCLIEN
```

<span data-ttu-id="d032a-117">Für die standardmäßigen Marshallingbeispiele:</span><span class="sxs-lookup"><span data-stu-id="d032a-117">For the standard marshaling samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    MARSHAL2
```

<span data-ttu-id="d032a-118">Für die Beispiele für den lokalen Client/Server außerhalb des Prozesses:</span><span class="sxs-lookup"><span data-stu-id="d032a-118">For the out-of-process local client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    LOCSERVE
    LOCCLIEN
```

<span data-ttu-id="d032a-119">Für die Apartment Model-Client/Server-Beispiele:</span><span class="sxs-lookup"><span data-stu-id="d032a-119">For the apartment model client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    APTSERVE
    APTCLIEN
```

<span data-ttu-id="d032a-120">Für die DCOM-Client/Server-Beispiele (verteiltes com):</span><span class="sxs-lookup"><span data-stu-id="d032a-120">For the DCOM (Distributed COM) client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    APTSERVE
    REMCLIEN
```

<span data-ttu-id="d032a-121">Die Beispiele für die kostenlose Threading Client/Server:</span><span class="sxs-lookup"><span data-stu-id="d032a-121">For the free threading client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    FRESERVE
    FRECLIEN
```

<span data-ttu-id="d032a-122">Für die Verbindungs fähigen COM-Objekt Client/Server-Beispiele:</span><span class="sxs-lookup"><span data-stu-id="d032a-122">For the connectable COM object client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    CONSERVE
    CONCLIEN
```

<span data-ttu-id="d032a-123">Für die strukturierten Speicher Client/Server-Beispiele:</span><span class="sxs-lookup"><span data-stu-id="d032a-123">For the structured storage client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    STOSERVE
    STOCLIEN
```

<span data-ttu-id="d032a-124">Für die persistenten Objekt Client/Server-Beispiele:</span><span class="sxs-lookup"><span data-stu-id="d032a-124">For the persistent object client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    PERSERVE
    PERTEXT
    PERDRAW
    PERCLIEN
```

<span data-ttu-id="d032a-125">Für die DCOM-Sicherheits Client/Server-Beispiele:</span><span class="sxs-lookup"><span data-stu-id="d032a-125">For the DCOM security client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    DCDMARSH
    DCDSERVE
    DCOMDRAW
```

 

 




