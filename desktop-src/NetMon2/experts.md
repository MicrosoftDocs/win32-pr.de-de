---
description: Ein Experte ist eine Microsoft Win32-DLL (Dynamic-Link Library), die den Netzwerk Datenverkehr analysiert, der von einem Netzwerk Paketanbieter (NPP) erfasst und in einer Erfassungs Datei abgelegt wird.
ms.assetid: 57d8164e-f587-4bb9-a0b1-6094037e584c
title: Experte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf5fc0096b15d590bf70859443667f2d9969f1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340154"
---
# <a name="expert"></a><span data-ttu-id="06ea5-103">Experte</span><span class="sxs-lookup"><span data-stu-id="06ea5-103">Expert</span></span>

<span data-ttu-id="06ea5-104">Ein Experte ist eine Microsoft Win32-DLL (Dynamic-Link Library), die den Netzwerk Datenverkehr analysiert, der von einem [*Netzwerk Paketanbieter*](n.md) (NPP) erfasst und in einer Erfassungs Datei abgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="06ea5-104">An expert is a Microsoft Win32 dynamic-link library (DLL) that analyzes network traffic collected by a [*network packet provider*](n.md) (NPP), and placed in a capture file.</span></span> <span data-ttu-id="06ea5-105">Nachdem die Daten aufgezeichnet und in einer Erfassungs Datei gespeichert wurden, arbeitet der Experte mit einem Parser, der auch als Protokoll Parser bezeichnet wird, um die Daten in der Datei zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="06ea5-105">After the data is captured and stored in a capture file, the expert works with a parser, also referred to as a protocol parser, to analyze the data in the file.</span></span> <span data-ttu-id="06ea5-106">Beispielsweise können Sie die Frames der Erfassungs Datei überprüfen und einen [*Parser*](p.md) verwenden, um Protokolle wie SMB (Server Message Block) oder TCP/IP (Transmission Control Protocol/Internet Protocol) zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="06ea5-106">For example, you can examine the frames of the capture file and use a [*parser*](p.md) to recognize protocols such as server message block (SMB), or Transmission Control Protocol/Internet Protocol (TCP/IP).</span></span>

<span data-ttu-id="06ea5-107">Sie können einen Experten so entwerfen, dass er mit allen Netzwerkmonitor Parser und sämtlichen Parser arbeitet, die Sie selbst erstellen.</span><span class="sxs-lookup"><span data-stu-id="06ea5-107">You can design an expert to work with all of the Network Monitor parsers, and any parsers that you create yourself.</span></span>

<span data-ttu-id="06ea5-108">Nachdem eine angeforderte Entsprechung von Protokollen einen bestimmten Frame identifiziert hat, extrahiert der Experte Daten aus dem Frame.</span><span class="sxs-lookup"><span data-stu-id="06ea5-108">After a requested match of protocols identifies a specific frame, the expert extracts data from the frame.</span></span> <span data-ttu-id="06ea5-109">Sie können den Experten programmieren, um Informationen in nutzbare Daten zu bearbeiten, die in der Netzwerkmonitor Ereignisanzeige angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="06ea5-109">You can program the expert to manipulate information into usable data that the Network Monitor Event Viewer displays.</span></span>

<span data-ttu-id="06ea5-110">Sie können einen Experten zur Laufzeit konfigurieren und dann Netzwerkmonitor verwenden, um die Benutzer Konfigurationsdaten für die Wiederverwendung mit unterschiedlichen Erfassungs Dateien zu speichern.</span><span class="sxs-lookup"><span data-stu-id="06ea5-110">You can configure an expert at run time, and then use Network Monitor to save user configuration data for reuse with different capture files.</span></span> <span data-ttu-id="06ea5-111">Sie können einen Experten verwenden, um Korrelations Daten und benutzerdefinierte Lösungen für Endbenutzer bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="06ea5-111">You can use an expert to provide correlation data and custom resolutions for end users.</span></span> <span data-ttu-id="06ea5-112">Weitere Informationen zur Erstellung von HTML-basierten Konfigurationsinformationen finden Sie auf der [Seite mit der Ereignis Referenz](event-reference-page.md).</span><span class="sxs-lookup"><span data-stu-id="06ea5-112">For more information about the creation of HTML-based configuration information, see [Event Reference Page](event-reference-page.md).</span></span>

<span data-ttu-id="06ea5-113">Während der Netzwerkmonitor-Installation werden die folgenden Experten-DLLs im Unterverzeichnis für Experten installiert:</span><span class="sxs-lookup"><span data-stu-id="06ea5-113">During Network Monitor setup, the following expert DLLs are installed in the Experts sub-directory:</span></span>

-   <span data-ttu-id="06ea5-114">Coalesce.dll</span><span class="sxs-lookup"><span data-stu-id="06ea5-114">Coalesce.dll</span></span>
-   <span data-ttu-id="06ea5-115">Propdist.dll</span><span class="sxs-lookup"><span data-stu-id="06ea5-115">Propdist.dll</span></span>
-   <span data-ttu-id="06ea5-116">Protdist.dll</span><span class="sxs-lookup"><span data-stu-id="06ea5-116">Protdist.dll</span></span>
-   <span data-ttu-id="06ea5-117">Resptime.dll</span><span class="sxs-lookup"><span data-stu-id="06ea5-117">Resptime.dll</span></span>
-   <span data-ttu-id="06ea5-118">Tcpipe.dll</span><span class="sxs-lookup"><span data-stu-id="06ea5-118">Tcpipe.dll</span></span>
-   <span data-ttu-id="06ea5-119">Topuser.dll</span><span class="sxs-lookup"><span data-stu-id="06ea5-119">Topuser.dll</span></span>

<span data-ttu-id="06ea5-120">Wenn Sie Netzwerkmonitor starten, erstellt die [**DllMain**](dllmain-expert.md) -Funktion alle Experten im Unterverzeichnis "Experten".</span><span class="sxs-lookup"><span data-stu-id="06ea5-120">When you start Network Monitor, the [**DllMain**](dllmain-expert.md) function builds all experts in the experts subdirectory.</span></span> <span data-ttu-id="06ea5-121">Wenn der Benutzer **im Menü Extras der Netzwerkmonitor** -Benutzeroberfläche auf **Experten** klickt, lädt Netzwerkmonitor die Experten-DLLs.</span><span class="sxs-lookup"><span data-stu-id="06ea5-121">When the user selects **Experts** on the **Tools** menu of the Network Monitor UI, Network Monitor loads the expert DLLs.</span></span> <span data-ttu-id="06ea5-122">Der Experte wird über den Einstiegspunkt " [Register Expert](register-expert.md) " aufgerufen, um grundlegende Details zum Experten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="06ea5-122">The expert is called through the [Register Expert](register-expert.md) entry point to provide basic details about the expert.</span></span>

![Dialogfeld "Experten für Netzwerküberwachung"](images/expick.png)

<span data-ttu-id="06ea5-124">Netzwerkmonitor die folgenden Funktionen zum Verwalten des Experten aufruft:</span><span class="sxs-lookup"><span data-stu-id="06ea5-124">Network Monitor calls the following functions to manage the expert:</span></span>

-   [<span data-ttu-id="06ea5-125">**DllMain**</span><span class="sxs-lookup"><span data-stu-id="06ea5-125">**DllMain**</span></span>](dllmain-expert.md)
-   [<span data-ttu-id="06ea5-126">**Experte registrieren**</span><span class="sxs-lookup"><span data-stu-id="06ea5-126">**Register Expert**</span></span>](register-expert.md)
-   [<span data-ttu-id="06ea5-127">**Ausführen**</span><span class="sxs-lookup"><span data-stu-id="06ea5-127">**Run**</span></span>](run.md)
-   [<span data-ttu-id="06ea5-128">**Konfigurieren**</span><span class="sxs-lookup"><span data-stu-id="06ea5-128">**Configure**</span></span>](configure.md)

<span data-ttu-id="06ea5-129">Der Experte muss jede der vorangehenden Funktionen implementieren.</span><span class="sxs-lookup"><span data-stu-id="06ea5-129">The expert must implement each of the preceding functions.</span></span>

 

 



