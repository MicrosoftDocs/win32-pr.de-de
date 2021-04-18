---
description: Wenn das System ein Programm startet, das dynamische Verknüpfungen der Ladezeit verwendet, verwendet es die Informationen, die der Linker in der Datei abgelegt hat, um die Namen der DLLs zu suchen, die vom Prozess verwendet werden.
ms.assetid: 29a17116-bb08-4fdd-857c-b7a7f8d2278c
title: Dynamische Verknüpfung Load-Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28435fd6df4a3fc5311dc46dbb761b48c139a6fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530014"
---
# <a name="load-time-dynamic-linking"></a><span data-ttu-id="47199-103">Dynamische Verknüpfung Load-Time</span><span class="sxs-lookup"><span data-stu-id="47199-103">Load-Time Dynamic Linking</span></span>

<span data-ttu-id="47199-104">Wenn das System ein Programm startet, das dynamische Verknüpfungen der Ladezeit verwendet, verwendet es die Informationen, die der Linker in der Datei abgelegt hat, um die Namen der DLLs zu suchen, die vom Prozess verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47199-104">When the system starts a program that uses load-time dynamic linking, it uses the information the linker placed in the file to locate the names of the DLLs that are used by the process.</span></span> <span data-ttu-id="47199-105">Das System sucht dann nach den DLLs.</span><span class="sxs-lookup"><span data-stu-id="47199-105">The system then searches for the DLLs.</span></span> <span data-ttu-id="47199-106">Weitere Informationen finden Sie unter [Dynamic-Link Library Search Order](dynamic-link-library-search-order.md).</span><span class="sxs-lookup"><span data-stu-id="47199-106">For more information, see [Dynamic-Link Library Search Order](dynamic-link-library-search-order.md).</span></span>

<span data-ttu-id="47199-107">Wenn das System eine erforderliche DLL nicht finden kann, wird der Prozess beendet, und es wird ein Dialogfeld angezeigt, in dem der Fehler an den Benutzer gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="47199-107">If the system cannot locate a required DLL, it terminates the process and displays a dialog box that reports the error to the user.</span></span> <span data-ttu-id="47199-108">Andernfalls ordnet das System die dll dem virtuellen Adressraum des Prozesses zu und erhöht den Verweis Zähler der dll.</span><span class="sxs-lookup"><span data-stu-id="47199-108">Otherwise, the system maps the DLL into the virtual address space of the process and increments the DLL reference count.</span></span>

<span data-ttu-id="47199-109">Das System ruft die Einstiegspunkt Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="47199-109">The system calls the entry-point function.</span></span> <span data-ttu-id="47199-110">Die Funktion empfängt einen Code, der angibt, dass der Prozess die dll lädt.</span><span class="sxs-lookup"><span data-stu-id="47199-110">The function receives a code indicating that the process is loading the DLL.</span></span> <span data-ttu-id="47199-111">Wenn die Einstiegspunktfunktion nicht den Wert TRUE zurückgibt, beendet das System den Prozess mit einer entsprechenden Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="47199-111">If the entry-point function does not return TRUE, the system terminates the process and reports the error.</span></span> <span data-ttu-id="47199-112">Weitere Informationen zur Einstiegspunkt Funktion finden Sie unter [Dynamic-Link Library Entry-Point Function](dynamic-link-library-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="47199-112">For more information about the entry-point function, see [Dynamic-Link Library Entry-Point Function](dynamic-link-library-entry-point-function.md).</span></span>

<span data-ttu-id="47199-113">Schließlich ändert das System die Funktions Adress Tabelle mit den Start Adressen für die importierten DLL-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="47199-113">Finally, the system modifies the function address table with the starting addresses for the imported DLL functions.</span></span>

<span data-ttu-id="47199-114">Die dll wird während der Initialisierung dem virtuellen Adressraum des Prozesses zugeordnet und nur bei Bedarf in den physischen Speicher geladen.</span><span class="sxs-lookup"><span data-stu-id="47199-114">The DLL is mapped into the virtual address space of the process during its initialization and is loaded into physical memory only when needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="47199-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="47199-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47199-116">Verwenden Load-Time dynamischen Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="47199-116">Using Load-Time Dynamic Linking</span></span>](using-load-time-dynamic-linking.md)
</dt> </dl>

 

 



