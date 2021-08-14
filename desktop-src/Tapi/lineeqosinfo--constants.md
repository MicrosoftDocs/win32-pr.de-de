---
description: Diese Konstanten werden von einem TSP verwendet, um das Ergebnis einer QoS-Anforderung (Quality of Service) zu identifizieren.
ms.assetid: 617ddbf4-212f-4990-93c2-f38f04b035ab
title: LINEEQOSINFO_ Konstanten (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c07a2d532e578b1f7df752cfd4930660d1d22dd4dd8406f0f8cc8bd61924bf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761393"
---
# <a name="lineeqosinfo_-constants"></a>LINEEQOSINFO-Konstanten \_

Diese Konstanten werden von einem TSP verwendet, um das Ergebnis einer QoS-Anforderung (Quality of Service) zu identifizieren.

<dl> <dt>

<span id="LINEEQOSINFO_NOQOS"></span><span id="lineeqosinfo_noqos"></span>**LINEEQOSINFO \_ NOQOS**
</dt> <dd> <dl> <dt>

 0x00000001
</dt> <dt>



QoS ist nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="LINEEQOSINFO_ADMISSIONFAILURE"></span><span id="lineeqosinfo_admissionfailure"></span>**LINEEQOSINFO \_ ADMISSIONFAILURE**
</dt> <dd> <dl> <dt>

 0x00000002
</dt> <dt>



Die QoS-Anforderung konnte nicht erfüllt werden.


</dt> </dl> </dd> <dt>

<span id="LINEEQOSINFO_POLICYFAILURE"></span><span id="lineeqosinfo_policyfailure"></span>**LINEEQOSINFO \_ POLICYFAILURE**
</dt> <dd> <dl> <dt>

 0x00000003
</dt> <dt>



Der angeforderte QoS-Typ wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="LINEEQOSINFO_GENERICERROR"></span><span id="lineeqosinfo_genericerror"></span>**LINEEQOSINFO \_ GENERICERROR**
</dt> <dd> <dl> <dt>

 0x00000004
</dt> <dt>



Nicht angegebener QoS-Fehler.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.2<br/>                                                      |
| Header<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



 

 




