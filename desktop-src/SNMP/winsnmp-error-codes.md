---
title: WinSNMP-Fehler Codes
description: WinSNMP-Fehler Codes
ms.assetid: 03b13b82-a31c-47e2-8b4d-17dcc4d19e56
keywords:
- WinSNMP-Fehler Codes SNMP
- Fehler Codes SNMP, WinSNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d3cff7bd1e534f5f9c1fb0ae2ea2687d2ba99a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473965"
---
# <a name="winsnmp-error-codes"></a><span data-ttu-id="8993b-105">WinSNMP-Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="8993b-105">WinSNMP Error Codes</span></span>

<span data-ttu-id="8993b-106">\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="8993b-106">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8993b-107">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="8993b-107">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="8993b-108">Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]</span><span class="sxs-lookup"><span data-stu-id="8993b-108">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

> [!Note]  
> <span data-ttu-id="8993b-109">Die in diesem Thema beschriebenen Fehler unterscheiden sich von den SNMP-Fehlercodes, die von den entsprechenden RFCs definiert werden.</span><span class="sxs-lookup"><span data-stu-id="8993b-109">The errors described in this topic are distinct from the SNMP error codes defined by the relevant RFCs.</span></span>

 

<span data-ttu-id="8993b-110">Alle WinSNMP-Funktionen geben den Wert **Snmpapi \_ Failure** zurück, wenn die Funktion fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="8993b-110">All WinSNMP functions return the value **SNMPAPI\_FAILURE** if the function fails.</span></span> <span data-ttu-id="8993b-111">Die WinSNMP-Anwendung muss sofort die [**snmpgetlasterror**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) -Funktion aufrufen, um erweiterte Fehlerinformationen abzurufen, wenn eine WinSNMP-Funktion fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="8993b-111">The WinSNMP application must immediately call the [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) function to retrieve extended error information when a WinSNMP function fails.</span></span> <span data-ttu-id="8993b-112">Die folgende Tabelle enthält Themen, in denen die von WinSNMP-Funktionen zurückgegebenen erweiterten Fehlercodes erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="8993b-112">The following table lists topics that discuss extended error codes returned by WinSNMP functions.</span></span>



| <span data-ttu-id="8993b-113">Thema</span><span class="sxs-lookup"><span data-stu-id="8993b-113">Topic</span></span>                                                        | <span data-ttu-id="8993b-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8993b-114">Description</span></span>                                             |
|--------------------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="8993b-115">Allgemeine WinSNMP-Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="8993b-115">WinSNMP Common Error Codes</span></span>](winsnmp-common-error-codes.md) | <span data-ttu-id="8993b-116">Beschreibt häufige Fehlercodes für die WinSNMP-API.</span><span class="sxs-lookup"><span data-stu-id="8993b-116">Describes common error codes for the WinSNMP API.</span></span>       |
| [<span data-ttu-id="8993b-117">Netzwerk Transport Fehler</span><span class="sxs-lookup"><span data-stu-id="8993b-117">Network Transport Errors</span></span>](network-transport-errors.md)     | <span data-ttu-id="8993b-118">Beschreibt Netzwerk Transport Fehler für die WinSNMP-API.</span><span class="sxs-lookup"><span data-stu-id="8993b-118">Describes network transport errors for the WinSNMP API.</span></span> |



 

<span data-ttu-id="8993b-119">Die WinSNMP-Fehler, die kontextspezifische Informationen übermitteln, sind auf der Seite Funktionsreferenz enthalten.</span><span class="sxs-lookup"><span data-stu-id="8993b-119">The WinSNMP errors that convey context-specific information are included in the function reference page.</span></span>

 

 