---
description: TAPI bietet eine Reihe von Funktionen zum Bearbeiten von Aufruf Handles und bestimmt die Beziehung zwischen Zeilen, aufrufen und Adressen usw.
ms.assetid: 283fe5e9-689f-4b87-97a6-b345c22ec6a2
title: Bearbeitung von anrufhandles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 248f16088f891b1441626097de5c803a8fe14991
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350571"
---
# <a name="call-handle-manipulation"></a><span data-ttu-id="c40fd-103">Bearbeitung von anrufhandles</span><span class="sxs-lookup"><span data-stu-id="c40fd-103">Call Handle Manipulation</span></span>

<span data-ttu-id="c40fd-104">TAPI bietet eine Reihe von Funktionen zum Bearbeiten von Aufruf Handles und bestimmt die Beziehung zwischen Zeilen, aufrufen und Adressen usw.</span><span class="sxs-lookup"><span data-stu-id="c40fd-104">TAPI provides a number of functions for manipulating call handles, determining the relationship among lines, calls, and address, and so on.</span></span> <span data-ttu-id="c40fd-105">Die meisten dieser Funktionen werden ausschließlich in TAPI ohne Verweis auf den Dienstanbieter implementiert, mit Ausnahme von [**TSPI \_ linegetcalladressid**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcalladdressid).</span><span class="sxs-lookup"><span data-stu-id="c40fd-105">Most of this functionality is implemented strictly within TAPI without reference to the service provider, except for [**TSPI\_lineGetCallAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcalladdressid).</span></span> <span data-ttu-id="c40fd-106">Diese Funktion Ruft den Adress Bezeichner eines vorhandenen Aufrufes in der Zeile ab.</span><span class="sxs-lookup"><span data-stu-id="c40fd-106">This function retrieves the address identifier of an existing call within its line.</span></span> <span data-ttu-id="c40fd-107">Dienstanbieter, die eine Zeile als Gruppe von Adress bezeichtern modellieren, können eine unvorhersehbare Adresse für einen neuen eingehenden oder ausgehenden Rückruf auswählen.</span><span class="sxs-lookup"><span data-stu-id="c40fd-107">Service providers that model a line as a group of address identifiers can choose an unpredictable address for a new inbound or outbound call.</span></span> <span data-ttu-id="c40fd-108">Diese Funktion bietet TAPI ausreichend Informationen, um den [**linegetnewcalls**](/windows/win32/api/tapi/nf-tapi-linegetnewcalls) -Vorgang zu implementieren, wenn er mit der Option "linecallselect Address" aufgerufen wird \_ .</span><span class="sxs-lookup"><span data-stu-id="c40fd-108">This function gives TAPI sufficient information to implement the [**lineGetNewCalls**](/windows/win32/api/tapi/nf-tapi-linegetnewcalls) operation when it is invoked with the LINECALLSELECT\_ADDRESS option.</span></span>

 

 
