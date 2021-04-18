---
title: Steuerelement Zustände des Registerkarten Steuer Elements (kommstrg. h)
description: Registerkarten-Steuerelemente unterstützen nun einen Element Zustand zur Unterstützung der TCM- \_ DeselectAll-Nachricht. Außerdem unterstützt die TCITEM-Strukturelement Zustands Werte.
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
ms.openlocfilehash: d5214f1a2eee757bfdf5b2a81a8916292b9d7f98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358365"
---
# <a name="tab-control-item-states"></a>Steuerelement Zustände von Registerkarten

Registerkarten-Steuerelemente unterstützen nun einen Element Zustand zur Unterstützung der [**TCM- \_ DeselectAll**](tcm-deselectall.md) -Nachricht. Außerdem unterstützt die [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) -Strukturelement Zustands Werte.



| Konstante                                                                                                                                                                     | BESCHREIBUNG                                                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCIS_BUTTONPRESSED"></span><span id="tcis_buttonpressed"></span><dl> <dt>**tcis- \_ ButtonPressed**</dt> </dl> | [Version 4,70](common-control-versions.md). Das Registerkarten-Steuerelement ist ausgewählt. Dieser Status ist nur dann sinnvoll, wenn das Style-Flag der [**TCS- \_ Schalt**](tab-control-styles.md) Flächen festgelegt wurde.<br/>                                 |
| <span id="TCIS_HIGHLIGHTED"></span><span id="tcis_highlighted"></span><dl> <dt>**tcis \_ hervorgehoben**</dt> </dl>       | [Version 4,71](common-control-versions.md). Das Registerkarten-Steuerelement wird hervorgehoben, und die Registerkarte und der Text werden mithilfe der aktuellen Hervorhebungs Farbe gezeichnet. Wenn Sie High-Color verwenden, handelt es sich hierbei um eine echte Interpolations-und nicht um eine Dithering-Farbe.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





