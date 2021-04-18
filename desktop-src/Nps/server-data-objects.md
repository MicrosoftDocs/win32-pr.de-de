---
title: Server Datenobjekte
description: Die Server Data Objects (SDO)-API ermöglicht die programmgesteuerte Konfiguration und Verwaltung eines Systems, auf dem NPS ausgeführt wird.
ms.assetid: 9d159e15-f534-4ab1-9641-db70064beb51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eebd0f837f9a8a36af1eb9118189015e677e2af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337446"
---
# <a name="server-data-objects"></a><span data-ttu-id="c68ac-103">Server Datenobjekte</span><span class="sxs-lookup"><span data-stu-id="c68ac-103">Server Data Objects</span></span>

> [!Note]  
> <span data-ttu-id="c68ac-104">Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt.</span><span class="sxs-lookup"><span data-stu-id="c68ac-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="c68ac-105">Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS.</span><span class="sxs-lookup"><span data-stu-id="c68ac-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="c68ac-106">Im gesamten Text wird NPS verwendet, um auf alle Versionen des Dienstanbieter zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="c68ac-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="c68ac-107">Die Server Data Objects (SDO)-API ermöglicht die programmgesteuerte Konfiguration und Verwaltung eines Systems, auf dem NPS ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c68ac-107">The Server Data Objects (SDO) API makes it possible to programmatically configure and administer a system running NPS.</span></span> <span data-ttu-id="c68ac-108">Mithilfe von SDO kann ein Entwickler auch Anwendungen schreiben, die RAS-Richtlinien und-Profile verwalten.</span><span class="sxs-lookup"><span data-stu-id="c68ac-108">Using SDO, a developer can also write applications that administer remote access policies and profiles.</span></span> <span data-ttu-id="c68ac-109">Die RAS-Richtlinien und-Profile werden vom Routing-und RAS-Dienst (RRAS) sowie von NPS verwendet, um zu bestimmen, ob ein Remote Client eine Verbindung mit einem Netzwerk Zugriffs Server (NAS) herstellen darf.</span><span class="sxs-lookup"><span data-stu-id="c68ac-109">The remote access policies and profiles are used by the Routing and Remote Access Service (RRAS) as well as NPS to determine whether a remote client is allowed to connect to a network access server (NAS).</span></span>

<span data-ttu-id="c68ac-110">Die SDO-API ist in jeder Umgebung anwendbar, die NPS oder RAS-Richtlinien verwendet.</span><span class="sxs-lookup"><span data-stu-id="c68ac-110">The SDO API is applicable in any environment that uses NPS or Remote Access Policies.</span></span>

<span data-ttu-id="c68ac-111">Mithilfe der SDO-API kann ein Entwickler jedes beliebige Element der NPS-Konfiguration bearbeiten, auf das über die NPS-Benutzeroberfläche zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="c68ac-111">With the SDO API, a developer can manipulate any element of the NPS configuration that is accessible through the NPS user interface.</span></span>

<span data-ttu-id="c68ac-112">Mithilfe der SDO-API können auch alle Werte festgelegt oder abgerufen werden, auf die über die Eigenschaften Seite Benutzer-Einwähleinstellungen zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="c68ac-112">The SDO API also makes it possible to set or retrieve any of the values accessible through the user dial-in settings property page.</span></span>

<span data-ttu-id="c68ac-113">Die SDO-API besteht aus COM-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="c68ac-113">The SDO API is composed of COM interfaces.</span></span> <span data-ttu-id="c68ac-114">Jede der Schnittstellen in der SDO-API erbt von der com- [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c68ac-114">Each of the interfaces in the SDO API inherits from the COM [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="c68ac-115">Die **IDispatch** -Schnittstelle ermöglicht es Entwicklern, die Methoden der SDO-Schnittstelle von Visual Basic oder einem beliebigen Automatisierungs Client sowie von C/C++ aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c68ac-115">The **IDispatch** interface enables developers to call the SDO interface methods from Visual Basic or any Automation client, as well as from C/C++.</span></span>

<span data-ttu-id="c68ac-116">Entwickler können die SDO-API auch aus Skriptsprachen wie VBScript abrufen.</span><span class="sxs-lookup"><span data-stu-id="c68ac-116">Developers can also call the SDO API from scripting languages such as VBScript.</span></span> <span data-ttu-id="c68ac-117">Da VBScript jedoch nur die Verwendung von Variant-Typparametern beschränkt, sind nicht alle Funktionen von SDO verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c68ac-117">However, because VBScript is limited to using VARIANT-type parameters only, not all the functionality of SDO is available.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c68ac-118">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c68ac-118">In This Section</span></span>

[<span data-ttu-id="c68ac-119">Übersicht</span><span class="sxs-lookup"><span data-stu-id="c68ac-119">Overview</span></span>](/windows/desktop/Nps/sdo-about-server-data-objects)

<span data-ttu-id="c68ac-120">Allgemeine Informationen zur Server Data Objects-API.</span><span class="sxs-lookup"><span data-stu-id="c68ac-120">General information about the Server Data Objects API.</span></span>

[<span data-ttu-id="c68ac-121">Genutzt</span><span class="sxs-lookup"><span data-stu-id="c68ac-121">Using</span></span>](/windows/desktop/Nps/sdo-using-server-data-objects)

<span data-ttu-id="c68ac-122">Beispielcode, der die Verwendung der Server Data Objects-API veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c68ac-122">Sample code that demonstrates how to use the Server Data Objects API.</span></span>

[<span data-ttu-id="c68ac-123">Verweis</span><span class="sxs-lookup"><span data-stu-id="c68ac-123">Reference</span></span>](/windows/desktop/Nps/sdo-server-data-objects-reference)

<span data-ttu-id="c68ac-124">Dokumentation der enumerierten Typen und Schnittstellen, die die Server Data Objects-API bilden.</span><span class="sxs-lookup"><span data-stu-id="c68ac-124">Documentation of the enumerated types and interfaces that compose the Server Data Objects API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c68ac-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c68ac-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c68ac-126">Netzwerk Richtlinien Server (Internet Authentication Service)</span><span class="sxs-lookup"><span data-stu-id="c68ac-126">Network Policy Server (Internet Authentication Service)</span></span>](portal.md)
</dt> <dt>

[<span data-ttu-id="c68ac-127">RAS-Dienst</span><span class="sxs-lookup"><span data-stu-id="c68ac-127">Remote Access Service</span></span>](/windows/desktop/RRAS/portal)
</dt> </dl>

 

 