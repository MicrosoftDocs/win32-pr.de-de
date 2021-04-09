---
description: Normalerweise werden Debuginformationen in einer Symbol Datei gespeichert, getrennt von der ausführbaren Datei.
ms.assetid: 610e5cd3-9dc3-462c-98f8-6a63874464f8
title: Symboldateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d964fbe0ab5f07a6c3d7cfa08b057550e1cc2c74
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126055"
---
# <a name="symbol-files"></a><span data-ttu-id="40cf6-103">Symboldateien</span><span class="sxs-lookup"><span data-stu-id="40cf6-103">Symbol Files</span></span>

<span data-ttu-id="40cf6-104">Normalerweise werden Debuginformationen in einer Symbol Datei gespeichert, getrennt von der ausführbaren Datei.</span><span class="sxs-lookup"><span data-stu-id="40cf6-104">Normally, debugging information is stored in a symbol file separate from the executable.</span></span> <span data-ttu-id="40cf6-105">Die Implementierung dieser Debuginformationen hat sich im Laufe der Jahre geändert, und in der folgenden Dokumentation finden Sie Anleitungen zu diesen verschiedenen Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="40cf6-105">The implementation of this debugging information has changed over the years, and the following documentation will provide guidance regarding these various implementations.</span></span>

## <a name="pdb-files"></a><span data-ttu-id="40cf6-106">PDB-Dateien</span><span class="sxs-lookup"><span data-stu-id="40cf6-106">PDB files</span></span>

<span data-ttu-id="40cf6-107">Alle modernen Versionen der Microsoft-Compiler speichern Debuginformationen zu einer kompilierten ausführbaren Datei in einer separaten *Programm Daten Bank* Datei (. pdb).</span><span class="sxs-lookup"><span data-stu-id="40cf6-107">All modern versions of the Microsoft compilers store debugging information about a compiled executable in a separate *program database* (.pdb) file.</span></span> <span data-ttu-id="40cf6-108">Diese Datei wird im Allgemeinen als *PDB* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="40cf6-108">This file is commonly referred to as a *PDB*.</span></span> <span data-ttu-id="40cf6-109">Die Daten werden in einer separaten Datei der ausführbaren Datei gespeichert, um die Größe der ausführbaren Datei einzuschränken, Speicherplatz auf dem Datenträger zu sparen und den Zeitaufwand für das Laden der Daten zu verkürzen.</span><span class="sxs-lookup"><span data-stu-id="40cf6-109">The data is stored in a separate file from the executable to help limit the size of the executable, saving disk storage space and reducing the time it takes to load the data.</span></span> <span data-ttu-id="40cf6-110">Diese Methodik ermöglicht außerdem die Verteilung der ausführbaren Datei, ohne diese wichtigen Informationen offenzulegen, was das Programm leichter umkehren könnte.</span><span class="sxs-lookup"><span data-stu-id="40cf6-110">This methodology also allows the executable to be distributed without disclosing this significant information which could make the program easier to reverse engineer.</span></span>

<span data-ttu-id="40cf6-111">Erstellen Sie zum Erstellen einer PDB-Datei die ausführbare Datei mit Debuginformationen gemäß den Anweisungen für die Buildtools.</span><span class="sxs-lookup"><span data-stu-id="40cf6-111">To create a PDB, build your executable file with debugging information according to the directions for your build tools.</span></span>

<span data-ttu-id="40cf6-112">Die dbghelp-API kann PDB verwenden, um die folgenden Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="40cf6-112">The DbgHelp API is able to use PDBs to obtain the following information.</span></span>

-   <span data-ttu-id="40cf6-113">publics und Exporte</span><span class="sxs-lookup"><span data-stu-id="40cf6-113">publics and exports</span></span>
-   <span data-ttu-id="40cf6-114">globale Symbole</span><span class="sxs-lookup"><span data-stu-id="40cf6-114">global symbols</span></span>
-   <span data-ttu-id="40cf6-115">lokale Symbole</span><span class="sxs-lookup"><span data-stu-id="40cf6-115">local symbols</span></span>
-   <span data-ttu-id="40cf6-116">Typdaten</span><span class="sxs-lookup"><span data-stu-id="40cf6-116">type data</span></span>
-   <span data-ttu-id="40cf6-117">Quelldateien</span><span class="sxs-lookup"><span data-stu-id="40cf6-117">source files</span></span>
-   <span data-ttu-id="40cf6-118">Zeilennummern</span><span class="sxs-lookup"><span data-stu-id="40cf6-118">line numbers</span></span>

## <a name="dbg-files-and-embedded-debug-information"></a><span data-ttu-id="40cf6-119">Dbg-Dateien und eingebettete Debuginformationen</span><span class="sxs-lookup"><span data-stu-id="40cf6-119">DBG files and embedded debug information</span></span>

<span data-ttu-id="40cf6-120">Frühere Versionen des Microsoft-Toolsets, das zum Einbetten der Debuginformationen in die ausführbare Datei verwendet wird, werden jedoch normalerweise in eine separate Datei mit der Erweiterung. dbg entfernt.</span><span class="sxs-lookup"><span data-stu-id="40cf6-120">Previous versions of the Microsoft toolset used to embed the debugging information in the executable, however it would normally be stripped out into a separate file with a .dbg extension.</span></span> <span data-ttu-id="40cf6-121">Dies wird häufig als *dbg* -Datei bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="40cf6-121">This is commonly known as a *DBG* file.</span></span> <span data-ttu-id="40cf6-122">Dbg-Dateien verwenden dasselbe PE-Dateiformat wie ausführbare Dateien.</span><span class="sxs-lookup"><span data-stu-id="40cf6-122">DBG files use the same PE file format as executables.</span></span>

<span data-ttu-id="40cf6-123">Die dbghelp-API-Unterstützung für DBGs und eingebettete Debuginformationen ist begrenzt und umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="40cf6-123">The DbgHelp API support for DBGs and embedded debugging information is limited and includes the following.</span></span>

-   <span data-ttu-id="40cf6-124">publics und Exporte</span><span class="sxs-lookup"><span data-stu-id="40cf6-124">publics and exports</span></span>
-   <span data-ttu-id="40cf6-125">globale Symbole</span><span class="sxs-lookup"><span data-stu-id="40cf6-125">global symbols</span></span>

 

 



