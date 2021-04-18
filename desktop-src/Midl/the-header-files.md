---
title: Die Header Dateien
description: Die Schnittstellen Header Datei (Name. h) enthält Typdefinitionen und Funktions Deklarationen auf der Grundlage der Schnittstellen Definition in der aktuellen IDL-Datei sowie alle Datentypen und Vorgänge, die in den in der \ include-Direktive enthaltenen Dateien deklariert werden.
ms.assetid: 81fac1fa-6bd7-4a3e-8aa6-5104d4b25b55
keywords:
- Header Dateien (Mitte)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214ae80877b88d8061769b0d6bd56c13469427fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341257"
---
# <a name="the-header-files"></a><span data-ttu-id="83a7c-104">Die Header Dateien</span><span class="sxs-lookup"><span data-stu-id="83a7c-104">The Header Files</span></span>

<span data-ttu-id="83a7c-105">Die Schnittstellen Header Datei (Name. h) enthält Typdefinitionen und Funktions Deklarationen, die auf der Schnittstellen Definition in der aktuellen IDL-Datei basieren, sowie alle Datentypen und Vorgänge, die in den in der include-Direktive enthaltenen Dateien deklariert werden \# .</span><span class="sxs-lookup"><span data-stu-id="83a7c-105">The interface header file (Name.h) contains type definitions and function declarations based on the interface definition in the current IDL file, as well as all the data types and operations declared in the files included with the \#include directive.</span></span> <span data-ttu-id="83a7c-106">Datentypen aus den Dateien, die mit der Import-Anweisung importiert werden, werden nicht in die Header Datei repliziert. Stattdessen enthält die generierte Header Datei eine include-Zeile zu der aus der importierten Datei generierten H-Datei.</span><span class="sxs-lookup"><span data-stu-id="83a7c-106">Data types from the files imported with the import directive are not replicated to the header file; instead, the generated header file contains an include line to the H file generated from the imported file.</span></span>

<span data-ttu-id="83a7c-107">Fügen Sie diese Datei in die Quelldateien für die Proxy-dll und für Client Anwendungen ein, die die-Schnittstelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="83a7c-107">Include this file in the source files for the proxy DLL and for client applications that use the interface.</span></span>

<span data-ttu-id="83a7c-108">Der Standardname für eine Header Datei, die aus einer Datei erstellt wird. idl ist File. h.</span><span class="sxs-lookup"><span data-stu-id="83a7c-108">The default name for a header file generated from a file.idl is File.h.</span></span> <span data-ttu-id="83a7c-109">Der [**/Header**](-header.md) -Compilerschalter überschreibt den Standardnamen der Schnittstellen Header Datei.</span><span class="sxs-lookup"><span data-stu-id="83a7c-109">The [**/header**](-header.md) MIDL compiler switch overrides the default name of the interface header file.</span></span>

 

 




