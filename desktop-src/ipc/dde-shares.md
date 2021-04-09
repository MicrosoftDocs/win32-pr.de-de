---
description: DDE-Freigaben sind eine Computer Ressource.
ms.assetid: 98d24300-52cc-4f0d-b74f-c58b823ac5f3
title: DDE-Freigaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 012c219897187c9e68b5b9e662b93678b77974c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865591"
---
# <a name="dde-shares"></a><span data-ttu-id="f87a1-103">DDE-Freigaben</span><span class="sxs-lookup"><span data-stu-id="f87a1-103">DDE Shares</span></span>

<span data-ttu-id="f87a1-104">\[Network DDE wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f87a1-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="f87a1-105">Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]</span><span class="sxs-lookup"><span data-stu-id="f87a1-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="f87a1-106">DDE-Freigaben sind eine Computer Ressource.</span><span class="sxs-lookup"><span data-stu-id="f87a1-106">DDE shares are a machine resource.</span></span> <span data-ttu-id="f87a1-107">Sie ähneln Dateifreigaben, da Sie verwendet werden, um den Zugriff auf eine Ressource zu steuern.</span><span class="sxs-lookup"><span data-stu-id="f87a1-107">They are similar to file shares because they are used to control access to a resource.</span></span> <span data-ttu-id="f87a1-108">Bei Dateifreigaben ist die Ressource eine Datei.</span><span class="sxs-lookup"><span data-stu-id="f87a1-108">With file shares, the resource is a file.</span></span> <span data-ttu-id="f87a1-109">Bei DDE-Freigaben werden die Daten dynamisch ausgetauscht.</span><span class="sxs-lookup"><span data-stu-id="f87a1-109">With DDE shares, the resource is dynamically exchanged data.</span></span> <span data-ttu-id="f87a1-110">Der Typ der ausgetauschten Daten wird von der Serveranwendung bestimmt, die die Daten bereitstellt, und der Client Anwendung, die die Daten anfordert.</span><span class="sxs-lookup"><span data-stu-id="f87a1-110">The type of data exchanged is determined by the server application that supplies the data and the client application that requests the data.</span></span>

<span data-ttu-id="f87a1-111">Der Server Ruft die [**nddeshareadd**](nddeshareadd.md) -Funktion auf, um die DDE-Freigabe zu erstellen, die im DDE Share Database Manager (DSDM) gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="f87a1-111">The server calls the [**NDdeShareAdd**](nddeshareadd.md) function to create the DDE share, which is stored in the DDE share database manager (DSDM).</span></span>

<span data-ttu-id="f87a1-112">Der Client startet die DDE-Konversation durch Herstellen einer Verbindung mit der DDE-Freigabe.</span><span class="sxs-lookup"><span data-stu-id="f87a1-112">The client starts the DDE conversation by connecting to the DDE share.</span></span> <span data-ttu-id="f87a1-113">Der Client muss die [**DDEInitialize**](/windows/win32/api/ddeml/nf-ddeml-ddeinitializea) -Funktion zum Initialisieren von Ddeml und zum Abrufen der [**ddeconnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) -Funktion zum Herstellen einer Verbindung mit der DDE-Freigabe aufruft.</span><span class="sxs-lookup"><span data-stu-id="f87a1-113">The client must call the [**DdeInitialize**](/windows/win32/api/ddeml/nf-ddeml-ddeinitializea) function to initialize DDEML and call the [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) function to connect to the DDE share.</span></span> <span data-ttu-id="f87a1-114">Im **ddeconnect** -Befehl gibt der Client den Dienstnamen wie folgt an:</span><span class="sxs-lookup"><span data-stu-id="f87a1-114">In the **DdeConnect** call, the client specifies the service name as follows:</span></span>

<span data-ttu-id="f87a1-115">\\\\*Computername* \\ Ndde $</span><span class="sxs-lookup"><span data-stu-id="f87a1-115">\\\\*ComputerName*\\NDDE$</span></span>

<span data-ttu-id="f87a1-116">Dabei steht *Computername* für den Namen des Computers, auf dem die Serveranwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f87a1-116">where *ComputerName* is the name of the computer running the server application.</span></span> <span data-ttu-id="f87a1-117">Der ndde $-Wert gibt an, dass das für [**ddeconnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) bereitgestellte Thema der DDE-Freigabe Name auf dem Remote Computer namens *Computername* ist.</span><span class="sxs-lookup"><span data-stu-id="f87a1-117">The NDDE$ indicates that the topic provided to [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) is the DDE share name on the remote computer named *ComputerName*.</span></span>

<span data-ttu-id="f87a1-118">Es gibt drei Typen von DDE-Freigaben: Alter Stil, neue Formatvorlage und statisch.</span><span class="sxs-lookup"><span data-stu-id="f87a1-118">There are three types of DDE shares: old style, new style, and static.</span></span> <span data-ttu-id="f87a1-119">Es ist typisch, nur den statischen Typ zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="f87a1-119">It is typical to support only the static type.</span></span> <span data-ttu-id="f87a1-120">Die Namen von statischen Freigaben verwenden die folgende Konvention: *ShareName*$.</span><span class="sxs-lookup"><span data-stu-id="f87a1-120">The names of static shares use the following convention: *ShareName*$.</span></span>

 

 
