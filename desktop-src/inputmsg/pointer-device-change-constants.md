---
title: Zeigergeräteänderung
description: Werte, die im wParam-Parameter der WM_POINTERDEVICECHANGE Nachricht übergeben werden können.
ms.assetid: B95191D7-820B-445A-A3A4-811F9F1A8C4F
topic_type:
- apiref
api_name:
- PDC_ARRIVAL
- PDC_REMOVAL
- PDC_ORIENTATION_0
- PDC_ORIENTATION_90
- PDC_ORIENTATION_180
- PDC_ORIENTATION_270
- PDC_MODE_DEFAULT
- PDC_MODE_CENTERED
- PDC_MAPPING_CHANGE
- PDC_RESOLUTION
- PDC_ORIGIN
- PDC_MODE_ASPECTRATIOPRESERVED
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 67dc120a4541b56638c2947c24534c9f42543533b4b1a97ace72297aaf48341c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602550"
---
# <a name="pointer-device-change"></a>Zeigergeräteänderung

Werte, die im *wParam-Parameter* der [**WM_POINTERDEVICECHANGE**](wm-pointerdevicechange.md) Nachricht übergeben werden können.

<dl> <dt>

<span id="PDC_ARRIVAL"></span><span id="pdc_arrival"></span>**PDC_ARRIVAL**
</dt> <dd> <dl> <dt>

0x001
</dt> <dt>



Ein neues Gerät ist angefügt.


</dt> </dl> </dd> <dt>

<span id="PDC_REMOVAL"></span><span id="pdc_removal"></span>**PDC_REMOVAL**
</dt> <dd> <dl> <dt>

0x002
</dt> <dt>



Ein Gerät wurde getrennt.


</dt> </dl> </dd> <dt>

<span id="PDC_ORIENTATION_0"></span><span id="pdc_orientation_0"></span>**PDC_ORIENTATION_0**
</dt> <dd> <dl> <dt>

0x004
</dt> <dt>



Ausrichtung des Geräts.


</dt> </dl> </dd> <dt>

<span id="PDC_ORIENTATION_90"></span><span id="pdc_orientation_90"></span>**PDC_ORIENTATION_90**
</dt> <dd> <dl> <dt>

0x008
</dt> <dt>



Ausrichtung des Geräts.


</dt> </dl> </dd> <dt>

<span id="PDC_ORIENTATION_180"></span><span id="pdc_orientation_180"></span>**PDC_ORIENTATION_180**
</dt> <dd> <dl> <dt>

0x010
</dt> <dt>



Ausrichtung des Geräts.


</dt> </dl> </dd> <dt>

<span id="PDC_ORIENTATION_270"></span><span id="pdc_orientation_270"></span>**PDC_ORIENTATION_270**
</dt> <dd> <dl> <dt>

0x020
</dt> <dt>



Ausrichtung des Geräts.


</dt> </dl> </dd> <dt>

<span id="PDC_MODE_DEFAULT"></span><span id="pdc_mode_default"></span>**PDC_MODE_DEFAULT**
</dt> <dd> <dl> <dt>

0x040
</dt> <dt>



Der Standardanzeigemodus.


</dt> </dl> </dd> <dt>

<span id="PDC_MODE_CENTERED"></span><span id="pdc_mode_centered"></span>**PDC_MODE_CENTERED**
</dt> <dd> <dl> <dt>

0x080
</dt> <dt>



Zentrierter Anzeigemodus.


</dt> </dl> </dd> <dt>

<span id="PDC_MAPPING_CHANGE"></span><span id="pdc_mapping_change"></span>**PDC_MAPPING_CHANGE**
</dt> <dd> <dl> <dt>

0x100
</dt> <dt>



Die Änderung der Anzeige in die Digitizerzuordnung.


</dt> </dl> </dd> <dt>

<span id="PDC_RESOLUTION"></span><span id="pdc_resolution"></span>**PDC_RESOLUTION**
</dt> <dd> <dl> <dt>

0x200
</dt> <dt>



Anzeigeauflösung.


</dt> </dl> </dd> <dt>

<span id="PDC_ORIGIN"></span><span id="pdc_origin"></span>**PDC_ORIGIN**
</dt> <dd> <dl> <dt>

0x400
</dt> <dt>



Der Anzeigeursprung.


</dt> </dl> </dd> <dt>

<span id="PDC_MODE_ASPECTRATIOPRESERVED"></span><span id="pdc_mode_aspectratiopreserved"></span>**PDC_MODE_ASPECTRATIOPRESERVED**
</dt> <dd> <dl> <dt>

0x800
</dt> <dt>



Das Seitenverhältnis der Anzeige.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Konstanten](constants.md)
</dt> <dt>

[**POINTER_INFO**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





