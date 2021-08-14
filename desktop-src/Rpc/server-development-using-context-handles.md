---
title: Serverentwicklung mit Kontexthandles
description: Aus Der Perspektive der Serverprogrammentwicklung ist ein Kontexthandle ein nicht typischer Zeiger. Serverprogramme initialisieren Kontexthandles, indem sie auf Daten im Arbeitsspeicher oder auf eine andere Form von Speicher verweisen (z. B. Dateien auf Datenträgern).
ms.assetid: 6a1aabca-4cb9-401c-90c7-0cff7a69b7b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db05441f7314fba628d1ec07db5f99266c595c84e672ada976b38f7576ab5d1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925336"
---
# <a name="server-development-using-context-handles"></a>Serverentwicklung mit Kontexthandles

Aus Der Perspektive der Serverprogrammentwicklung ist ein Kontexthandle ein nicht typischer Zeiger. Serverprogramme initialisieren Kontexthandles, indem sie auf Daten im Arbeitsspeicher oder auf eine andere Form von Speicher verweisen (z. B. Dateien auf Datenträgern).

Angenommen, ein Client verwendet ein Kontexthandle, um eine Reihe von Updates für einen Datensatz in einer Datenbank anzufordern. Der Client ruft eine Remoteprozedur auf dem Server auf und übergibt ihr einen Suchschlüssel. Das Serverprogramm durchsucht die Datenbank nach dem Suchschlüssel und ruft die ganzzahlige Datensatznummer des übereinstimmenden Datensatzes ab. Der Server kann dann einen Zeiger auf void an einer Speicherposition zeigen, die die Datensatznummer enthält. Nach der Rückgabe muss die Remoteprozedur den Zeiger als Kontexthandle über den Rückgabewert oder die Parameterliste zurückgeben. Der Client muss den Zeiger jedes Mal an den Server übergeben, wenn er Remoteprozeduren aufgerufen hat, um den Datensatz zu aktualisieren. Bei jedem dieser Aktualisierungsvorgänge würde der Server den void-Zeiger in einen Zeiger auf eine ganze Zahl umwerfen.

Nachdem das Serverprogramm das Kontexthandle auf Kontextdaten verweist, gilt das Handle als geöffnet. Handles, die einen **NULL-Wert** enthalten, werden geschlossen. Der Server verwaltet ein geöffnetes Kontexthandle, bis der Client eine Remoteprozedur aufruft, die sie schließt. Wenn die Clientsitzung beendet wird, während das Handle geöffnet ist, ruft die RPC-Laufzeit die Server-Run-Down-Routine auf, um das Handle frei zu machen.

Das folgende Codefragment veranschaulicht, wie ein Server ein Kontexthandle implementieren kann. In diesem Beispiel verwaltet der Server eine Datendatei, in die der Client mithilfe von Remoteprozeduren schreibt. Die Kontextinformationen sind ein Dateihandle, das den aktuellen Speicherort in der Datei nachverfolgt, an der der Server Daten schreibt. Das Dateihandle wird als Kontexthandle in der Parameterliste für Remoteprozeduraufrufe gepackt. Eine -Struktur enthält den Dateinamen und das Dateihandle. Die Schnittstellendefinition für dieses Beispiel wird unter [Schnittstellenentwicklung mit Kontexthandles](interface-development-using-context-handles.md)gezeigt.


```C++
/* cxhndlp.c (fragment of file containing remote procedures) */
typedef struct 
{
     FILE* hFile;
     char   achFile[256];
} FILE_CONTEXT_TYPE;
```



Die Funktion RemoteOpen öffnet eine Datei auf dem Server:


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



Die Funktion RemoteClose schließt eine Datei auf dem Server. Beachten Sie, dass die Serveranwendung dem Kontexthandle als Teil der Close-Funktion **NULL** zuweisen muss. Dadurch wird dem Serverstub und der RPC-Laufzeitbibliothek mitgeteilt, dass das Kontexthandle gelöscht wurde. Andernfalls bleibt die Verbindung geöffnet, und schließlich kommt es zu einem Kontextablauf.


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
> Es ist zwar zu erwarten, dass der Client ein gültiges Kontexthandle an einen Aufruf mit \[ in- und ausgehenden \] richtungsweisen Attributen übergibt, RPC lehnt **jedoch KEINE NULL-Kontexthandles** für diese Kombination von richtungsweisen Attributen ab. Das **NULL-Kontexthandle** wird als **NULL-Zeiger** an den Server übergeben. Der Servercode für Aufrufe, die ein \[ In-Out-Kontexthandle enthalten, \] sollte geschrieben werden, um eine Zugriffsverletzung zu vermeiden, wenn ein **NULL-Zeiger** empfangen wird.

 

 

 




