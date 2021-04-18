---
title: DVC-Implementierungs Details
description: Dieser Abschnitt enthält Informationen zum Schreiben eines Client Moduls für einen dynamischen virtuellen Kanal (DVC).
ms.assetid: 338556d9-e9a7-4926-a09c-8e2ce1627467
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 876722736a95b45918d8a5b9e229f4f9eda5840b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341227"
---
# <a name="dvc-implementation-details"></a><span data-ttu-id="c2fb7-103">DVC-Implementierungs Details</span><span class="sxs-lookup"><span data-stu-id="c2fb7-103">DVC Implementation Details</span></span>

<span data-ttu-id="c2fb7-104">Dieser Abschnitt enthält Informationen zum Schreiben eines Client Moduls für einen dynamischen virtuellen Kanal (DVC).</span><span class="sxs-lookup"><span data-stu-id="c2fb7-104">This section contains information about how to write a dynamic virtual channel (DVC) client module.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c2fb7-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c2fb7-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="c2fb7-106">Schreiben eines Client-DVC-Moduls</span><span class="sxs-lookup"><span data-stu-id="c2fb7-106">Writing a Client DVC Module</span></span>](writing-a-client-dvc-component.md)
</dt> <dd>

<span data-ttu-id="c2fb7-107">Zum Schreiben eines c#-Client Moduls (Dynamic Virtual Channel) müssen Sie zuerst ein Remotedesktopverbindung-Client-Plug-in (RDC) implementieren und registrieren.</span><span class="sxs-lookup"><span data-stu-id="c2fb7-107">To write a dynamic virtual channel (DVC) client module, you must first implement and register a Remote Desktop Connection (RDC) client plug-in.</span></span>

</dd> <dt>

[<span data-ttu-id="c2fb7-108">DVC-Plug-in-Registrierung</span><span class="sxs-lookup"><span data-stu-id="c2fb7-108">DVC plug-in registration</span></span>](dvc-plug-in-registration.md)
</dt> <dd>

<span data-ttu-id="c2fb7-109">Beschreibt die Syntax für den DVC (Dynamic Virtual Channel)-Plug-in-Eintrag für den Remotedesktopverbindung-Client (RDC).</span><span class="sxs-lookup"><span data-stu-id="c2fb7-109">Describes syntax for the dynamic virtual channel (DVC) plug-in entry for the Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="c2fb7-110">Starten eines DVC-Listener</span><span class="sxs-lookup"><span data-stu-id="c2fb7-110">Starting a DVC Listener</span></span>](starting-a-dvc-listener.md)
</dt> <dd>

<span data-ttu-id="c2fb7-111">Zum Herstellen einer erfolgreichen Verbindung zwischen zwei DVC-Modulen (Dynamic Virtual Channel), die auf dem-Client und-Server des-Remotedesktopverbindung (RDC) ausgeführt werden, muss ein DVC-Listener ausgeführt werden und sich in einem Empfangs Zustand befinden.</span><span class="sxs-lookup"><span data-stu-id="c2fb7-111">To establish a successful connection between two dynamic virtual channel (DVC) modules that are running on the Remote Desktop Connection (RDC) client and server, a DVC listener must be running and in a listening state.</span></span>

</dd> <dt>

[<span data-ttu-id="c2fb7-112">Akzeptieren einer Verbindung</span><span class="sxs-lookup"><span data-stu-id="c2fb7-112">Accepting a Connection</span></span>](accepting-a-connection.md)
</dt> <dd>

<span data-ttu-id="c2fb7-113">Zu einem bestimmten Zeitpunkt fordert der DVC-Client (Dynamic Virtual Channel) eine Verbindung mit dem DVC-Listener an.</span><span class="sxs-lookup"><span data-stu-id="c2fb7-113">At some point in time, the dynamic virtual channel (DVC) client will request a connection to the DVC listener.</span></span>

</dd> <dt>

[<span data-ttu-id="c2fb7-114">Schreiben von Daten mithilfe eines DVC-Kanals</span><span class="sxs-lookup"><span data-stu-id="c2fb7-114">Writing Data by Using a DVC Channel</span></span>](writing-data-by-using-a-dvc-channel.md)
</dt> <dd>

<span data-ttu-id="c2fb7-115">Das Schreiben von Kanaldaten mithilfe eines dynamischen virtuellen Kanals (DVC) ist sowohl für den Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server als auch für den Client symmetrisch.</span><span class="sxs-lookup"><span data-stu-id="c2fb7-115">Writing channel data by using a dynamic virtual channel (DVC) is symmetric for both the Remote Desktop Session Host (RD Session Host) server and the client.</span></span>

</dd> <dt>

[<span data-ttu-id="c2fb7-116">Testen und Debuggen</span><span class="sxs-lookup"><span data-stu-id="c2fb7-116">Testing and Debugging</span></span>](testing-and-debugging.md)
</dt> <dd>

<span data-ttu-id="c2fb7-117">Es gibt einen "Echo"-Listener, der vom RDC-Client (Remotedesktopverbindung) implementiert wird, der immer vorhanden ist und auf eingehende Verbindungen lauscht.</span><span class="sxs-lookup"><span data-stu-id="c2fb7-117">There is an "echo" listener that is implemented by the Remote Desktop Connection (RDC) client, which is always present and listening for incoming connections.</span></span>

</dd> <dt>

[<span data-ttu-id="c2fb7-118">Beispiel für DVC-Client-Plug-in</span><span class="sxs-lookup"><span data-stu-id="c2fb7-118">DVC Client Plug-in Example</span></span>](dvc-client-plug-in-example.md)
</dt> <dd>

<span data-ttu-id="c2fb7-119">C++-Codebeispiel, das veranschaulicht, wie Remotedesktopverbindung ein RDC-Client (Dynamic Virtual Channel)-Plug-in für Clients erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c2fb7-119">C++ code sample that shows how to create a Remote Desktop Connection (RDC) client dynamic virtual channel (DVC) plug-in.</span></span>

</dd> <dt>

[<span data-ttu-id="c2fb7-120">Beispiel für das DVC-Server Modul</span><span class="sxs-lookup"><span data-stu-id="c2fb7-120">DVC Server Module Example</span></span>](dvc-server-component-example.md)
</dt> <dd>

<span data-ttu-id="c2fb7-121">C++-Codebeispiel, das zeigt, wie das serverseitige Dynamic Virtual Channel (DVC)-Modul erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c2fb7-121">C++ code sample that shows how to create the server-side dynamic virtual channel (DVC) module.</span></span>

</dd> </dl>

 

 




