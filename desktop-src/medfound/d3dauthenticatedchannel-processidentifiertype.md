---
description: Gibt den Typ des Prozesses an, der in der D3DAUTHENTICATEDCHANNEL \_ queryrestrictedsharedresourceprocess- \_ Ausgabestruktur identifiziert wird.
ms.assetid: 8878905e-f55b-4dbc-9608-da0082daf673
title: D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE-Enumeration (D3d9types. h)
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
ms.openlocfilehash: 1b2fdb7384ff868b02f54650de9662b297ce39db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127937"
---
# <a name="d3dauthenticatedchannel_processidentifiertype-enumeration"></a>D3DAUTHENTICATEDCHANNEL \_ processidentifiertype-Enumeration

Gibt den Typ des Prozesses an, der in der [**D3DAUTHENTICATEDCHANNEL \_ queryrestrictedsharedresourceprocess- \_ Ausgabe**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md) Struktur identifiziert wird.

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

<span id="PROCESSIDTYPE_UNKNOWN"></span><span id="processidtype_unknown"></span>**der processidtype ist \_ unbekannt.**
</dt> <dd>

Unbekannter Prozesstyp.

</dd> <dt>

<span id="PROCESSIDTYPE_DWM"></span><span id="processidtype_dwm"></span>**processidtype \_ DWM**
</dt> <dd>

Desktopfenster-Manager (DWM)-Prozess.

</dd> <dt>

<span id="PROCESSIDTYPE_HANDLE"></span><span id="processidtype_handle"></span>**processidtype- \_ handle**
</dt> <dd>

Handle für einen Prozess.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>D3d9types. h (Include d3d9. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-videoenumerationen](direct3d-video-enumerations.md)
</dt> </dl>

 

 




