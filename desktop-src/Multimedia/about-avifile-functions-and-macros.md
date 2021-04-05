---
title: Informationen zu avifile-Funktionen und-Makros
description: Informationen zu avifile-Funktionen und-Makros
ms.assetid: 877f6759-8271-47eb-8a7f-540393e5ae89
keywords:
- Avifileingeit-Funktion
- Avifileexit-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f66bbac900b69841fd7cba814aad339731b75727
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037574"
---
# <a name="about-avifile-functions-and-macros"></a><span data-ttu-id="edffb-105">Informationen zu avifile-Funktionen und-Makros</span><span class="sxs-lookup"><span data-stu-id="edffb-105">About AVIFile Functions and Macros</span></span>

<span data-ttu-id="edffb-106">Die avifile-Funktionen und-Makros verarbeiten die Informationen in zeitbasierten Dateien als einen oder mehrere *Datenströme* anstelle von markierten Datenblöcken, die als Blöcke bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="edffb-106">The AVIFile functions and macros handle the information in time-based files as one or more *data streams* instead of tagged blocks of data called chunks.</span></span> <span data-ttu-id="edffb-107">Datenströme verweisen auf die Komponenten einer zeitbasierten Datei.</span><span class="sxs-lookup"><span data-stu-id="edffb-107">Data streams refer to the components of a time-based file.</span></span> <span data-ttu-id="edffb-108">Eine AVI-Datei kann mehrere verschiedene Arten von Daten enthalten, z. b. eine Videosequenz, einen englischen Sound Sound und einen französischen Sound.</span><span class="sxs-lookup"><span data-stu-id="edffb-108">An AVI file can contain several different types of data, such as a video sequence, an English soundtrack, and a French soundtrack.</span></span> <span data-ttu-id="edffb-109">Mithilfe von avifile kann eine Anwendung separat auf jede dieser Komponenten zugreifen.</span><span class="sxs-lookup"><span data-stu-id="edffb-109">Using AVIFile, an application can access each of these components separately.</span></span>

> [!Note]  
> <span data-ttu-id="edffb-110">Obwohl die avifile-Funktionen und-Makros mit einer beliebigen Riff Datei funktionieren, wird in dieser Übersicht ihre Verwendung nur mit AVI-Dateien veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="edffb-110">Although the AVIFile functions and macros work with any RIFF file, this overview demonstrates their use with AVI files only.</span></span> <span data-ttu-id="edffb-111">AVI-Dateien sind in der Regel die zeitbasierten Dateien, die mit den avifile-Makros und-Funktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="edffb-111">AVI files are typically the time-based files used with the AVIFile macros and functions.</span></span>

 

<span data-ttu-id="edffb-112">Avifile-Funktionen und-Makros sind in einer Dynamic Link Library enthalten.</span><span class="sxs-lookup"><span data-stu-id="edffb-112">AVIFile functions and macros are contained in a dynamic-link library.</span></span> <span data-ttu-id="edffb-113">Um die Bibliothek zu initialisieren, verwenden [**Sie die avifilinput IT**](/windows/desktop/api/Vfw/nf-vfw-avifileinit) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="edffb-113">To initialize the library, use the [**AVIFileInit**](/windows/desktop/api/Vfw/nf-vfw-avifileinit) function.</span></span> <span data-ttu-id="edffb-114">Nachdem Sie die Bibliothek initialisiert haben, können Sie eine beliebige der avifile-Funktionen oder-Makros verwenden.</span><span class="sxs-lookup"><span data-stu-id="edffb-114">After you initialize the library, you can use any of the AVIFile functions or macros.</span></span> <span data-ttu-id="edffb-115">Verwenden Sie zum Freigeben der Bibliothek die [**avifileexit**](/windows/desktop/api/Vfw/nf-vfw-avifileexit) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="edffb-115">To release the library, use the [**AVIFileExit**](/windows/desktop/api/Vfw/nf-vfw-avifileexit) function.</span></span> <span data-ttu-id="edffb-116">Avifile verwaltet den Verweis Zähler der Anwendungen, die die Bibliothek verwenden, jedoch nicht die, die Sie freigegeben haben.</span><span class="sxs-lookup"><span data-stu-id="edffb-116">AVIFile maintains a reference count of the applications that are using the library, but not those that have released it.</span></span> <span data-ttu-id="edffb-117">Ihre Anwendungen sollten jede Verwendung von **AVIFileInit** mit einem **avifileexit** -Befehl ausgleichen, um die Bibliothek vollständig freizugeben, nachdem jede Anwendung Sie verwendet hat.</span><span class="sxs-lookup"><span data-stu-id="edffb-117">Your applications should balance each use of **AVIFileInit** with a call to **AVIFileExit** to completely release the library after each application finishes using it.</span></span>

 

 




