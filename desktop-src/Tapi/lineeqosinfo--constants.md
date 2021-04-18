---
description: Diese Konstanten werden von einem TSP verwendet, um das Ergebnis einer QoS (Quality of Service)-Anforderung zu identifizieren.
ms.assetid: 617ddbf4-212f-4990-93c2-f38f04b035ab
title: LINEEQOSINFO_ Konstanten (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 423cc6172a1c6c87c1f3bb38929f727a15dad5c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354731"
---
# <a name="lineeqosinfo_-constants"></a>Lineeqosinfo- \_ Konstanten

Diese Konstanten werden von einem TSP verwendet, um das Ergebnis einer QoS (Quality of Service)-Anforderung zu identifizieren.

<dl> <dt>

<span id="LINEEQOSINFO_NOQOS"></span><span id="lineeqosinfo_noqos"></span>**lineeqosinfo- \_ noqos**
</dt> <dd> <dl> <dt>

 0x00000001
</dt> <dt>



QoS ist nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="LINEEQOSINFO_ADMISSIONFAILURE"></span><span id="lineeqosinfo_admissionfailure"></span>**lineeqosinfo- \_ admissionfailure**
</dt> <dd> <dl> <dt>

 0x00000002
</dt> <dt>



Die QoS-Anforderung konnte nicht erfüllt werden.


</dt> </dl> </dd> <dt>

<span id="LINEEQOSINFO_POLICYFAILURE"></span><span id="lineeqosinfo_policyfailure"></span>**lineeqosinfo \_ PolicyFailure**
</dt> <dd> <dl> <dt>

 0x00000003
</dt> <dt>



Der angeforderte QoS-Typ wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="LINEEQOSINFO_GENERICERROR"></span><span id="lineeqosinfo_genericerror"></span>**lineeqosinfo \_ genericerror**
</dt> <dd> <dl> <dt>

 0x00000004
</dt> <dt>



Nicht spezifizierter QoS-Fehler.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,2<br/>                                                      |
| Header<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



 

 




