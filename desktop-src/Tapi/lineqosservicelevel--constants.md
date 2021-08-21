---
description: Diese Konstanten werden von einem TSP verwendet, um den Typ einer erforderlichen QoS-Ebene (Quality of Service) zu identifizieren.
ms.assetid: 9fc3f6eb-7103-43c5-84f8-3842757e5be7
title: LINEQOSSERVICELEVEL_ Konstanten (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a74a4508b54a8b56e8e9cb359f966122c5c009f0e5ede0f1b8544cd1e46330c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003008"
---
# <a name="lineqosservicelevel_-constants"></a>LINEQOSSERVICELEVEL-Konstanten \_

Diese Konstanten werden von einem TSP verwendet, um den Typ einer erforderlichen QoS-Ebene (Quality of Service) zu identifizieren.

<dl> <dt>

<span id="LINEQOSSERVICELEVEL_NEEDED"></span><span id="lineqosservicelevel_needed"></span>**LINEQOSSERVICELEVEL \_ ERFORDERLICH**
</dt> <dd> <dl> <dt>

 0x00000001
</dt> <dt>



Die qualität des angeforderten Servicelevels ist eine Anforderung.


</dt> </dl> </dd> <dt>

<span id="LINEQOSSERVICELEVEL_IFAVAILABLE"></span><span id="lineqosservicelevel_ifavailable"></span>**LINEQOSSERVICELEVEL, \_ FALLS VERFÜGBAR**
</dt> <dd> <dl> <dt>

 0x00000002
</dt> <dt>



Die erforderliche Servicelevelqualität( falls verfügbar).


</dt> </dl> </dd> <dt>

<span id="LINEQOSSERVICELEVEL_BESTEFFORT"></span><span id="lineqosservicelevel_besteffort"></span>**LINEQOSSERVICELEVEL \_ BESTEFFORT**
</dt> <dd> <dl> <dt>

 0x00000003
</dt> <dt>



Die erforderliche Servicelevelqualität ist "beste Leistung".


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.2<br/>                                                      |
| Header<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



 

 




