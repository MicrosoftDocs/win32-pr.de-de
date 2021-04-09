---
title: WinSNMP-Datentypen
description: Die standardmäßigen WinSNMP-Datentypen werden in WinSNMP definiert. H-Datei.
ms.assetid: 20f1bbc3-5a08-4206-980d-22a794cda402
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7061ade6f9b69c63ba4718d9d79bbd4d39c67b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039485"
---
# <a name="winsnmp-data-types"></a><span data-ttu-id="b56e7-103">WinSNMP-Datentypen</span><span class="sxs-lookup"><span data-stu-id="b56e7-103">WinSNMP Data Types</span></span>

<span data-ttu-id="b56e7-104">\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="b56e7-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b56e7-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="b56e7-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b56e7-106">Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]</span><span class="sxs-lookup"><span data-stu-id="b56e7-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="b56e7-107">Die standardmäßigen WinSNMP-Datentypen werden in WinSNMP definiert. H-Datei.</span><span class="sxs-lookup"><span data-stu-id="b56e7-107">The standard WinSNMP data types are defined in the WINSNMP.H file.</span></span>

<span data-ttu-id="b56e7-108">Beachten Sie, dass WinSNMP einige Parameter mit dem Typ "Long Integer" mit Vorzeichen, **smiint**, angibt.</span><span class="sxs-lookup"><span data-stu-id="b56e7-108">Note that WinSNMP specifies some parameters with the signed long integer type, **smiINT**.</span></span> <span data-ttu-id="b56e7-109">Dies ermöglicht es WinSNMP, die Datenelemente zu erfüllen, insbesondere die PDU-Komponenten, die in den entsprechenden RFCs definiert sind.</span><span class="sxs-lookup"><span data-stu-id="b56e7-109">This enables WinSNMP to comply with the data elements, especially the PDU components, defined in the relevant RFCs.</span></span>

 

 