---
description: Definiert die verschiedenen Bereitschaftszustände der Medienquellenerweiterung.
ms.assetid: 7455B92F-CC2D-4743-935D-F5EBFD834397
title: MF_MSE_READY-Enumeration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MSE_READY
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 28f476c32abbffa8faadd8a7c527f07d81632eee10f1c6cfc54eacc926b4f4e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104576"
---
# <a name="mf_mse_ready-enumeration"></a>MF \_ MSE \_ READY-Enumeration

Definiert die verschiedenen Bereitschaftszustände der Medienquellenerweiterung.

## <a name="syntax"></a>Syntax


```C++
typedef enum _MF_MSE_READY { 
  MF_MSE_READY_CLOSED  = 1,
  MF_MSE_READY_OPEN    = 2,
  MF_MSE_READY_ENDED   = 3
} MF_MSE_READY;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="MF_MSE_READY_CLOSED"></span><span id="mf_mse_ready_closed"></span>**MF \_ MSE \_ READY \_ CLOSED**
</dt> <dd>

Die Medienquelle ist geschlossen.

</dd> <dt>

<span id="MF_MSE_READY_OPEN"></span><span id="mf_mse_ready_open"></span>**MF \_ MSE \_ READY \_ OPEN**
</dt> <dd>

Die Medienquelle ist geöffnet.

</dd> <dt>

<span id="MF_MSE_READY_ENDED"></span><span id="mf_mse_ready_ended"></span>**MF \_ MSE \_ READY \_ BEENDET**
</dt> <dd>

Die Medienquelle wird beendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Enumerationen](media-foundation-enumerations.md)
</dt> </dl>

 

 




