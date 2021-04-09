---
title: Erstellen einer Datei oder eines streamhandlers
description: Erstellen einer Datei oder eines streamhandlers
ms.assetid: 9ec1af9a-f428-4323-a4f8-3eb923ce78d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b2f118f4f5279cea1aacedd58b86f23afa9a9af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036827"
---
# <a name="creating-a-file-or-stream-handler"></a><span data-ttu-id="1e92a-103">Erstellen einer Datei oder eines streamhandlers</span><span class="sxs-lookup"><span data-stu-id="1e92a-103">Creating a File or Stream Handler</span></span>

<span data-ttu-id="1e92a-104">In einer Anwendung, die in der Programmiersprache C geschrieben ist, erstellt ein Datei-oder streamhandler in der Regel eine Funktion für jede Methode.</span><span class="sxs-lookup"><span data-stu-id="1e92a-104">In an application written in the C programming language, a file or stream handler usually creates a function for each method.</span></span> <span data-ttu-id="1e92a-105">Die Anwendung greift auf diese Funktionen über ein Array von Funktions Zeigern zu, die der streamhandler erstellt.</span><span class="sxs-lookup"><span data-stu-id="1e92a-105">Your application accesses these functions through an array of function pointers the stream handler creates.</span></span> <span data-ttu-id="1e92a-106">Eine **iavistreamvtbl** -Struktur enthält das Array von Funktions Zeigern.</span><span class="sxs-lookup"><span data-stu-id="1e92a-106">An **IAVIStreamVtbl** structure contains the array of function pointers.</span></span> <span data-ttu-id="1e92a-107">Ein Datenstrom Handler kann jeden beliebigen Namen zuweisen, den er für die Methoden erstellt.</span><span class="sxs-lookup"><span data-stu-id="1e92a-107">A stream handler can assign any name it wants to functions it creates for the methods.</span></span> <span data-ttu-id="1e92a-108">Die Position des Funktions Zeigers in der Struktur impliziert die Entsprechung der Funktion zur Methode.</span><span class="sxs-lookup"><span data-stu-id="1e92a-108">The position of the function pointer in the structure implies the correspondence of the function to the method.</span></span> <span data-ttu-id="1e92a-109">Beispielsweise entspricht der erste Funktionszeiger in der-Struktur der **QueryInterface** -Methode.</span><span class="sxs-lookup"><span data-stu-id="1e92a-109">For example, the first function pointer in the structure corresponds to the **QueryInterface** method.</span></span> <span data-ttu-id="1e92a-110">Der Datenstrom Handler muss alle Funktionen einer Schnittstelle bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="1e92a-110">Your stream handler must provide all the functions of an interface.</span></span>

 

 




