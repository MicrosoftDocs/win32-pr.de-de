---
description: Ein Transportprotokoll muss ordnungsgemäß auf dem System installiert und bei Windows Sockets registriert sein, damit es für eine Anwendung zugänglich ist.
ms.assetid: 45b20f66-4e12-44df-b64b-c96cd5b24cd4
title: Gleichzeitiger Zugriff auf mehrere Transport Protokolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e4b9d97743691bc527c455881cd0da5803b62b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368219"
---
# <a name="simultaneous-access-to-multiple-transport-protocols"></a><span data-ttu-id="c1238-103">Gleichzeitiger Zugriff auf mehrere Transport Protokolle</span><span class="sxs-lookup"><span data-stu-id="c1238-103">Simultaneous Access to Multiple Transport Protocols</span></span>

<span data-ttu-id="c1238-104">Ein Transportprotokoll muss ordnungsgemäß auf dem System installiert und bei Windows Sockets registriert sein, damit es für eine Anwendung zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="c1238-104">A transport protocol must be properly installed on the system and registered with Windows Sockets to be accessible to an application.</span></span> <span data-ttu-id="c1238-105">Die Ws2- \_32.dll Bibliothek exportiert eine Reihe von Funktionen, um den Registrierungsprozess zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="c1238-105">The Ws2\_32.dll library exports a set of functions to facilitate the registration process.</span></span> <span data-ttu-id="c1238-106">Dies umfasst das Erstellen einer neuen Registrierung und das Entfernen einer vorhandenen Registrierung.</span><span class="sxs-lookup"><span data-stu-id="c1238-106">This includes creating a new registration and removing an existing one.</span></span>

<span data-ttu-id="c1238-107">Wenn neue Registrierungen erstellt werden, stellt der Aufrufer (d. h. das Installationsskript des Stapel Anbieters) eine oder mehrere gefüllte [**wsaprotocol \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) -Informationsstrukturen bereit, die einen vollständigen Satz von Informationen über das Protokoll enthalten.</span><span class="sxs-lookup"><span data-stu-id="c1238-107">When new registrations are created, the caller (that is, the stack vendor's installation script) supplies one or more filled in [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structures containing a complete set of information about the protocol.</span></span> <span data-ttu-id="c1238-108">Weitere Informationen finden Sie unter [Windows Sockets 2 SPI](about-the-winsock-spi.md).</span><span class="sxs-lookup"><span data-stu-id="c1238-108">For more information, see [Windows Sockets 2 SPI](about-the-winsock-spi.md).</span></span> <span data-ttu-id="c1238-109">Alle auf diese Weise installierten Transport Stapel werden als Windows Sockets-Dienstanbieter bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c1238-109">Any transport stack installed in this manner is referred to as a Windows Sockets service provider.</span></span>

<span data-ttu-id="c1238-110">Unter Windows XP mit Service Pack 2 (SP2), Windows Server 2003 mit Service Pack 1 (SP1) und Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="c1238-110">On Windows XP with Service Pack 2 (SP2), Windows Server 2003 with Service Pack 1 (SP1), and Windows Vista and later.</span></span> <span data-ttu-id="c1238-111">der Winsock-Katalog mit einer Liste installierter Transport-und Namespace Anbieter kann mit dem folgenden Befehl an einer Eingabeaufforderung angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="c1238-111">the Winsock catalog that contains a list of installed transport and namespace providers can be displayed in a command prompt with the following command:</span></span>

<span data-ttu-id="c1238-112">**netsh Winsock Show Catalog**</span><span class="sxs-lookup"><span data-stu-id="c1238-112">**netsh winsock show catalog**</span></span>

<span data-ttu-id="c1238-113">Das Microsoft Windows Software Development Kit (SDK) umfasst *Sporder.exe*, mit dem der Benutzer die Reihenfolge anzeigen und ändern kann, in der die Dienstanbieter aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="c1238-113">The Microsoft Windows Software Development Kit (SDK) includes *Sporder.exe*, which enables the user to view and modify the order in which service providers are enumerated.</span></span> <span data-ttu-id="c1238-114">Mithilfe von *Sporder.exe* kann ein Benutzer manuell einen bestimmten TCP/IP-Protokollstapel als standardmäßigen TCP/IP-Anbieter einrichten, wenn mehr als ein solcher Stapel vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c1238-114">Using *Sporder.exe*, a user can manually establish a particular TCP/IP protocol stack as the default TCP/IP provider if more than one such stack is present.</span></span>

<span data-ttu-id="c1238-115">Die *Sporder.exe* -Anwendung verwendet exportierte Funktionen aus *Sporder.dll* , um die Dienstanbieter neu anzuordnen.</span><span class="sxs-lookup"><span data-stu-id="c1238-115">The *Sporder.exe* application uses exported functions from *Sporder.dll* to reorder the service providers.</span></span> <span data-ttu-id="c1238-116">Daher können Installationsanwendungen die von *Sporder.dll* bereitgestellte Schnittstelle verwenden, um Dienstanbieter Programm gesteuert neu zu ordnen.</span><span class="sxs-lookup"><span data-stu-id="c1238-116">As a result, installation applications can use the interface provided by *Sporder.dll* to programmatically reorder service providers.</span></span>

-   [<span data-ttu-id="c1238-117">Geschichtete Protokolle und Protokoll Ketten</span><span class="sxs-lookup"><span data-stu-id="c1238-117">Layered Protocols and Protocol Chains</span></span>](layered-protocols-and-protocol-chains-2.md)
-   [<span data-ttu-id="c1238-118">Verwenden mehrerer Protokolle</span><span class="sxs-lookup"><span data-stu-id="c1238-118">Using Multiple Protocols</span></span>](using-multiple-protocols-2.md)
-   [<span data-ttu-id="c1238-119">Mehrere Anbieter Einschränkungen bei SELECT</span><span class="sxs-lookup"><span data-stu-id="c1238-119">Multiple Provider Restrictions on Select</span></span>](multiple-provider-restrictions-on-select-2.md)

 

 
