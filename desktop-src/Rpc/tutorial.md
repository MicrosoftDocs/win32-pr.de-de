---
title: Tutorial
description: Dieses Tutorial führt Sie durch die Schritte, die erforderlich sind, um eine einfache verteilte Anwendung mit einem einzelnen Client aus einer vorhandenen eigenständigen Anwendung zu erstellen.
ms.assetid: afdfa037-58c0-4dcf-aa27-6839db0515e6
keywords:
- Remote Prozedur Aufruf RPC, Tutorial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c19b0d8ec3b3eb55cf29ccfd87eca43775c2ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037327"
---
# <a name="tutorial"></a><span data-ttu-id="974fb-104">Tutorial</span><span class="sxs-lookup"><span data-stu-id="974fb-104">Tutorial</span></span>

<span data-ttu-id="974fb-105">Dieses Tutorial führt Sie durch die Schritte, die erforderlich sind, um eine einfache verteilte Anwendung mit einem einzelnen Client aus einer vorhandenen eigenständigen Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="974fb-105">This tutorial takes you through the steps required to create a simple, single-client, single-server distributed application from an existing standalone application.</span></span> <span data-ttu-id="974fb-106">Diese Schritte sind die folgenden:</span><span class="sxs-lookup"><span data-stu-id="974fb-106">These steps are:</span></span>

-   <span data-ttu-id="974fb-107">Erstellen Sie Schnittstellendefinitionen und Anwendungs Konfigurationsdateien.</span><span class="sxs-lookup"><span data-stu-id="974fb-107">Create interface definition and application configuration files.</span></span>
-   <span data-ttu-id="974fb-108">Verwenden Sie den-compilercompiler zum Generieren von Client-und Serverstub und-Headern in C-Sprache aus diesen Dateien.</span><span class="sxs-lookup"><span data-stu-id="974fb-108">Use the MIDL compiler to generate C-language client and server stubs and headers from those files.</span></span>
-   <span data-ttu-id="974fb-109">Schreiben Sie eine Client Anwendung, die die Verbindung mit dem Server verwaltet.</span><span class="sxs-lookup"><span data-stu-id="974fb-109">Write a client application that manages its connection to the server.</span></span>
-   <span data-ttu-id="974fb-110">Schreiben Sie eine Serveranwendung, die die eigentlichen Remote Prozeduren enthält.</span><span class="sxs-lookup"><span data-stu-id="974fb-110">Write a server application that contains the actual remote procedures.</span></span>
-   <span data-ttu-id="974fb-111">Kompilieren Sie diese Dateien, und verknüpfen Sie Sie mit der RPC-Lauf Zeit Bibliothek, um die verteilte Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="974fb-111">Compile and link these files to the RPC run-time library to produce the distributed application.</span></span>

<span data-ttu-id="974fb-112">Die Client Anwendung übergibt eine Zeichenfolge in einem Remote Prozedur Aufrufer an den Server, und der Server gibt die Zeichenfolge "Hello, World" in die Standardausgabe aus.</span><span class="sxs-lookup"><span data-stu-id="974fb-112">The client application passes a character string to the server in a remote procedure call, and the server prints the string "Hello, World" to its standard output.</span></span>

<span data-ttu-id="974fb-113">Die gesamten Quelldateien für diese Beispielanwendung mit zusätzlichem Code zum Behandeln der Befehlszeilen Eingabe und zum ausgeben verschiedener Statusmeldungen an den Benutzer finden Sie im \\ Verzeichnis "Hello Hello" des Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="974fb-113">The complete source files for this example application, with additional code to handle command-line input and to output various status messages to the user, are in the RPC\\Hello directory of the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="974fb-114">In diesem Abschnitt werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="974fb-114">This section presents its discussion in the following topics:</span></span>

-   [<span data-ttu-id="974fb-115">Die eigenständige Anwendung</span><span class="sxs-lookup"><span data-stu-id="974fb-115">The Standalone Application</span></span>](the-standalone-application.md)
-   [<span data-ttu-id="974fb-116">Definieren der Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="974fb-116">Defining the Interface</span></span>](defining-the-interface.md)
-   [<span data-ttu-id="974fb-117">Die UUID wird erzeugt.</span><span class="sxs-lookup"><span data-stu-id="974fb-117">Generating the UUID</span></span>](generating-the-uuid.md)
-   [<span data-ttu-id="974fb-118">Die IDL-Datei</span><span class="sxs-lookup"><span data-stu-id="974fb-118">The IDL File</span></span>](the-idl-file.md)
-   [<span data-ttu-id="974fb-119">Die ACF-Datei</span><span class="sxs-lookup"><span data-stu-id="974fb-119">The ACF File</span></span>](the-acf-file.md)
-   [<span data-ttu-id="974fb-120">Erstellen der Stubdateien</span><span class="sxs-lookup"><span data-stu-id="974fb-120">Generating the Stub Files</span></span>](generating-the-stub-files.md)
-   [<span data-ttu-id="974fb-121">Die Client Anwendung</span><span class="sxs-lookup"><span data-stu-id="974fb-121">The Client Application</span></span>](the-client-application.md)
-   [<span data-ttu-id="974fb-122">Die Server Anwendung</span><span class="sxs-lookup"><span data-stu-id="974fb-122">The Server Application</span></span>](the-server-application.md)
-   [<span data-ttu-id="974fb-123">Beenden der Server Anwendung</span><span class="sxs-lookup"><span data-stu-id="974fb-123">Stopping the Server Application</span></span>](stopping-the-server-application.md)
-   [<span data-ttu-id="974fb-124">Kompilieren und verknüpfen</span><span class="sxs-lookup"><span data-stu-id="974fb-124">Compiling and Linking</span></span>](compiling-and-linking.md)
-   [<span data-ttu-id="974fb-125">Ausführen der Anwendung</span><span class="sxs-lookup"><span data-stu-id="974fb-125">Running the Application</span></span>](running-the-application.md)

 

 




