---
title: Server Entwicklung mithilfe von Kontext Handles
description: Aus Sicht der Serverprogramm Entwicklung ist ein Kontext Handle ein nicht typisierter Zeiger. Server Programme initialisieren Kontext Handles, indem Sie Sie auf Daten im Arbeitsspeicher oder in einer anderen Form von Speicher (z. b. Dateien auf Datenträgern) verweisen.
ms.assetid: 6a1aabca-4cb9-401c-90c7-0cff7a69b7b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f743a4a6aa4a2aa7b6987bb54dc56e55cffbc76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037406"
---
# <a name="server-development-using-context-handles"></a><span data-ttu-id="89d89-104">Server Entwicklung mithilfe von Kontext Handles</span><span class="sxs-lookup"><span data-stu-id="89d89-104">Server Development Using Context Handles</span></span>

<span data-ttu-id="89d89-105">Aus Sicht der Serverprogramm Entwicklung ist ein Kontext Handle ein nicht typisierter Zeiger.</span><span class="sxs-lookup"><span data-stu-id="89d89-105">From the perspective of server program development, a context handle is an untyped pointer.</span></span> <span data-ttu-id="89d89-106">Server Programme initialisieren Kontext Handles, indem Sie Sie auf Daten im Arbeitsspeicher oder in einer anderen Form von Speicher (z. b. Dateien auf Datenträgern) verweisen.</span><span class="sxs-lookup"><span data-stu-id="89d89-106">Server programs initialize context handles by pointing them at data in memory or on some other form of storage (such as files on disks).</span></span>

<span data-ttu-id="89d89-107">Nehmen wir beispielsweise an, dass ein Client ein Kontext Handle verwendet, um eine Reihe von Updates für einen Datensatz in einer Datenbank anzufordern.</span><span class="sxs-lookup"><span data-stu-id="89d89-107">For instance, suppose that a client uses a context handle to request a series of updates to a record in a database.</span></span> <span data-ttu-id="89d89-108">Der Client ruft eine Remote Prozedur auf dem Server auf und übergibt ihm einen Suchschlüssel.</span><span class="sxs-lookup"><span data-stu-id="89d89-108">The client calls a remote procedure on the server and passes it a search key.</span></span> <span data-ttu-id="89d89-109">Das Serverprogramm sucht in der Datenbank nach dem Suchschlüssel und ruft die ganzzahlige Datensatznummer des übereinstimmenden Datensatzes ab.</span><span class="sxs-lookup"><span data-stu-id="89d89-109">The server program searches the database for the search key and obtains the integer record number of the matching record.</span></span> <span data-ttu-id="89d89-110">Der Server kann dann einen Zeiger auf den Speicherort, der die Datensatznummer enthält, auf "void" zeigen.</span><span class="sxs-lookup"><span data-stu-id="89d89-110">The server can then point a pointer to void at a memory location containing the record number.</span></span> <span data-ttu-id="89d89-111">Wenn der Wert zurückgegeben wird, muss die Remote Prozedur den Zeiger als Kontext Handle über seinen Rückgabewert oder seine Parameterliste zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="89d89-111">When it returns, the remote procedure would need to return the pointer as a context handle through its return value or its parameter list.</span></span> <span data-ttu-id="89d89-112">Der Client müsste den Zeiger an den Server übergeben, wenn er Remote Prozeduren zum Aktualisieren des Datensatzes aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="89d89-112">The client would need to pass the pointer to the server each time it called remote procedures to update the record.</span></span> <span data-ttu-id="89d89-113">Während jedes dieser Aktualisierungs Vorgänge wandelt der Server den void-Zeiger in einen Zeiger auf eine Ganzzahl um.</span><span class="sxs-lookup"><span data-stu-id="89d89-113">During each of these update operations, the server would cast the void pointer to be a pointer to an integer.</span></span>

<span data-ttu-id="89d89-114">Nachdem das Serverprogramm das Kontext Handle auf Kontext Daten verweist, gilt das Handle als geöffnet.</span><span class="sxs-lookup"><span data-stu-id="89d89-114">After the server program points the context handle at context data, the handle is considered opened.</span></span> <span data-ttu-id="89d89-115">Handles, die einen **null** -Wert enthalten, werden geschlossen.</span><span class="sxs-lookup"><span data-stu-id="89d89-115">Handles containing a **NULL** value are closed.</span></span> <span data-ttu-id="89d89-116">Der Server verwaltet ein geöffnetes Kontext Handle, bis der Client eine Remote Prozedur aufruft, die ihn schließt.</span><span class="sxs-lookup"><span data-stu-id="89d89-116">The server maintains an opened context handle until the client calls a remote procedure that closes it.</span></span> <span data-ttu-id="89d89-117">Wenn die Client Sitzung beendet wird, während das Handle geöffnet ist, ruft die RPC-Laufzeit die Server-Lauf Zeit Routine auf, um das Handle freizugeben.</span><span class="sxs-lookup"><span data-stu-id="89d89-117">If the client session terminates while the handle is open, the RPC run time calls the server run-down routine to free the handle.</span></span>

<span data-ttu-id="89d89-118">Das folgende Code Fragment veranschaulicht, wie ein-Server ein Kontext Handle implementieren kann.</span><span class="sxs-lookup"><span data-stu-id="89d89-118">The following code fragment demonstrates how a server might implement a context handle.</span></span> <span data-ttu-id="89d89-119">In diesem Beispiel verwaltet der Server eine Datendatei, in die der Client mithilfe von Remote Prozeduren schreibt.</span><span class="sxs-lookup"><span data-stu-id="89d89-119">In this example, the server maintains a data file that the client writes to using remote procedures.</span></span> <span data-ttu-id="89d89-120">Die Kontextinformationen sind ein Datei Handle, das den aktuellen Speicherort in der Datei nachverfolgt, an der der Serverdaten schreibt.</span><span class="sxs-lookup"><span data-stu-id="89d89-120">The context information is a file handle that keeps track of the current location in the file where the server will write data.</span></span> <span data-ttu-id="89d89-121">Das Datei Handle wird als Kontext Handle in der Parameterliste für Remote Prozedur Aufrufe verpackt.</span><span class="sxs-lookup"><span data-stu-id="89d89-121">The file handle is packaged as a context handle in the parameter list to remote procedure calls.</span></span> <span data-ttu-id="89d89-122">Eine-Struktur enthält den Dateinamen und das Datei handle.</span><span class="sxs-lookup"><span data-stu-id="89d89-122">A structure contains the file name and the file handle.</span></span> <span data-ttu-id="89d89-123">Die Schnittstellen Definition für dieses Beispiel wird unter [Schnittstellen Entwicklung mithilfe von Kontext Handles](interface-development-using-context-handles.md)gezeigt.</span><span class="sxs-lookup"><span data-stu-id="89d89-123">The interface definition for this example is shown in [Interface Development Using Context Handles](interface-development-using-context-handles.md).</span></span>


```C++
/* cxhndlp.c (fragment of file containing remote procedures) */
typedef struct 
{
     FILE* hFile;
     char   achFile[256];
} FILE_CONTEXT_TYPE;
```



<span data-ttu-id="89d89-124">Die Funktion remoteopen öffnet eine Datei auf dem Server:</span><span class="sxs-lookup"><span data-stu-id="89d89-124">The function RemoteOpen opens a file on the server:</span></span>


```C++
short RemoteOpen(
    PPCONTEXT_HANDLE_TYPE pphContext,
    unsigned char *pszFileName)
{
    FILE               *hFile;
    FILE_CONTEXT_TYPE  *pFileContext;
 
    if ((hFile = fopen(pszFileName, "r")) == NULL) 
    {
        *pphContext = (PCONTEXT_HANDLE_TYPE) NULL;
        return(-1);
    }
    else 
    {
        pFileContext = (FILE_CONTEXT_TYPE *) 
                       MIDL_user_allocate(sizeof(FILE_CONTEXT_TYPE));
        pFileContext->hFile = hFile;
        // check if pszFileName is longer than 256 and if yes, return
        // an error
        strcpy_s(pFileContext->achFile, srlen(pszFileName), pszFileName);
        *pphContext = (PCONTEXT_HANDLE_TYPE) pFileContext;
        return(0);
    }
}
```



<span data-ttu-id="89d89-125">Die Funktion RemoteRead liest eine Datei auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="89d89-125">The function RemoteRead reads a file on the server.</span></span>


```C++
short RemoteRead(
    PCONTEXT_HANDLE_TYPE phContext, 
    unsigned char *pbBuf, 
    short *pcbBuf) 
{ 
    FILE_CONTEXT_TYPE *pFileContext; 
    printf("in RemoteRead\n"); 
    pFileContext = (FILE_CONTEXT_TYPE *) phContext; 
    *pcbBuf = (short) fread(pbBuf, sizeof(char), 
                            BUFSIZE, 
                            pFileContext->hFile); 
    return(*pcbBuf); 
}
```



<span data-ttu-id="89d89-126">Die Funktion remoteclose schließt eine Datei auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="89d89-126">The function RemoteClose closes a file on the server.</span></span> <span data-ttu-id="89d89-127">Beachten Sie, dass die Serveranwendung dem Kontext Handle als Teil der Close-Funktion **null** zuweisen muss.</span><span class="sxs-lookup"><span data-stu-id="89d89-127">Note that the server application has to assign **NULL** to the context handle as part of the close function.</span></span> <span data-ttu-id="89d89-128">Dies kommuniziert mit dem Serverstub und der RPC-Lauf Zeit Bibliothek, dass das Kontext Handle gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="89d89-128">This communicates to the server stub and the RPC run-time library that the context handle has been deleted.</span></span> <span data-ttu-id="89d89-129">Andernfalls wird die Verbindung geöffnet, und schließlich wird eine Kontext Zusammenführung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="89d89-129">Otherwise, the connection will be kept open and eventually a context run-down will occur.</span></span>


```C++
void RemoteClose(PPCONTEXT_HANDLE_TYPE pphContext)
{
    FILE_CONTEXT_TYPE *pFileContext;
 
    if (*pphContext == NULL)
    {
        //Log error, client tried to close a NULL handle.
        return;
    }
    pFileContext = (FILE_CONTEXT_TYPE *)*pphContext;
    printf("File %s closed.\n", pFileContext->achFile);
    fclose(pFileConext->hFile);
    MIDL_user_free(pFileContext);
 
    // This tells the run-time, when it is marshalling the out 
    // parameters, that the context handle has been closed normally.
    *pphContext = NULL;
}
```



> [!Note]  
> <span data-ttu-id="89d89-130">Es wird erwartet, dass der Client ein gültiges Kontext Handle an einen Aufruf mit \[ in-, out- \] direktionalen Attributen übergibt, dass RPC keine **null** -Kontext Handles für diese Kombination aus direktionalen Attributen ablehnt.</span><span class="sxs-lookup"><span data-stu-id="89d89-130">While it is expected the client passes a valid context handle to a call with \[in, out\] directional attributes, RPC does not reject **NULL** context handles for this combination of directional attributes.</span></span> <span data-ttu-id="89d89-131">Das **null** -Kontext Handle wird als **null** -Zeiger an den Server übermittelt.</span><span class="sxs-lookup"><span data-stu-id="89d89-131">The **NULL** context handle is passed to the server as a **NULL** pointer.</span></span> <span data-ttu-id="89d89-132">Der Servercode für Aufrufe, die ein \[ in-, out- \] Kontext Handle enthalten, sollte geschrieben werden, um eine Zugriffsverletzung beim Empfang eines **null** -Zeigers zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="89d89-132">The server code for calls containing an \[in, out\] context handle should be written to avoid an access violation when a **NULL** pointer is received.</span></span>

 

 

 




