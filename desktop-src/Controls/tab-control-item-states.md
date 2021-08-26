---
title: Elementzustände des Registerkartensteuerelements (CommCtrl.h)
description: Registerkartensteuerelement unterstützen jetzt einen Elementzustand zur Unterstützung der \_ TCM-DESELECTALL-Nachricht. Darüber hinaus unterstützt die TCITEM-Struktur Elementzustandswerte.
ms.assetid: c4181fe6-0055-45c9-a3d0-8cda051383f2
topic_type:
- apiref
api_name:
- TCIS_BUTTONPRESSED
- TCIS_HIGHLIGHTED
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75f3bba0ecd29c7ab84c6b68010f8af52c8db2cfc9dc4080fb73e37b408ee1a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919280"
---
# <a name="tab-control-item-states"></a>Elementzustände des Registerkartensteuerelements

Registerkartensteuerelement unterstützen jetzt einen Elementzustand zur Unterstützung der [**\_ TCM-DESELECTALL-Nachricht.**](tcm-deselectall.md) Darüber hinaus unterstützt die [**TCITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tcitema) Elementzustandswerte.



| Konstante                                                                                                                                                                     | BESCHREIBUNG                                                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCIS_BUTTONPRESSED"></span><span id="tcis_buttonpressed"></span><dl> <dt>**TCIS \_ BUTTONPRESSED**</dt> </dl> | [Version 4.70.](common-control-versions.md) Das Registerkartensteuerelement ist ausgewählt. Dieser Zustand ist nur sinnvoll, wenn das [**TCS \_ BUTTONS-Stilflag**](tab-control-styles.md) festgelegt wurde.<br/>                                 |
| <span id="TCIS_HIGHLIGHTED"></span><span id="tcis_highlighted"></span><dl> <dt>**TCIS \_ HERVORGEHOBEN**</dt> </dl>       | [Version 4.71.](common-control-versions.md) Das Registerkartensteuerelement wird hervorgehoben, und die Registerkarte und der Text werden mit der aktuellen Hervorhebungsfarbe gezeichnet. Bei Verwendung von hoher Farbe ist dies eine echte Interpolation, keine geblendete Farbe.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





