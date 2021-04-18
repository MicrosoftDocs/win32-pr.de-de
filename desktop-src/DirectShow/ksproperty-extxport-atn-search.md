---
description: Diese Eigenschaft sendet einen Befehl an das Gerät, um nach einer absoluten Nachverfolgung zu suchen (ATN). Der UVC-Gerätetreiber unterstützt diese Eigenschaft.
ms.assetid: 209e0aa3-d7a3-4b5c-ae5a-5063a3804a9d
title: KSPROPERTY_EXTXPORT_ATN_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc8ff454386c444ed6b55bfbeede60196a75127c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344770"
---
# <a name="ksproperty_extxport_atn_search"></a>ksproperty \_ extxport- \_ Atn- \_ Suche

Diese Eigenschaft sendet einen Befehl an das Gerät, um nach einer absoluten Nachverfolgung zu suchen (ATN). Der UVC-Gerätetreiber unterstützt diese Eigenschaft.



|                   |                                       |
|-------------------|---------------------------------------|
| Eigenschaftensatz-GUID | propseetid- \_ Ext- \_ Transport             |
| Eigenschafts-ID       | ksproperty \_ extxport- \_ Atn- \_ Suche     |
| Datentyp         | **Ksproperty \_ Extxport \_ S** -Struktur |



 

## <a name="remarks"></a>Bemerkungen

Legen Sie den **dwabstracknumber** -Member der **ksproperty \_ extxport \_ S** -Struktur auf den folgenden Wert fest:


```
(absolute track number << 1) + continuity bit
```



Die UVC-Spezifikation definiert nicht, wie das Gerät das Kontinuitäts Bit verwendet. Die Struktur von **ksproperty \_ extxport \_ S** wird im Windows-DDK beschrieben.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften Satz für externen Geräte Transport](external-device-transport-property-set.md)
</dt> </dl>

 

 



