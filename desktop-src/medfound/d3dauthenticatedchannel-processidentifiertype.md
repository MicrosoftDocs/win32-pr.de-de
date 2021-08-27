---
description: Gibt den Prozesstyp an, der in der D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_ OUTPUT-Struktur identifiziert wird.
ms.assetid: 8878905e-f55b-4dbc-9608-da0082daf673
title: D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE -Enumeration (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 522fee8421ec61b58bd67065c31b968252c2c7d563e94f7eda7a9f5105d20382
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061980"
---
# <a name="d3dauthenticatedchannel_processidentifiertype-enumeration"></a>D3DAUTHENTICATEDCHANNEL \_ PROCESSIDENTIFIERTYPE-Enumeration

Gibt den Prozesstyp an, der in der [**D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_ OUTPUT-Struktur identifiziert**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md) wird.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  PROCESSIDTYPE_UNKNOWN  = 0,
  PROCESSIDTYPE_DWM      = 1,
  PROCESSIDTYPE_HANDLE   = 2
} D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="PROCESSIDTYPE_UNKNOWN"></span><span id="processidtype_unknown"></span>**PROCESSIDTYPE \_ UNKNOWN**
</dt> <dd>

Unbekannter Prozesstyp.

</dd> <dt>

<span id="PROCESSIDTYPE_DWM"></span><span id="processidtype_dwm"></span>**PROCESSIDTYPE \_ DWM**
</dt> <dd>

Desktopfenster-Manager (DWM)-Prozess.

</dd> <dt>

<span id="PROCESSIDTYPE_HANDLE"></span><span id="processidtype_handle"></span>**PROCESSIDTYPE \_ HANDLE**
</dt> <dd>

Handle für einen Prozess.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>D3d9types.h (include D3d9.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Videoenumeration](direct3d-video-enumerations.md)
</dt> </dl>

 

 




