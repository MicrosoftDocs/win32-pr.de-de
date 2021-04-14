---
description: Normalerweise implementiert ein Medien Dienstanbieter (MSP) die Terminal Erstellung.
ms.assetid: 203fccc0-aa5a-4ec3-97d3-546c36018d52
title: Schreiben eines austauschbaren Terminals
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6cbfe2da0c121fcee820d47fd57216840d23c59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526810"
---
# <a name="writing-a-pluggable-terminal"></a><span data-ttu-id="a5b65-103">Schreiben eines austauschbaren Terminals</span><span class="sxs-lookup"><span data-stu-id="a5b65-103">Writing a Pluggable Terminal</span></span>

<span data-ttu-id="a5b65-104">Normalerweise implementiert ein Medien Dienstanbieter (MSP) die Terminal Erstellung.</span><span class="sxs-lookup"><span data-stu-id="a5b65-104">Normally, a media service provider (MSP) implements terminal creation.</span></span> <span data-ttu-id="a5b65-105">Ab Windows 2000 SP1 umfasst TAPI 3 austauschbare Terminals, mit denen eine Anwendung die Terminal Erstellung implementieren kann.</span><span class="sxs-lookup"><span data-stu-id="a5b65-105">Starting with Windows 2000 SP1, TAPI 3 includes pluggable terminals to allow an application to implement terminal creation.</span></span> <span data-ttu-id="a5b65-106">Weitere Informationen zur Verwendung dieser Terminals finden Sie in der Übersicht über die [Implementierung von austauschbaren Terminals](implementing-pluggable-terminals.md) .</span><span class="sxs-lookup"><span data-stu-id="a5b65-106">Please see the overview on [implementing pluggable terminals](implementing-pluggable-terminals.md) for additional information on using these terminals.</span></span>

<span data-ttu-id="a5b65-107">Austauschbare Terminals sollten nicht regelmäßig verwendet werden, da die vollständigen Funktionen eines Terminals nur verfügbar sind, wenn ein MSP ihn vollständig kennt.</span><span class="sxs-lookup"><span data-stu-id="a5b65-107">You should not use pluggable terminals routinely because the full capabilities of a terminal will only be available when an MSP is fully aware of it.</span></span> <span data-ttu-id="a5b65-108">Außerdem sollten Sie nicht versuchen, austauschbare Terminals zu implementieren, es sei denn, Sie sind bereits mit dem Schreiben von Medien Dienstanbietern vertraut.</span><span class="sxs-lookup"><span data-stu-id="a5b65-108">Further, you should not attempt to implement pluggable terminals unless you are already familiar with writing media service providers.</span></span> <span data-ttu-id="a5b65-109">Die Techniken und potenziellen Probleme sind sehr ähnlich.</span><span class="sxs-lookup"><span data-stu-id="a5b65-109">The techniques and potential problems involved are quite similar.</span></span>

<span data-ttu-id="a5b65-110">Die Bereitstellung eines speziellen Beispiels für ein austauschbares Terminal ist derzeit für die Situation eines Konferenz Servers vorhanden, der nicht-Windows 2000 SP1-oder nicht-Multicast-H. 323-Clients zu TAPI 3 mehr Parteien-SDP/IP-Multicast Konferenzen hinzufügen muss.</span><span class="sxs-lookup"><span data-stu-id="a5b65-110">Provision for a special case of pluggable terminal currently exists for the situation of a conferencing server that needs to add non-Windows 2000 SP1 or nonmulticast H.323 clients to TAPI 3 multiparty SDP/IP multicast conferences.</span></span>

 

 



