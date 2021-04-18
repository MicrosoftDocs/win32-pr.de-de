---
title: Öffnen und Schließen von Dateien
description: Öffnen und Schließen von Dateien
ms.assetid: 72655d33-f685-4205-a982-f7cd20c59f22
keywords:
- AVIFileOpen-Funktion
- Avifilerelease-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68e1c51c4747e03bf4f18a8e6c560e45798e1c8c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106351862"
---
# <a name="opening-and-closing-files"></a><span data-ttu-id="a3b53-105">Öffnen und Schließen von Dateien</span><span class="sxs-lookup"><span data-stu-id="a3b53-105">Opening and Closing Files</span></span>

<span data-ttu-id="a3b53-106">Eine Anwendung muss vor dem Lesen oder schreiben eine AVI-Datei öffnen.</span><span class="sxs-lookup"><span data-stu-id="a3b53-106">An application must open an AVI file before reading or writing.</span></span> <span data-ttu-id="a3b53-107">Um eine AVI-Datei zu öffnen, verwenden Sie die [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="a3b53-107">To open an AVI file, use the [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) function.</span></span> <span data-ttu-id="a3b53-108">**AVIFileOpen** gibt die Adresse einer AVI-Datei Schnittstelle zurück, die das Handle der geöffneten Datei enthält, und erhöht den Verweis Zähler der Datei.</span><span class="sxs-lookup"><span data-stu-id="a3b53-108">**AVIFileOpen** returns the address of an AVI file interface that contains the handle of the open file and increments the reference count of the file.</span></span>

<span data-ttu-id="a3b53-109">Die **AVIFileOpen** -Funktion unterstützt die von Flags, die mit der [OpenFile](/documentation/) -Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3b53-109">The **AVIFileOpen** function supports the OF flags used with the [OpenFile](/documentation/) function.</span></span> <span data-ttu-id="a3b53-110">Wenn eine Anwendung in eine vorhandene Datei schreibt, muss Sie die des \_ Schreib Flags in **AVIFileOpen** einschließen.</span><span class="sxs-lookup"><span data-stu-id="a3b53-110">If an application writes to an existing file, it must include the OF\_WRITE flag in **AVIFileOpen**.</span></span> <span data-ttu-id="a3b53-111">Ebenso müssen Sie, wenn Ihre Anwendung eine neue Datei erstellt und in diese schreibt, den von \_ Create-und \_ Write-Flags in **AVIFileOpen** einschließen.</span><span class="sxs-lookup"><span data-stu-id="a3b53-111">Similarly, if your application creates and writes to a new file, you must include the OF\_CREATE and OF\_WRITE flags in **AVIFileOpen**.</span></span>

<span data-ttu-id="a3b53-112">Wenn Sie eine Datei mithilfe von **AVIFileOpen** öffnen, können Sie einen Standarddatei Handler verwenden, oder Sie können einen benutzerdefinierten Datei Handler zum Lesen und Schreiben in die Datei und deren Datenströme angeben.</span><span class="sxs-lookup"><span data-stu-id="a3b53-112">When you open a file using **AVIFileOpen**, you can use a default file handler or you can specify a custom file handler to read and write to the file and its data streams.</span></span> <span data-ttu-id="a3b53-113">In beiden Fällen durchsucht avifile die Registrierung nach dem richtigen Datei Handler, der verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a3b53-113">In either case, AVIFile searches the registry for the correct file handler to use.</span></span> <span data-ttu-id="a3b53-114">Sie müssen sicherstellen, dass benutzerdefinierte Datei Handler in der Registrierung vorliegen, bevor eine Anwendung darauf zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="a3b53-114">You must ensure custom file handlers are in the registry before an application can access them.</span></span>

<span data-ttu-id="a3b53-115">Sie können den Verweis Zähler einer Datei mithilfe der [**avifileadressf**](/windows/desktop/api/Vfw/nf-vfw-avifileaddref) -Funktion erhöhen.</span><span class="sxs-lookup"><span data-stu-id="a3b53-115">You can increment the reference count of a file by using the [**AVIFileAddRef**](/windows/desktop/api/Vfw/nf-vfw-avifileaddref) function.</span></span> <span data-ttu-id="a3b53-116">Dies kann z. b. der Fall sein, wenn Sie ein Handle der Datei Schnittstelle an eine andere Anwendung übergeben oder wenn Sie eine Datei geöffnet lassen möchten, während Sie eine Funktion verwenden, die die Datei normalerweise schließt.</span><span class="sxs-lookup"><span data-stu-id="a3b53-116">For example, you might want to do this when passing a handle of the file interface to another application, or when you want to keep a file open while using a function that would normally close the file.</span></span>

<span data-ttu-id="a3b53-117">Sie können eine Datei mit der [**avifilerelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) -Funktion schließen.</span><span class="sxs-lookup"><span data-stu-id="a3b53-117">You can close a file by using the [**AVIFileRelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) function.</span></span> <span data-ttu-id="a3b53-118">Die **avifilerelease** -Funktion Dekremente den Verweis Zähler einer AVI-Datei, speichert Änderungen an der Datei und schließt die Datei, wenn der Verweis Zähler Null erreicht.</span><span class="sxs-lookup"><span data-stu-id="a3b53-118">The **AVIFileRelease** function decrements the reference count of an AVI file, saves changes made to the file, and when the reference count reaches zero, closes the file.</span></span> <span data-ttu-id="a3b53-119">Ihre Anwendungen sollten den Verweis Zähler ausgleichen, indem Sie für jede Verwendung von [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) und **avifileadressf** einen **avifilerelease** -Rückruf einschließen.</span><span class="sxs-lookup"><span data-stu-id="a3b53-119">Your applications should balance the reference count by including a call to **AVIFileRelease** for each use of [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) and **AVIFileAddRef**.</span></span>

> [!Note]  
> <span data-ttu-id="a3b53-120">Eine Anwendung kann eine Datei mit einem oder mehreren Programmthreads öffnen.</span><span class="sxs-lookup"><span data-stu-id="a3b53-120">An application can open a file with one or more program threads.</span></span> <span data-ttu-id="a3b53-121">Um jedoch eine bestmögliche Leistung zu erzielen, sollte jeweils nur ein Thread auf die Datei zugreifen.</span><span class="sxs-lookup"><span data-stu-id="a3b53-121">However, for the best possible performance, only one thread should access the file at any one time.</span></span>

 

 

 