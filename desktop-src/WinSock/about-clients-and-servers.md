---
description: 'Es gibt zwei unterschiedliche Arten von socketnetzwerkanwendungen: Server und Client.'
ms.assetid: 05e42384-1746-462d-82c7-8df848b4525e
title: Informationen zu Servern und Clients
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a951d23ba1c6ad4f0f5ffd1f674b056a36c3f8dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353072"
---
# <a name="about-servers-and-clients"></a><span data-ttu-id="af40c-103">Informationen zu Servern und Clients</span><span class="sxs-lookup"><span data-stu-id="af40c-103">About Servers and Clients</span></span>

<span data-ttu-id="af40c-104">Es gibt zwei unterschiedliche Arten von socketnetzwerkanwendungen: Server und Client.</span><span class="sxs-lookup"><span data-stu-id="af40c-104">There are two distinct types of socket network applications: Server and Client.</span></span>

<span data-ttu-id="af40c-105">Server und Clients haben unterschiedliche Verhaltensweisen. Daher ist der Prozess der Erstellung anders.</span><span class="sxs-lookup"><span data-stu-id="af40c-105">Servers and Clients have different behaviors; therefore, the process of creating them is different.</span></span> <span data-ttu-id="af40c-106">Im folgenden finden Sie das allgemeine Modell zum Erstellen eines TCP/IP-Streamingservers und-Clients.</span><span class="sxs-lookup"><span data-stu-id="af40c-106">What follows is the general model for creating a streaming TCP/IP Server and Client.</span></span>

## <a name="server"></a><span data-ttu-id="af40c-107">Server</span><span class="sxs-lookup"><span data-stu-id="af40c-107">Server</span></span>

1.  <span data-ttu-id="af40c-108">Initialisieren Sie Winsock.</span><span class="sxs-lookup"><span data-stu-id="af40c-108">Initialize Winsock.</span></span>
2.  <span data-ttu-id="af40c-109">Erstellen Sie einen Socket.</span><span class="sxs-lookup"><span data-stu-id="af40c-109">Create a socket.</span></span>
3.  <span data-ttu-id="af40c-110">Binden Sie den Socket.</span><span class="sxs-lookup"><span data-stu-id="af40c-110">Bind the socket.</span></span>
4.  <span data-ttu-id="af40c-111">Lauschen Sie an den Socket für einen Client.</span><span class="sxs-lookup"><span data-stu-id="af40c-111">Listen on the socket for a client.</span></span>
5.  <span data-ttu-id="af40c-112">Akzeptieren Sie eine Verbindung von einem Client.</span><span class="sxs-lookup"><span data-stu-id="af40c-112">Accept a connection from a client.</span></span>
6.  <span data-ttu-id="af40c-113">Empfangen und Senden von Daten.</span><span class="sxs-lookup"><span data-stu-id="af40c-113">Receive and send data.</span></span>
7.  <span data-ttu-id="af40c-114">Trennen.</span><span class="sxs-lookup"><span data-stu-id="af40c-114">Disconnect.</span></span>

## <a name="client"></a><span data-ttu-id="af40c-115">Client</span><span class="sxs-lookup"><span data-stu-id="af40c-115">Client</span></span>

1.  <span data-ttu-id="af40c-116">Initialisieren Sie Winsock.</span><span class="sxs-lookup"><span data-stu-id="af40c-116">Initialize Winsock.</span></span>
2.  <span data-ttu-id="af40c-117">Erstellen Sie einen Socket.</span><span class="sxs-lookup"><span data-stu-id="af40c-117">Create a socket.</span></span>
3.  <span data-ttu-id="af40c-118">Stellen Sie eine Verbindung mit dem Server her.</span><span class="sxs-lookup"><span data-stu-id="af40c-118">Connect to the server.</span></span>
4.  <span data-ttu-id="af40c-119">Senden und empfangen von Daten.</span><span class="sxs-lookup"><span data-stu-id="af40c-119">Send and receive data.</span></span>
5.  <span data-ttu-id="af40c-120">Trennen.</span><span class="sxs-lookup"><span data-stu-id="af40c-120">Disconnect.</span></span>

> [!Note]  
> <span data-ttu-id="af40c-121">Einige der Schritte sind für einen Client und einen Server identisch.</span><span class="sxs-lookup"><span data-stu-id="af40c-121">Some of the steps are the same for a client and a server.</span></span> <span data-ttu-id="af40c-122">Diese Schritte sind nahezu genau gleichermaßen implementiert.</span><span class="sxs-lookup"><span data-stu-id="af40c-122">These steps are implemented almost exactly alike.</span></span> <span data-ttu-id="af40c-123">Einige der Schritte in diesem Handbuch gelten speziell für den Typ der Anwendung, die erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="af40c-123">Some of the steps in this guide will be specific to the type of application being created.</span></span>

 

<span data-ttu-id="af40c-124">Erster Schritt: [Erstellen einer grundlegenden Winsock-Anwendung](creating-a-basic-winsock-application.md)</span><span class="sxs-lookup"><span data-stu-id="af40c-124">First Step: [Creating a Basic Winsock Application](creating-a-basic-winsock-application.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="af40c-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="af40c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af40c-126">Einstieg in Winsock</span><span class="sxs-lookup"><span data-stu-id="af40c-126">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> </dl>

 

 



