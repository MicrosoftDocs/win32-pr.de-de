---
description: Der INITIALIZE \_ NEGOTIATION-Datentyp ist ein spezieller Wert vom Typ DWORD.
ms.assetid: ce978913-47a1-4387-bd1b-1795aaf82dd7
title: INITIALIZE_NEGOTIATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d24763b9214dcffab99c83f24028e451a33d70dd7e4210f4eff64b0c39306d6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762777"
---
# <a name="initialize_negotiation"></a>INITIALIZE \_ NEGOTIATION

Der **INITIALIZE \_ NEGOTIATION-Datentyp** ist ein spezieller Wert vom **Typ DWORD.** Sie kann als *dwDeviceID-Parameter* in den [**Funktionen TSPI \_ lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) und [**TSPI \_ phoneNegotiateTSPIVersion übergeben**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) werden. Dies bedeutet, dass TAPI unabhängig von bestimmten Geräten eine TSPI-Schnittstellenversionsnummer aushandeln kann.

 

 
