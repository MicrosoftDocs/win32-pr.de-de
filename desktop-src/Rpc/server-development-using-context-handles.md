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
# <a name="server-development-using-context-handles"></a>Server Entwicklung mithilfe von Kontext Handles

Aus Sicht der Serverprogramm Entwicklung ist ein Kontext Handle ein nicht typisierter Zeiger. Server Programme initialisieren Kontext Handles, indem Sie Sie auf Daten im Arbeitsspeicher oder in einer anderen Form von Speicher (z. b. Dateien auf Datenträgern) verweisen.

Nehmen wir beispielsweise an, dass ein Client ein Kontext Handle verwendet, um eine Reihe von Updates für einen Datensatz in einer Datenbank anzufordern. Der Client ruft eine Remote Prozedur auf dem Server auf und übergibt ihm einen Suchschlüssel. Das Serverprogramm sucht in der Datenbank nach dem Suchschlüssel und ruft die ganzzahlige Datensatznummer des übereinstimmenden Datensatzes ab. Der Server kann dann einen Zeiger auf den Speicherort, der die Datensatznummer enthält, auf "void" zeigen. Wenn der Wert zurückgegeben wird, muss die Remote Prozedur den Zeiger als Kontext Handle über seinen Rückgabewert oder seine Parameterliste zurückgeben. Der Client müsste den Zeiger an den Server übergeben, wenn er Remote Prozeduren zum Aktualisieren des Datensatzes aufgerufen hat. Während jedes dieser Aktualisierungs Vorgänge wandelt der Server den void-Zeiger in einen Zeiger auf eine Ganzzahl um.

Nachdem das Serverprogramm das Kontext Handle auf Kontext Daten verweist, gilt das Handle als geöffnet. Handles, die einen **null** -Wert enthalten, werden geschlossen. Der Server verwaltet ein geöffnetes Kontext Handle, bis der Client eine Remote Prozedur aufruft, die ihn schließt. Wenn die Client Sitzung beendet wird, während das Handle geöffnet ist, ruft die RPC-Laufzeit die Server-Lauf Zeit Routine auf, um das Handle freizugeben.

Das folgende Code Fragment veranschaulicht, wie ein-Server ein Kontext Handle implementieren kann. In diesem Beispiel verwaltet der Server eine Datendatei, in die der Client mithilfe von Remote Prozeduren schreibt. Die Kontextinformationen sind ein Datei Handle, das den aktuellen Speicherort in der Datei nachverfolgt, an der der Serverdaten schreibt. Das Datei Handle wird als Kontext Handle in der Parameterliste für Remote Prozedur Aufrufe verpackt. Eine-Struktur enthält den Dateinamen und das Datei handle. Die Schnittstellen Definition für dieses Beispiel wird unter [Schnittstellen Entwicklung mithilfe von Kontext Handles](interface-development-using-context-handles.md)gezeigt.


```C++
/* cxhndlp.c (fragment of file containing remote procedures) */
typedef struct 
{
     FILE* hFile;
     char   achFile[256];
} FILE_CONTEXT_TYPE;
```



Die Funktion remoteopen öffnet eine Datei auf dem Server:


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



Die Funktion RemoteRead liest eine Datei auf dem Server.


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



Die Funktion remoteclose schließt eine Datei auf dem Server. Beachten Sie, dass die Serveranwendung dem Kontext Handle als Teil der Close-Funktion **null** zuweisen muss. Dies kommuniziert mit dem Serverstub und der RPC-Lauf Zeit Bibliothek, dass das Kontext Handle gelöscht wurde. Andernfalls wird die Verbindung geöffnet, und schließlich wird eine Kontext Zusammenführung ausgeführt.


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
> Es wird erwartet, dass der Client ein gültiges Kontext Handle an einen Aufruf mit \[ in-, out- \] direktionalen Attributen übergibt, dass RPC keine **null** -Kontext Handles für diese Kombination aus direktionalen Attributen ablehnt. Das **null** -Kontext Handle wird als **null** -Zeiger an den Server übermittelt. Der Servercode für Aufrufe, die ein \[ in-, out- \] Kontext Handle enthalten, sollte geschrieben werden, um eine Zugriffsverletzung beim Empfang eines **null** -Zeigers zu vermeiden.

 

 

 




