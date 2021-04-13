---
description: Eine allgemeine Übertragung über das Internet erfolgt durch Festlegen der \_ Felder SA netnum und SA \_ nodenum auf Binärdateien (1).
ms.assetid: a56f3059-d6e5-42eb-8ba2-16071fffafa5
title: Alle Routen Broadcast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15830ad4f82a3cc5d93e84762c8c17ed0cfd85bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484963"
---
# <a name="all-routes-broadcast"></a><span data-ttu-id="ca0f8-103">Alle Routen Broadcast</span><span class="sxs-lookup"><span data-stu-id="ca0f8-103">All Routes Broadcast</span></span>

<span data-ttu-id="ca0f8-104">Eine allgemeine Übertragung über das Internet erfolgt durch Festlegen der Felder **sa \_ netnum** und **sa \_ nodenum** auf Binärdateien (1).</span><span class="sxs-lookup"><span data-stu-id="ca0f8-104">A general broadcast through the Internet is achieved by setting the **sa\_netnum** and **sa\_nodenum** fields to binary ones (1).</span></span> <span data-ttu-id="ca0f8-105">Der Dienstanbieter übersetzt diese Anforderung in ein Typ-20-Paket, das IPX-Router erkennen und weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="ca0f8-105">The service provider translates this request to a type-20 packet, which IPX routers recognize and forward.</span></span> <span data-ttu-id="ca0f8-106">Das Paket besucht alle Subnetze und kann mehrmals dupliziert werden.</span><span class="sxs-lookup"><span data-stu-id="ca0f8-106">The packet visits all subnets and may be duplicated several times.</span></span> <span data-ttu-id="ca0f8-107">Empfänger müssen mehrere doppelte Kopien des Datagramms verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="ca0f8-107">Receivers must handle several duplicate copies of the datagram.</span></span>

<span data-ttu-id="ca0f8-108">Die Verwendung dieses Broadcast Typs ist für Netzwerkadministratoren unpopulär, daher sollte die Verwendung sehr eingeschränkt sein.</span><span class="sxs-lookup"><span data-stu-id="ca0f8-108">Use of this broadcast type is unpopular among network administrators, so its use should be extremely limited.</span></span> <span data-ttu-id="ca0f8-109">Viele Router deaktivieren diese Art von Broadcast, sodass Teile des Subnetzes nicht für das Paket unsichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="ca0f8-109">Many routers disable this type of broadcast, leaving parts of the subnet invisible to the packet.</span></span>

 

 



