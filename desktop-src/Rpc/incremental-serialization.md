---
title: Krementelle Serialisierung
description: Wenn Sie die Serialisierung im inkrementellen Stil verwenden, stellen Sie drei Routinen zum Bearbeiten des Puffers bereit.
ms.assetid: c7383b4d-94d1-4edd-ac29-c11fb5343156
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 409f8da0881719ec9273f4dd12cc99e3d36c35a3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516017"
---
# <a name="incremental-serialization"></a><span data-ttu-id="5a31e-103">Krementelle Serialisierung</span><span class="sxs-lookup"><span data-stu-id="5a31e-103">Incremental Serialization</span></span>

<span data-ttu-id="5a31e-104">Wenn Sie die Serialisierung im inkrementellen Stil verwenden, stellen Sie drei Routinen zum Bearbeiten des Puffers bereit.</span><span class="sxs-lookup"><span data-stu-id="5a31e-104">When using the incremental style serialization, you supply three routines to manipulate the buffer.</span></span> <span data-ttu-id="5a31e-105">Diese Routinen lauten: Zuordnungsmodus, Lese-und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="5a31e-105">These routines are: Alloc, Read, and Write.</span></span> <span data-ttu-id="5a31e-106">Die Belegungs Routine ordnet einen Puffer mit der erforderlichen Größe zu.</span><span class="sxs-lookup"><span data-stu-id="5a31e-106">The Alloc routine allocates a buffer of the required size.</span></span> <span data-ttu-id="5a31e-107">Die Schreib Routine schreibt die Daten in den Puffer, und die Lese Routine ruft einen Puffer ab, der gemarshallte Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="5a31e-107">The Write routine writes the data into the buffer, and the Read routine retrieves a buffer that contains marshaled data.</span></span> <span data-ttu-id="5a31e-108">Mit einem einzelnen Serialisierungsaufruf können mehrere Aufrufe dieser Routinen durchführen werden.</span><span class="sxs-lookup"><span data-stu-id="5a31e-108">A single serialization call can make several calls to these routines.</span></span>

<span data-ttu-id="5a31e-109">Der inkrementelle Stil der Serialisierung verwendet die folgenden Routinen:</span><span class="sxs-lookup"><span data-stu-id="5a31e-109">The incremental style of serialization uses the following routines:</span></span>

-   [<span data-ttu-id="5a31e-110">**Mesencodeinkrementallenker Create**</span><span class="sxs-lookup"><span data-stu-id="5a31e-110">**MesEncodeIncrementalHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate)
-   [<span data-ttu-id="5a31e-111">**Mesdecodeinkrementallagercreate**</span><span class="sxs-lookup"><span data-stu-id="5a31e-111">**MesDecodeIncrementalHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate)
-   [<span data-ttu-id="5a31e-112">**Mesincrementalhandlereset**</span><span class="sxs-lookup"><span data-stu-id="5a31e-112">**MesIncrementalHandleReset**</span></span>](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset)
-   [<span data-ttu-id="5a31e-113">**Meslenker frei**</span><span class="sxs-lookup"><span data-stu-id="5a31e-113">**MesHandleFree**</span></span>](/windows/desktop/api/Midles/nf-midles-meshandlefree)

<span data-ttu-id="5a31e-114">Die Prototypen für die Zuordnungs-, Lese-und Schreibfunktionen, die Sie bereitstellen müssen, sind unten dargestellt:</span><span class="sxs-lookup"><span data-stu-id="5a31e-114">The prototypes for the Alloc, Read, and Write functions that you must provide are shown below:</span></span>

``` syntax
void __RPC_USER Alloc (
   void *State,          /* application-defined pointer */
   char **pBuffer,       /* returns pointer to allocated buffer */
   unsigned int *pSize); /* inputs requested bytes; outputs 
                         /* pBuffer size */

void __RPC_USER Write (
   void *State,          /* application-defined pointer */
   char *Buffer,         /* buffer with serialized data */
   unsigned int Size);   /* number of bytes to write from Buffer */

void __RPC_USER Read (
   void *State,          /* application-defined pointer */
   char **pBuffer,       /* returned pointer to buffer with data */
   unsigned int *pSize); /* number of bytes to read into pBuffer */
```

<span data-ttu-id="5a31e-115">Die Zustands Eingabe ein Parameter für alle drei Funktionen ist der Anwendungs definierte Zeiger, der dem Codierungs Dienst Handle zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="5a31e-115">The State input a parameter for all three functions is the application-defined pointer that was associated with the encoding services handle.</span></span> <span data-ttu-id="5a31e-116">Die Anwendung kann mit diesem Zeiger auf die Struktur zugreifen, die anwendungsspezifische Informationen enthält, z. b. ein Datei Handle oder einen Streamzeiger.</span><span class="sxs-lookup"><span data-stu-id="5a31e-116">The application can use this pointer to access the structure containing application-specific information, such as a file handle or stream pointer.</span></span> <span data-ttu-id="5a31e-117">Beachten Sie, dass die Stub den Zustands Zeiger nicht ändern, um ihn an die Zuordnungen, Lese-und Schreibfunktionen zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="5a31e-117">Note that the stubs do not modify the State pointer other than to pass it to the Alloc, Read, and Write functions.</span></span> <span data-ttu-id="5a31e-118">Während der Codierung wird die Zuweisung zum Abrufen eines Puffers aufgerufen, in den die Daten serialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="5a31e-118">During encoding, Alloc is called to obtain a buffer into which the data is serialized.</span></span> <span data-ttu-id="5a31e-119">Anschließend wird Write aufgerufen, damit die Anwendung steuern kann, wann und wo die serialisierten Daten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="5a31e-119">Then, Write is called to enable the application to control when and where the serialized data is stored.</span></span> <span data-ttu-id="5a31e-120">Beim Decodieren wird Read aufgerufen, um die angeforderte Anzahl von Bytes serialisierter Daten von dem Speicherort der Anwendung zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="5a31e-120">During decoding, Read is called to return the requested number of bytes of serialized data from where the application stored it.</span></span>

<span data-ttu-id="5a31e-121">Ein wichtiges Feature des inkrementellen Stils ist, dass das Handle den Zustands Zeiger für Sie beibehält.</span><span class="sxs-lookup"><span data-stu-id="5a31e-121">An important feature of the incremental style is that the handle keeps the state pointer for you.</span></span> <span data-ttu-id="5a31e-122">Dieser Zeiger behält den Zustand bei und wird nie von den RPC-Funktionen berührt, es sei denn, er übergibt den Zeiger an die Zuordnungs-, Schreib-oder Lesefunktion.</span><span class="sxs-lookup"><span data-stu-id="5a31e-122">This pointer maintains the state and is never touched by the RPC functions, except when passing the pointer to Alloc, Write, or Read function.</span></span> <span data-ttu-id="5a31e-123">Das Handle behält außerdem einen internen Zustand bei, der es ermöglicht, mehrere Typinstanzen in denselben Puffer zu codieren und zu decodieren, indem bei Bedarf für die Ausrichtung Auffüllung hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="5a31e-123">The handle also maintains an internal state that makes it possible to encode and decode several type instances to the same buffer by adding padding as needed for alignment.</span></span> <span data-ttu-id="5a31e-124">Die [**mesincrementalhandlereset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) -Funktion setzt ein Handle auf den ursprünglichen Zustand zurück, um das Lesen oder Schreiben am Anfang des Puffers zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5a31e-124">The [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) function resets a handle to its initial state to enable reading or writing from the beginning of the buffer.</span></span>

<span data-ttu-id="5a31e-125">Die Zuordnungs-und Schreibfunktionen, zusammen mit einem Anwendungs definierten Zeiger, werden einem Codierungs Dienst Handle durch einen Aufrufen der [**mesencodeinkrementallenker Create**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate) -Funktion zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="5a31e-125">The Alloc and Write functions, along with an application-defined pointer, are associated with an encoding-services handle by a call to the [**MesEncodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate) function.</span></span> <span data-ttu-id="5a31e-126">**Mesencodeinkrementaltorcreate** ordnet den für das Handle benötigten Arbeitsspeicher zu und initialisiert ihn anschließend.</span><span class="sxs-lookup"><span data-stu-id="5a31e-126">**MesEncodeIncrementalHandleCreate** allocates the memory needed for the handle and then initializes it.</span></span>

<span data-ttu-id="5a31e-127">Die Anwendung kann [**mesdecodeinkrementallagercreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate) aufrufen, um ein Decodierungs Handle zu erstellen, [**mesincrementalhandlereset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) zum erneuten Initialisieren des Handles oder [**meslagerfree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) , um den Arbeitsspeicher des Handles freizugeben.</span><span class="sxs-lookup"><span data-stu-id="5a31e-127">The application can call [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate) to create a decoding handle, [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) to reinitialize the handle, or [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) to free the handle's memory.</span></span> <span data-ttu-id="5a31e-128">Die Read-Funktion wird zusammen mit einem Anwendungs definierten Parameter einem Decodierungs Handle durch einen aufzurufenden Vorgang der **mesdecodeinkrementallagercreate** -Routine zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="5a31e-128">The Read function, along with an application-defined parameter, is associated with a decoding handle by a call to the **MesDecodeIncrementalHandleCreate** routine.</span></span> <span data-ttu-id="5a31e-129">Die-Funktion erstellt das Handle und initialisiert es.</span><span class="sxs-lookup"><span data-stu-id="5a31e-129">The function creates the handle and initializes it.</span></span>

<span data-ttu-id="5a31e-130">Die Parameter userState, Zuordnungen, Write und Read von [**mesincrementalhandlereset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) können **null** sein, um anzugeben, dass keine Änderung vorgenommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a31e-130">The UserState, Alloc, Write, and Read parameters of [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) can be **NULL** to indicate no change.</span></span>

 

 




