---
description: Enthält die Antwort auf eine D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES-Abfrage.
ms.assetid: 9f66a467-ba05-413b-b001-ea4c5ca4a37d
title: D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT-Struktur (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 1f4d7a0f8ceadc4e40ceaf327b7dc45fd10bd3427620971b16c5a02659c0a067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828710"
---
# <a name="d3dauthenticatedchannel_queryinfobustype_output-structure"></a>D3DAUTHENTICATEDCHANNEL \_ \_ QUERYINFOBUSTYPE-AUSGABEstruktur

Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES-Abfrage.**](d3dauthenticatedquery-accessibilityattributes.md)

Rufen Sie [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)auf, um diese Abfrage zu senden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  D3DBUSTYPE                           BusType;
  BOOL                                 bAccessibleInContiguousBlocks;
  BOOL                                 bAccessibleInNonContiguousBlocks;
} D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT;
```



## <a name="members"></a>Member

<dl> <dt>

**Ausgabe**
</dt> <dd>

Eine [**D3DAUTHENTICATEDCHANNEL \_ QUERY \_ OUTPUT-Struktur,**](d3dauthenticatedchannel-query-output.md) die eine Nachrichtenauthentifizierungscode (MAC) und andere Daten enthält.

</dd> <dt>

**BusType**
</dt> <dd>

Ein bitweises **OR** von Flags aus der [**D3DBUSTYPE-Enumeration.**](d3dbustype.md)

</dd> <dt>

**bAccessibleInContiguousBlocks**
</dt> <dd>

**True** gibt an, dass die CPU oder der Bus möglicherweise auf zusammenhängende Videospeicherblöcke zugreifen können.

</dd> <dt>

**bAccessibleInNonContiguousBlocks**
</dt> <dd>

True gibt an, dass die CPU oder der Bus möglicherweise auf nicht zusammenhängende Videospeicherblöcke zugreifen kann.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Videostrukturen](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




