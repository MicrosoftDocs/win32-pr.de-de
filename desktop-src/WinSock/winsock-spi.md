---
description: Windows Sockets (Winsock) Service Provider Interface (SPI).
ms.assetid: 59ac7ce6-10e7-40ac-bdce-dc01251b0bc5
title: Winsock SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ecf63a45f5175a86b8f5eb2a77ef0293182e38f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349462"
---
# <a name="winsock-spi"></a><span data-ttu-id="f093c-103">Winsock SPI</span><span class="sxs-lookup"><span data-stu-id="f093c-103">Winsock SPI</span></span>

<span data-ttu-id="f093c-104">Die Winsock-Dienstanbieter Schnittstelle oder Winsock SPI ist eine spezialisierte Disziplin von Winsock, die zum Erstellen von Anbietern verwendet wird. Transportanbieter wie TCP/IP-oder IPX/SPX-Protokollstapel verwenden die Winsock SPI, wie auch Namespace Anbieter wie das DNS (Domain Naming System) des Internets.</span><span class="sxs-lookup"><span data-stu-id="f093c-104">The Winsock Service Provider Interface, or Winsock SPI, is a specialized discipline of Winsock used to create providers; transport providers such as TCP/IP or IPX/SPX protocol stacks use the Winsock SPI, as do namespace providers such as the Internet's Domain Naming System (DNS).</span></span>

<span data-ttu-id="f093c-105">Herkömmliche Netzwerk Programmierung, z. b. das Aktivieren von Anwendungen für die Kommunikation über das Netzwerk, erfordert keine Verwendung von Winsock SPI-Schnittstellen. Verwenden Sie stattdessen [Winsock](winsock-reference.md) -Standardschnittstellen.</span><span class="sxs-lookup"><span data-stu-id="f093c-105">Traditional network programming, such as enabling applications to communicate over the network, does not require use of Winsock SPI interfaces; use standard [Winsock](winsock-reference.md) interfaces instead.</span></span>

 

<span data-ttu-id="f093c-106">Die Winsock-SPI verwendet die folgende funktionspräfix-Benennungs Konvention.</span><span class="sxs-lookup"><span data-stu-id="f093c-106">The Winsock SPI uses the following function prefix naming convention.</span></span>



| <span data-ttu-id="f093c-107">Präfix</span><span class="sxs-lookup"><span data-stu-id="f093c-107">Prefix</span></span> | <span data-ttu-id="f093c-108">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f093c-108">Meaning</span></span>                          | <span data-ttu-id="f093c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f093c-109">Description</span></span>                                       |
|--------|----------------------------------|---------------------------------------------------|
| <span data-ttu-id="f093c-110">WSP</span><span class="sxs-lookup"><span data-stu-id="f093c-110">WSP</span></span>    | <span data-ttu-id="f093c-111">Windows Sockets-Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="f093c-111">Windows Sockets Service Provider</span></span> | <span data-ttu-id="f093c-112">Einstiegspunkte des Transport Dienstanbieters</span><span class="sxs-lookup"><span data-stu-id="f093c-112">Transport service provider entry points</span></span>           |
| <span data-ttu-id="f093c-113">WPU</span><span class="sxs-lookup"><span data-stu-id="f093c-113">WPU</span></span>    | <span data-ttu-id="f093c-114">Windows Sockets-Anbieter-uprufe</span><span class="sxs-lookup"><span data-stu-id="f093c-114">Windows Sockets Provider Upcall</span></span>  | <span data-ttu-id="f093c-115">Ws2 \_32.dll Einstiegspunkte für Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="f093c-115">Ws2\_32.dll entry points for service providers</span></span>    |
| <span data-ttu-id="f093c-116">WSC</span><span class="sxs-lookup"><span data-stu-id="f093c-116">WSC</span></span>    | <span data-ttu-id="f093c-117">Windows Sockets-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="f093c-117">Windows Sockets Configuration</span></span>    | <span data-ttu-id="f093c-118">Ws2 \_32.dll Einstiegspunkte für Installations-Applets</span><span class="sxs-lookup"><span data-stu-id="f093c-118">WS2\_32.dll entry points for installation applets</span></span> |
| <span data-ttu-id="f093c-119">NSP</span><span class="sxs-lookup"><span data-stu-id="f093c-119">NSP</span></span>    | <span data-ttu-id="f093c-120">Namespace Anbieter</span><span class="sxs-lookup"><span data-stu-id="f093c-120">Namespace Provider</span></span>               | <span data-ttu-id="f093c-121">Einstiegspunkte des Namespace Anbieters</span><span class="sxs-lookup"><span data-stu-id="f093c-121">Namespace provider entry points</span></span>                   |



 

 

 



