---
description: Der TAPI-Server (tapisrv) ist das zentrale Repository von Telefoniedaten auf einem Benutzer Computer.
ms.assetid: 794d230c-abe8-429d-bbf5-91ba364b16ab
title: TAPI-Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838a6886a5d8e56519f10fc370ed15adc3b1af7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866912"
---
# <a name="tapi-server"></a><span data-ttu-id="64472-103">TAPI-Server</span><span class="sxs-lookup"><span data-stu-id="64472-103">TAPI Server</span></span>

<span data-ttu-id="64472-104">Der TAPI-Server (tapisrv) ist das zentrale Repository von Telefoniedaten auf einem Benutzer Computer.</span><span class="sxs-lookup"><span data-stu-id="64472-104">The TAPI server (TAPISRV) is the central repository of telephony data on a user computer.</span></span> <span data-ttu-id="64472-105">Dieser Dienst Prozess verfolgt lokale und Remote Telefonieressourcen, für die Verarbeitung von unterstützten Telefonieanforderungen registrierte Anwendungen und ausstehende asynchrone Funktionen und ermöglicht außerdem eine konsistente Schnittstelle mit Telefoniedienstanbietern (Telefoniedienstanbietern).</span><span class="sxs-lookup"><span data-stu-id="64472-105">This service process tracks local and remote telephony resources, applications registered to handle Assisted Telephony requests, and pending asynchronous functions, and it also enables a consistent interface with telephony service providers (TSPs).</span></span> <span data-ttu-id="64472-106">Weitere Informationen und ein Diagramm, das die Beziehung zwischen dem TAPI-Server und anderen Komponenten und einer Übersicht über seine Rollen veranschaulicht, finden Sie unter [Microsoft Telefonie-Programmiermodell](microsoft-telephony-programming-model.md).</span><span class="sxs-lookup"><span data-stu-id="64472-106">For more information and a diagram that illustrates the relationship of the TAPI Server to other components and an overview of their roles, see [Microsoft Telephony Programming Model](microsoft-telephony-programming-model.md).</span></span>

<span data-ttu-id="64472-107">Für Computer, die unter Windows Server 2003-Betriebssystemen, Windows XP und Windows 2000 ausgeführt werden, wird tapisrv innerhalb des Kontexts von Svchost.exe ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="64472-107">For computers running on Windows Server 2003 operating systems, Windows XP, and Windows 2000, TAPISRV runs within the context of Svchost.exe.</span></span> <span data-ttu-id="64472-108">Für Computer, die unter Windows NT ausgeführt werden, wird dieser als separater Dienst Prozess ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="64472-108">For computers running on Windows NT, it runs as a separate service process.</span></span> <span data-ttu-id="64472-109">Wenn eine Anwendung eine TAPI-dll in ihren Prozessbereich lädt und einen Initialisierungs Vorgang ausführt, stellt die dll einen RPC-Link zum TAPI-Server her.</span><span class="sxs-lookup"><span data-stu-id="64472-109">When an application loads a TAPI DLL into its process space and performs an initialization operation, the DLL establishes an RPC link to the TAPI Server.</span></span> <span data-ttu-id="64472-110">Der TAPI-Server lädt Telefondienstanbieter (TSPS) in seinen Prozessbereich.</span><span class="sxs-lookup"><span data-stu-id="64472-110">The TAPI Server loads telephone service providers (TSPs) into its process space.</span></span> <span data-ttu-id="64472-111">Unabhängig davon, wie viele Anwendungen auf die Geräte eines bestimmten Anbieters zugreifen, ist nur eine Instanz eines bestimmten TSP vorhanden.</span><span class="sxs-lookup"><span data-stu-id="64472-111">Regardless of how many applications access a given provider's devices, only one instance of a given TSP will exist.</span></span>

 

 



