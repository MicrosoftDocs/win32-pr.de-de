---
description: Einige der Netzwerkanbieter Funktionen übernehmen die Adresse und Größe eines Puffers, in dem die Funktion eine Datenstruktur mit variabler Größe platziert.
ms.assetid: 0029a04d-6cf2-40e1-ae1d-4c349a379ad7
title: Verarbeiten von gepufferten Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e123fc1ccccae6120b6db1c9ada554acc5b02a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217335"
---
# <a name="handling-buffered-data"></a><span data-ttu-id="724a5-103">Verarbeiten von gepufferten Daten</span><span class="sxs-lookup"><span data-stu-id="724a5-103">Handling Buffered Data</span></span>

<span data-ttu-id="724a5-104">Einige der Netzwerkanbieter Funktionen übernehmen die Adresse und Größe eines Puffers, in dem die Funktion eine Datenstruktur mit variabler Größe platziert.</span><span class="sxs-lookup"><span data-stu-id="724a5-104">Several of the network provider functions take the address and size of a buffer into which the function places a variable-sized data structure.</span></span>

<span data-ttu-id="724a5-105">In jedem Fall ist der verwendete Mechanismus identisch.</span><span class="sxs-lookup"><span data-stu-id="724a5-105">In each case, the mechanism used is the same.</span></span> <span data-ttu-id="724a5-106">Der Aufrufer ordnet einen Puffer zu und übergibt seine Adresse an die Funktion.</span><span class="sxs-lookup"><span data-stu-id="724a5-106">The caller allocates a buffer and passes its address to the function.</span></span> <span data-ttu-id="724a5-107">Außerdem übergibt Sie die Adresse eines **DWORD** , das die Größe des Puffers angibt, in Bytes.</span><span class="sxs-lookup"><span data-stu-id="724a5-107">It also passes the address of a **DWORD** that specifies the size of the buffer, in bytes.</span></span>

<span data-ttu-id="724a5-108">Die Funktion kopiert dann den Großteil der angeforderten Datenstruktur, wie Sie in den Puffer kopiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="724a5-108">The function then copies as much of the requested data structure as it can into the buffer.</span></span> <span data-ttu-id="724a5-109">Wenn alle Daten in den Puffer passen, gibt die Funktion "WN Success" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="724a5-109">If all of the data fits into the buffer, the function returns WN\_SUCCESS.</span></span> <span data-ttu-id="724a5-110">Wenn die Daten nicht in den Puffer passen, bleiben die Daten möglicherweise unvollständig, und die Funktion legt den Fehler für die WN- \_ Daten mehr fest \_ .</span><span class="sxs-lookup"><span data-stu-id="724a5-110">If the data does not fit into the buffer, the data may be left incomplete, and the function sets the WN\_MORE\_DATA error.</span></span> <span data-ttu-id="724a5-111">In beiden Fällen wird das **DWORD** , das die Größe des Puffers angibt, auf die Anzahl der Bytes festgelegt, die tatsächlich für die Datenstruktur erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="724a5-111">In either case, the **DWORD** indicating the size of the buffer is set to the number of bytes actually required by the data structure.</span></span> <span data-ttu-id="724a5-112">Auf diese Weise kann der Aufrufer einen neuen Puffer der erforderlichen Größe zuordnen und die Funktion erneut aufzurufen, wenn der Puffer, der an übergeben wurde, zu klein war und die Funktion fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="724a5-112">This way, if the buffer passed in was too small and the function failed, the caller may allocate a new buffer of the required size and call the function again.</span></span>

<span data-ttu-id="724a5-113">Wenn die zurückgegebenen Datenstrukturen Zeichen folgen variabler Länge enthalten, enthalten die einzelnen Datenstrukturen in der Regel Zeiger auf diese Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="724a5-113">When the data structures returned include variable-length strings, the individual data structures typically contain pointers to these strings.</span></span> <span data-ttu-id="724a5-114">Die Zeichen folgen selbst sollten auch innerhalb des Puffers abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="724a5-114">The strings themselves should also be placed within the buffer.</span></span> <span data-ttu-id="724a5-115">Es ist jedoch wichtig, Sie am Ende des Puffers zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="724a5-115">However, it is important to place them at the end of the buffer.</span></span> <span data-ttu-id="724a5-116">Andernfalls wird die Indizierung der Nth-Struktur unmöglich.</span><span class="sxs-lookup"><span data-stu-id="724a5-116">Otherwise, they will make indexing to the Nth structure impossible.</span></span> <span data-ttu-id="724a5-117">Anders ausgedrückt: alle Strukturen werden am Anfang des Puffers zusammenhängend angeordnet.</span><span class="sxs-lookup"><span data-stu-id="724a5-117">In other words, all structures are located contiguously at the beginning of the buffer.</span></span> <span data-ttu-id="724a5-118">Zeiger auf Zeichen folgen oder Variablen mit variabler Länge müssen tatsächliche Zeiger sein, nicht im Puffer Offsets.</span><span class="sxs-lookup"><span data-stu-id="724a5-118">Pointers to strings or variable length data must be actual pointers, not offsets into the buffer.</span></span>

<span data-ttu-id="724a5-119">Wenn ein Puffer zum übergeben und Zurückgeben von Daten verwendet wird, die nur aus Zeichen folgen bestehen, muss das **DWORD** , das die Größe des Puffers angibt, auf die Gesamtanzahl der Zeichen festgelegt werden, die in diese Zeichen folgen passen, nicht auf die Anzahl der Bytes.</span><span class="sxs-lookup"><span data-stu-id="724a5-119">When a buffer is used to pass in and return data that consists only of strings, the **DWORD** specifying the size of the buffer should be set to the total number of characters that will fit in these strings, not to the number of bytes.</span></span>

 

 



