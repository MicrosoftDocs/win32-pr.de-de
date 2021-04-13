---
title: Definieren von Pipes in IDL-Dateien
description: Wenn eine Pipe in einer IDL-Datei definiert ist, generiert der Mittelwert Compiler eine Pipe-Steuerungsstruktur, deren Member Zeiger auf Push-, Pull-und Zuordnungs Prozeduren sowie eine Zustands Variable sind, die diese Prozeduren koordiniert.
ms.assetid: f6c282e4-3056-48c4-bd12-dfcae6d238d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 115be7fc5d00458d13df102afebe9ba5b55de070
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390686"
---
# <a name="defining-pipes-in-idl-files"></a><span data-ttu-id="c80ed-103">Definieren von Pipes in IDL-Dateien</span><span class="sxs-lookup"><span data-stu-id="c80ed-103">Defining Pipes in IDL Files</span></span>

<span data-ttu-id="c80ed-104">Wenn eine Pipe in einer IDL-Datei definiert ist, generiert der Mittelwert Compiler eine Pipe-Steuerungsstruktur, deren Member Zeiger auf Push-, Pull-und Zuordnungs Prozeduren sowie eine Zustands Variable sind, die diese Prozeduren koordiniert.</span><span class="sxs-lookup"><span data-stu-id="c80ed-104">When a pipe is defined in an IDL file, the MIDL compiler generates a pipe control structure whose members are pointers to push, pull, and alloc procedures as well as a state variable that coordinates these procedures.</span></span> <span data-ttu-id="c80ed-105">Die Client Anwendung initialisiert die Felder in der Pipe-Steuerelement Struktur, behält deren Zustands Variable bei und verwaltet die Datenübertragung mit eigenen Push-, Pull-und Zuordnungsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="c80ed-105">The client application initializes the fields in the pipe control structure, maintains its state variable, and manages the data transfer with its own push, pull, and alloc functions.</span></span> <span data-ttu-id="c80ed-106">Der Client-Stub-Code ruft diese Anwendungsfunktionen während der Datenübertragung in Schleifen auf.</span><span class="sxs-lookup"><span data-stu-id="c80ed-106">The client stub code calls these application functions in loops during data transfer.</span></span> <span data-ttu-id="c80ed-107">Bei einer Eingabe Pipe marshunscht der Clientstub die Übertragungsdaten und überträgt sie an den Serverstub.</span><span class="sxs-lookup"><span data-stu-id="c80ed-107">For an input pipe, the client stub marshals the transfer data and transmits it to the server stub.</span></span> <span data-ttu-id="c80ed-108">Bei einer Ausgabe Pipe werden die Daten vom Clientstub in einen Puffer entmarshunpliziert, und ein Zeiger an den Puffer wird an die Client Anwendung zurückgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c80ed-108">For an output pipe, the client stub unmarshals the data into a buffer and passes a pointer to that buffer back to the client application.</span></span>

<span data-ttu-id="c80ed-109">Der Server-Stub-Code initialisiert die Felder der Pipe-Steuerelement Struktur mit einer Statusvariablen sowie Zeiger auf Push-und Pull-Routinen.</span><span class="sxs-lookup"><span data-stu-id="c80ed-109">The server stub code initializes the fields of the pipe control structure to a state variable, as well as pointers to push and pull routines.</span></span> <span data-ttu-id="c80ed-110">Der Server-Stub verwaltet den Status und verwaltet seinen privaten Speicher für die Übertragungsdaten.</span><span class="sxs-lookup"><span data-stu-id="c80ed-110">The server stub maintains the state and manages its private storage for the transfer data.</span></span> <span data-ttu-id="c80ed-111">Die Serveranwendung ruft während des Remote Prozedur Aufrufs die Pull-und pushroutinen in Schleifen auf, da Sie Daten vom Clientstub empfängt und abmarshalls oder Daten an den Client-Stub überträgt.</span><span class="sxs-lookup"><span data-stu-id="c80ed-111">The server application calls the pull and push routines in loops during the remote procedure call as it receives and unmarshals data from the client stub, or marshals and transmits data to the client stub.</span></span>

<span data-ttu-id="c80ed-112">Die folgende Beispiel-IDL-Datei definiert eine lange Pipe des pipetyps \_ , deren Elementgröße als **Long**-Wert definiert ist.</span><span class="sxs-lookup"><span data-stu-id="c80ed-112">The following example IDL file defines a pipe type LONG\_PIPE, whose element size is defined as **long**.</span></span> <span data-ttu-id="c80ed-113">Außerdem werden Funktionsprototypen für die Remote Prozedur Aufrufe von inpipe und outpipe zum Senden bzw. empfangen von Daten deklariert.</span><span class="sxs-lookup"><span data-stu-id="c80ed-113">It also declares function prototypes for the remote procedure calls InPipe and OutPipe, to send and receive data, respectively.</span></span> <span data-ttu-id="c80ed-114">Wenn der Mittell-Compiler die IDL-Datei verarbeitet, generiert er die im Beispiel gezeigte Header Datei.</span><span class="sxs-lookup"><span data-stu-id="c80ed-114">When the MIDL compiler processes the IDL file, it generates the header file shown in the example.</span></span>

## <a name="example"></a><span data-ttu-id="c80ed-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c80ed-115">Example</span></span>

``` syntax
// File: pipedemo.idl
typedef pipe long LONG_PIPE;
void InPipe( [in] LONG_PIPE pipe_data );
void OutPipe( [out] LONG_PIPE *pipe_data ); 
//end pipedemo.idl
 
// File: pipedemo.h (fragment)
// Generated by the MIDL compiler from pipedemo.idl
typedef struct pipe_LONG_PIPE
{
    void (__RPC_FAR * pull) (
        char __RPC_FAR * state,
        long __RPC_FAR * buf,
        unsigned long esize,
        unsigned long __RPC_FAR * ecount );
    void (__RPC_FAR * push) (
        char __RPC_FAR * state,
        long __RPC_FAR * buf,
        unsigned long ecount );
    void (__RPC_FAR * alloc) (
        char __RPC_FAR * state,
        unsigned long bsize,
        long __RPC_FAR * __RPC_FAR * buf,
        unsigned long __RPC_FAR * bcount );
    char __RPC_FAR * state;
} LONG_PIPE;
 
void InPipe( 
    /* [in] */ LONG_PIPE pipe_data);
void OutPipe( 
    /* [out] */ LONG_PIPE __RPC_FAR *pipe_data);
//end pipedemo.h
```

## <a name="related-topics"></a><span data-ttu-id="c80ed-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c80ed-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c80ed-117">Kanal</span><span class="sxs-lookup"><span data-stu-id="c80ed-117">pipe</span></span>](/windows/desktop/Midl/pipe)
</dt> <dt>

[<span data-ttu-id="c80ed-118">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="c80ed-118">**/Oi**</span></span>](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 