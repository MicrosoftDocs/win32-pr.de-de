---
description: Der Datentyp für die Initialisierung der \_ Aushandlung ist ein spezieller Wert des Typs DWORD.
ms.assetid: ce978913-47a1-4387-bd1b-1795aaf82dd7
title: INITIALIZE_NEGOTIATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51a55879a0952d3f8b5e268ec6a01a666bdbf5ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753417"
---
# <a name="initialize_negotiation"></a><span data-ttu-id="2e36f-103">Aushandlung initialisieren \_</span><span class="sxs-lookup"><span data-stu-id="2e36f-103">INITIALIZE\_NEGOTIATION</span></span>

<span data-ttu-id="2e36f-104">Der Datentyp für die **Initialisierung der \_ Aushandlung** ist ein spezieller Wert des Typs **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="2e36f-104">The **INITIALIZE\_NEGOTIATION** datatype is a special value of type **DWORD**.</span></span> <span data-ttu-id="2e36f-105">Sie kann als *dwdeviceid* -Parameter in den [**TSPI \_ linenegotiatetspiversion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) -und [**TSPI \_ phonenegotiatetspiversion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) -Funktionen übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="2e36f-105">It can be passed as the *dwDeviceID* parameter in the [**TSPI\_lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) and [**TSPI\_phoneNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) functions.</span></span> <span data-ttu-id="2e36f-106">Dies deutet darauf hin, dass TAPI eine TSPI-Schnittstellen Versionsnummer unabhängig von bestimmten Geräten aushandeln kann.</span><span class="sxs-lookup"><span data-stu-id="2e36f-106">Doing so indicates that TAPI can negotiate a TSPI interface version number independent of any specific devices.</span></span>

 

 
