---
title: Informationen zu SNMP
description: SNMP verwendet eine verteilte Architektur, bestehend aus Managern und Agents.
ms.assetid: 55be55a8-1968-4373-a969-f7e03b75a824
keywords:
- SNMP, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1dab65173c96dce4bbd2f30edbca2a91f6153d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039434"
---
# <a name="about-snmp"></a><span data-ttu-id="7e2bc-104">Informationen zu SNMP</span><span class="sxs-lookup"><span data-stu-id="7e2bc-104">About SNMP</span></span>

<span data-ttu-id="7e2bc-105">\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="7e2bc-105">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7e2bc-106">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="7e2bc-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="7e2bc-107">Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]</span><span class="sxs-lookup"><span data-stu-id="7e2bc-107">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="7e2bc-108">SNMP verwendet eine verteilte Architektur, bestehend aus Managern und Agents.</span><span class="sxs-lookup"><span data-stu-id="7e2bc-108">SNMP uses a distributed architecture consisting of managers and agents.</span></span> <span data-ttu-id="7e2bc-109">Ein Agent ist eine SNMP-Anwendung, die auf Abfragen von SNMP-Manager-Anwendungen antwortet.</span><span class="sxs-lookup"><span data-stu-id="7e2bc-109">An agent is an SNMP application that responds to queries from SNMP manager applications.</span></span> <span data-ttu-id="7e2bc-110">Der SNMP-Agent ist für das Abrufen und Aktualisieren lokaler Verwaltungsinformationen basierend auf den Anforderungen des SNMP-Managers verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="7e2bc-110">The SNMP agent is responsible for retrieving and updating local management information based on the requests of the SNMP manager.</span></span> <span data-ttu-id="7e2bc-111">Der Agent benachrichtigt auch registrierte Manager, wenn wichtige Ereignisse oder Traps auftreten.</span><span class="sxs-lookup"><span data-stu-id="7e2bc-111">The agent also notifies registered managers when significant events or traps occur.</span></span> <span data-ttu-id="7e2bc-112">Ein Manager ist eine SNMP-Anwendung, die Abfragen für SNMP-Agent-Anwendungen generiert und Traps von SNMP-Agent-Anwendungen empfängt.</span><span class="sxs-lookup"><span data-stu-id="7e2bc-112">A manager is an SNMP application that generates queries to SNMP agent applications and receives traps from SNMP agent applications.</span></span>

<span data-ttu-id="7e2bc-113">Auf Computern, auf denen Microsoft Windows XP/Windows 2000/Windows NT ausgeführt wird, wird der SNMP-Agent vom SNMP-Dienst (SNMP.EXE) implementiert.</span><span class="sxs-lookup"><span data-stu-id="7e2bc-113">On computers running Microsoft Windows XP/Windows 2000/Windows NT, the SNMP agent is implemented by the SNMP service (SNMP.EXE).</span></span> <span data-ttu-id="7e2bc-114">Der SNMP-Manager ist in der Regel eine SNMP-Verwaltungs Konsolenanwendung eines Drittanbieters.</span><span class="sxs-lookup"><span data-stu-id="7e2bc-114">The SNMP manager is typically a third-party SNMP management console application.</span></span> <span data-ttu-id="7e2bc-115">Die Verwaltungs Konsolenanwendung muss nicht auf demselben Host wie der SNMP-Agent ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7e2bc-115">The management console application does not need to run on the same host as the SNMP agent.</span></span> <span data-ttu-id="7e2bc-116">Um die Informationen zu verwenden, die der Microsoft SNMP-Dienst bereitstellt, benötigen Sie mindestens eine SNMP-Verwaltungs Konsolenanwendung.</span><span class="sxs-lookup"><span data-stu-id="7e2bc-116">To use the information the Microsoft SNMP service provides, you need at least one SNMP management console application.</span></span> <span data-ttu-id="7e2bc-117">Das System enthält Bibliotheken, die SNMP-Verwaltungs Konsolen Anwendungen unterstützen. zurzeit ist jedoch keine SNMP-Verwaltungs Konsolenanwendung enthalten.</span><span class="sxs-lookup"><span data-stu-id="7e2bc-117">The system includes libraries that support SNMP management console applications, but it does not include an SNMP management console application at this time.</span></span>

 

 