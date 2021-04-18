---
title: Beispiele (RPC)
description: Beispiele zur Veranschaulichung von RPC-Konzepten (Remote Prozedur Aufruf).
ms.assetid: d5db3085-6df0-4539-a605-d60055f4f4ec
keywords:
- Remote Prozedur Aufruf RPC, Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e6a814d78afbfc7fefa979c890cbbb8c3d4ce0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106340745"
---
# <a name="examples-rpc"></a><span data-ttu-id="efd9a-104">Beispiele (RPC)</span><span class="sxs-lookup"><span data-stu-id="efd9a-104">Examples (RPC)</span></span>

<span data-ttu-id="efd9a-105">Das Platform Software Development Kit (SDK) enthält Beispiele, die eine Vielzahl von Remote Prozedur Aufruf-Konzepten (RPC) veranschaulichen, wie im folgenden dargestellt:</span><span class="sxs-lookup"><span data-stu-id="efd9a-105">The Platform Software Development Kit (SDK) includes examples that demonstrate a variety of Remote Procedure Call (RPC) concepts, as follows:</span></span>

-   <span data-ttu-id="efd9a-106">Asyncrpc veranschaulicht die Struktur einer RPC-Anwendung, die asynchrone Remote Prozedur Aufrufe verwendet.</span><span class="sxs-lookup"><span data-stu-id="efd9a-106">ASYNCRPC illustrates the structure of an RPC application that uses asynchronous remote procedure calls.</span></span> <span data-ttu-id="efd9a-107">Außerdem werden verschiedene Benachrichtigungs Methoden für den Abschluss des Aufrufes veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="efd9a-107">It also demonstrates various methods of notification of the call's completion.</span></span>
-   <span data-ttu-id="efd9a-108">Cluuid veranschaulicht die Verwendung der Client-Objekt-UUID, um es einem Client zu ermöglichen, aus mehreren Implementierungen einer Remote Prozedur auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="efd9a-108">CLUUID demonstrates use of the client-object UUID to enable a client to select from multiple implementations of a remote procedure.</span></span>
-   <span data-ttu-id="efd9a-109">Das Datenverzeichnis enthält vier Programme: dunion veranschaulicht diskriminierte (nicht gekapselte) Unions; "INOUT" veranschaulicht [ \[ in \] ](../midl/in.md)-, [ \[ out \] ](../midl/out-idl.md) -Parameter; Repas zeigt die [Darstellung \_ als](/windows/desktop/Midl/represent-as) Attribut an. Xmit veranschaulicht das über [tragen \_ als](/windows/desktop/Midl/transmit-as) -Attribut.</span><span class="sxs-lookup"><span data-stu-id="efd9a-109">DATA directory contains four programs: DUNION illustrates discriminated (nonencapsulated) unions; INOUT demonstrates [\[in\]](../midl/in.md), [\[out\]](../midl/out-idl.md) parameters; REPAS demonstrates the [represent\_as](/windows/desktop/Midl/represent-as) attribute; XMIT demonstrates the [transmit\_as](/windows/desktop/Midl/transmit-as) attribute.</span></span>
-   <span data-ttu-id="efd9a-110">Dynetpt veranschaulicht, wie eine Client Anwendung über dynamische Endpunkte eine Verbindung mit dem Server verwaltet.</span><span class="sxs-lookup"><span data-stu-id="efd9a-110">DYNEPT demonstrates a client application managing its connection to the server through dynamic endpoints.</span></span>
-   <span data-ttu-id="efd9a-111">Das Verzeichnis filerep enthält vier Beispiele, die veranschaulichen, wie Entwickler einen einfachen Datei Replikations Dienst, einen Datei Replikations Dienst für mehrere Benutzer, einen Dienst zur Unterstützung von Sicherheitsfunktionen und einen Dienst mit asynchronen RPC-Pipes schreiben können.</span><span class="sxs-lookup"><span data-stu-id="efd9a-111">FILEREP directory contains four samples illustrating how developers can write a simple file replication service, a multi-user file replication service, a service supporting security features, and a service using RPC asynchronous pipes.</span></span>
-   <span data-ttu-id="efd9a-112">Das Handles-Verzeichnis enthält die drei Programme Auto, cxhndl, rdef, die die [automatische \_ Handhabung](/windows/desktop/Midl/auto-handle), das \[ Kontext \_ handle \] und generische (benutzerdefinierte) Handles veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="efd9a-112">HANDLES directory contains three programs, AUTO, CXHNDL, USRDEF, which demonstrate [auto\_handle](/windows/desktop/Midl/auto-handle), \[context\_handle\], and generic (user-defined) handles, respectively.</span></span>
-   <span data-ttu-id="efd9a-113">Hello ist eine Client/Server-Implementierung von "Hello, World".</span><span class="sxs-lookup"><span data-stu-id="efd9a-113">HELLO is a client/server implementation of "Hello, world."</span></span>
-   <span data-ttu-id="efd9a-114">Das Pickle-Verzeichnis enthält zwei Programme: picklp veranschaulicht die Serialisierung von Daten Prozeduren. Picklt veranschaulicht die Serialisierung des Datentyps. Beide Programme verwenden die Attribute [ \[ Codieren \] ](../midl/encode.md) und [ \[ decodieren \] ](../midl/decode.md) .</span><span class="sxs-lookup"><span data-stu-id="efd9a-114">PICKLE directory contains two programs: PICKLP demonstrates data procedure serialization; PICKLT demonstrates data type serialization; both programs use the [\[encode\]](../midl/encode.md) and [\[decode\]](../midl/decode.md) attributes.</span></span>
-   <span data-ttu-id="efd9a-115">Pipes veranschaulicht die Verwendung des pipetypkonstruktors.</span><span class="sxs-lookup"><span data-stu-id="efd9a-115">PIPES demonstrates the use of the pipe-type constructor.</span></span>
-   <span data-ttu-id="efd9a-116">Rpcsvc veranschaulicht die Implementierung eines Dienstanbieter mit RPC.</span><span class="sxs-lookup"><span data-stu-id="efd9a-116">RPCSVC demonstrates the implementation of a service with RPC.</span></span>
-   <span data-ttu-id="efd9a-117">StrOut veranschaulicht, wie Arbeitsspeicher auf einem Server für ein zweidimensionales Objekt (ein Array von Zeigern) belegt und als \[ nur-Out-Parameter an den Client zurückgegeben wird \] .</span><span class="sxs-lookup"><span data-stu-id="efd9a-117">STROUT demonstrates how to allocate memory at a server for a two-dimensional object (an array of pointers) and pass it back to the client as an \[out\]-only parameter.</span></span> <span data-ttu-id="efd9a-118">Der Client gibt dann den Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="efd9a-118">The client then frees the memory.</span></span> <span data-ttu-id="efd9a-119">Diese Technik ermöglicht es dem Stub, den Server aufzurufen, ohne im Voraus zu wissen, wie viele Daten zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="efd9a-119">This technique allows the stub to call the server without knowing in advance how much data will be returned.</span></span>

    <span data-ttu-id="efd9a-120">Dieses Programm ermöglicht es dem Benutzer auch, für Unicode oder ANSI zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="efd9a-120">This program also allows the user to compile either for UNICODE or ANSI.</span></span>

<span data-ttu-id="efd9a-121">Alle Quelldateien und Makefiles für diese Programme befinden sich im Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="efd9a-121">All of the source files and makefiles for these programs are located in the Platform SDK.</span></span>

<span data-ttu-id="efd9a-122">Informationen zur grundlegenden Entwicklung von RPC-Anwendungen und einfacheren Beispielen finden Sie in den Themen zum [Tutorial](tutorial.md) .</span><span class="sxs-lookup"><span data-stu-id="efd9a-122">For basic RPC application development and simpler examples, please see the [Tutorial](tutorial.md) topics.</span></span>

 

 
