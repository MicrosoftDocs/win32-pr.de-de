---
title: Neues in SNMP
description: SNMP unterstützt die Verwendung von IPv6 ab Windows Vista.
ms.assetid: 38d71c0a-8de1-45a7-958c-aa44411451bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 913f71cdf0b23800340f2c43f7b7fa22f45883a2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729784"
---
# <a name="new-in-snmp"></a><span data-ttu-id="a7fbe-103">Neues in SNMP</span><span class="sxs-lookup"><span data-stu-id="a7fbe-103">New in SNMP</span></span>

<span data-ttu-id="a7fbe-104">\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="a7fbe-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a7fbe-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="a7fbe-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a7fbe-106">Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]</span><span class="sxs-lookup"><span data-stu-id="a7fbe-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="a7fbe-107">SNMP unterstützt die Verwendung von IPv6 ab Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a7fbe-107">SNMP supports the use of IPv6 starting with Windows Vista.</span></span> <span data-ttu-id="a7fbe-108">SNMP unterstützt IPv6 jedoch nur für Netzwerke mit Windows Server 2008 und Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a7fbe-108">However, SNMP supports IPv6 only for networks running Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="a7fbe-109">Dies liegt daran, dass SNMP den aktualisierten Protokollstapel erfordert, der in diesen Betriebssystemen für die IPv6-Unterstützung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a7fbe-109">This is because SNMP requires the updated protocol stack available in these operating systems for its IPv6 support.</span></span>

<span data-ttu-id="a7fbe-110">Die IPv6-Kommunikation schlägt fehl, es sei denn, Ihr Netzwerk ist allein ein Windows Server 2008-Netzwerk, auch wenn ein IPv6-Protokollstapel separat auf den Computern installiert ist, auf denen frühere Versionen von Windows ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a7fbe-110">Unless your network is solely a Windows Server 2008 network, IPv6 communications will fail, even if an IPv6 protocol stack is separately installed on those computers that run earlier versions of Windows.</span></span> <span data-ttu-id="a7fbe-111">SNMP-Agents, die unter Windows Server 2003, oder Windows XP oder Windows 2000 ausgeführt werden, Antworten beispielsweise nur auf Abfragen, die an Ihre IPv4-Adressen gerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="a7fbe-111">For example, SNMP agents that run on Windows Server 2003, or Windows XP, or Windows 2000, respond only to queries that are made to their IPv4 addresses.</span></span>

 

 