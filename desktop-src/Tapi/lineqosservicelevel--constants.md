---
description: Diese Konstanten werden von einem TSP verwendet, um den Typ einer erforderlichen QoS-Ebene (Quality of Service) zu identifizieren.
ms.assetid: 9fc3f6eb-7103-43c5-84f8-3842757e5be7
title: LINEQOSSERVICELEVEL_ Konstanten (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c0629715e461a15e21e1730f86edb61d83d60db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356024"
---
# <a name="lineqosservicelevel_-constants"></a>Lineqosservicelevel- \_ Konstanten

Diese Konstanten werden von einem TSP verwendet, um den Typ einer erforderlichen QoS-Ebene (Quality of Service) zu identifizieren.

<dl> <dt>

<span id="LINEQOSSERVICELEVEL_NEEDED"></span><span id="lineqosservicelevel_needed"></span>**lineqosservicelevel \_ erforderlich**
</dt> <dd> <dl> <dt>

 0x00000001
</dt> <dt>



Die geforderte Quality of Service Level ist eine Voraussetzung.


</dt> </dl> </dd> <dt>

<span id="LINEQOSSERVICELEVEL_IFAVAILABLE"></span><span id="lineqosservicelevel_ifavailable"></span>**lineqosservicelevel \_ ifavailable**
</dt> <dd> <dl> <dt>

 0x00000002
</dt> <dt>



Die erforderliche Quality of Service Level, falls verfügbar.


</dt> </dl> </dd> <dt>

<span id="LINEQOSSERVICELEVEL_BESTEFFORT"></span><span id="lineqosservicelevel_besteffort"></span>**lineqosservicelevel \_ BestEffort**
</dt> <dd> <dl> <dt>

 0x00000003
</dt> <dt>



Die Qualität der Service Level ist erforderlich.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,2<br/>                                                      |
| Header<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



 

 




