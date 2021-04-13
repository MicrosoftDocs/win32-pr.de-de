---
description: Beschreibt den Vorgang eines Netzwerk-e/a-Vorgangs unter Windows.
ms.assetid: 72dc0c57-28ae-4289-bb0d-b399d294c126
title: Beschreibung eines Netzwerk-e/a-Vorgangs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371b72389554f1c3fa2ec43180b1a6e4c76dc012
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345799"
---
# <a name="description-of-a-network-io-operation"></a><span data-ttu-id="047f6-103">Beschreibung eines Netzwerk-e/a-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="047f6-103">Description of a Network I/O Operation</span></span>

<span data-ttu-id="047f6-104">In der folgenden Abbildung wird der Vorgang eines Netzwerk-e/a-Vorgangs unter Windows veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="047f6-104">The following figure illustrates the process of a network I/O operation under Windows.</span></span>

![Netzwerk-e/a-Vorgang unter Windows](images/fig4.png)

<span data-ttu-id="047f6-106">Wenn eine Anwendung eine Datei-e/a-Funktion aufruft, um auf eine Datei auf einem Remote Computer zuzugreifen, treten die folgenden Ereignisse auf:</span><span class="sxs-lookup"><span data-stu-id="047f6-106">When an application calls a file I/O function to access a file on a remote computer, the following events occur:</span></span>

-   <span data-ttu-id="047f6-107">Die e/a-Anforderung wird von einem [Netzwerkredirector](network-redirectors.md), auch als Redirector bezeichnet, auf dem lokalen Computer abgefangen.</span><span class="sxs-lookup"><span data-stu-id="047f6-107">The I/O request is intercepted by a [network redirector](network-redirectors.md), also referred to simply as a redirector, on the local computer.</span></span> <span data-ttu-id="047f6-108">Dies wird in der obigen Abbildung durch den voll tonpfeil zwischen der Anwendung und dem clientredirector dargestellt.</span><span class="sxs-lookup"><span data-stu-id="047f6-108">This is depicted in the preceding figure by the solid arrow between the application and the client redirector.</span></span>
-   <span data-ttu-id="047f6-109">Der Redirector erstellt ein Datenpaket, das alle Informationen über die Anforderung enthält, und sendet es an den Server, auf dem sich die Datei befindet.</span><span class="sxs-lookup"><span data-stu-id="047f6-109">The redirector constructs a data packet containing all of the information about the request, and sends it to the server where the file is located.</span></span> <span data-ttu-id="047f6-110">Dies wird in der obigen Abbildung durch den voll tonpfeil zwischen dem clientredirector und dem serverredirector dargestellt.</span><span class="sxs-lookup"><span data-stu-id="047f6-110">This is depicted in the preceding figure by the solid arrow between the client redirector and the server redirector.</span></span>
-   <span data-ttu-id="047f6-111">Der Redirector auf dem Server empfängt das Paket vom Client, authentifiziert den Zugriff auf die Datei, die für die e/a-Anforderung erforderlich ist, und führt bei der Authentifizierung die Anforderung im Auftrag des Clients aus.</span><span class="sxs-lookup"><span data-stu-id="047f6-111">The redirector on the server receives the packet from the client, authenticates the access to the file required by the I/O request, and, if authenticated, executes the request on behalf of the client.</span></span> <span data-ttu-id="047f6-112">Wenn dies nicht der Fall ist, wird an den Redirector auf dem Client ein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="047f6-112">If not, it returns an error code to the redirector on the client.</span></span> <span data-ttu-id="047f6-113">Dies wird in der obigen Abbildung durch den gekrümmten voll tonpfeil zwischen dem Server Redirector und der Datei dargestellt.</span><span class="sxs-lookup"><span data-stu-id="047f6-113">This is depicted in the preceding figure by the curved solid arrow between the server redirector and the file.</span></span>
-   <span data-ttu-id="047f6-114">Wenn die Anforderung ausgeführt wurde, sendet der Redirector auf dem Server alle Daten, die sich aus der e/a-Anforderung ergeben, sowie eine Erfolgs Benachrichtigung an den Redirector auf dem Client.</span><span class="sxs-lookup"><span data-stu-id="047f6-114">When the request has been executed, the redirector on the server sends any data resulting from the I/O request to the redirector on the client along with a success notification.</span></span> <span data-ttu-id="047f6-115">Dies wird in der obigen Abbildung durch den gepunkteten Pfeil zwischen dem Server und dem clientredirector dargestellt.</span><span class="sxs-lookup"><span data-stu-id="047f6-115">This is depicted in the preceding figure by the dotted arrow between the server and the client redirector.</span></span>
-   <span data-ttu-id="047f6-116">Der Redirector auf dem Client empfängt das Paket vom Server und übergibt die Daten im Paket zusammen mit einer Erfolgs Benachrichtigung an die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="047f6-116">The redirector on the client receives the packet from the server and passes the data in the packet to the application along with a success notification.</span></span> <span data-ttu-id="047f6-117">Dies wird in der obigen Abbildung durch den gepunkteten Pfeil zwischen dem clientredirector und der Anwendung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="047f6-117">This is depicted in the preceding figure by the dotted arrow between the client redirector and the application.</span></span>

<span data-ttu-id="047f6-118">Windows kann eine Vielzahl von Netzwerkprotokollen verwenden, um einen Netzwerk-e/a-Vorgang auszuführen, einschließlich der [Übersicht über das Microsoft SMB-Protokoll und CIFS-Protokoll](microsoft-smb-protocol-and-cifs-protocol-overview.md) und NFS.</span><span class="sxs-lookup"><span data-stu-id="047f6-118">Windows can use a variety of networking protocols to perform a network I/O operation, including [Microsoft SMB Protocol and CIFS Protocol Overview](microsoft-smb-protocol-and-cifs-protocol-overview.md) and NFS.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="047f6-119">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="047f6-119">In this section</span></span>



| <span data-ttu-id="047f6-120">Thema</span><span class="sxs-lookup"><span data-stu-id="047f6-120">Topic</span></span>                                                                                       | <span data-ttu-id="047f6-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="047f6-121">Description</span></span>                                                          |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="047f6-122">Unterschiede in lokalen und Netzwerk-e/a</span><span class="sxs-lookup"><span data-stu-id="047f6-122">Differences in Local and Network I/O</span></span>](differences-in-local-and-network-i-o.md)<br/> | <span data-ttu-id="047f6-123">Unterschiede zwischen lokalem e/a und Netzwerk-e/a unter Windows.</span><span class="sxs-lookup"><span data-stu-id="047f6-123">Differences between local I/O and network I/O on Windows.</span></span><br/> |
| [<span data-ttu-id="047f6-124">Netzwerkredirectors</span><span class="sxs-lookup"><span data-stu-id="047f6-124">Network Redirectors</span></span>](network-redirectors.md)<br/>                                   | <span data-ttu-id="047f6-125">Beschreibt die Funktionalität eines Netzwerkredirector.</span><span class="sxs-lookup"><span data-stu-id="047f6-125">Describes the functionality of a network redirector.</span></span><br/>      |



 

 

 




