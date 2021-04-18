---
description: Enthält die Antwort auf eine D3DAUTHENTICATEDQUERY \_ accessibilityattributabfrage.
ms.assetid: 9f66a467-ba05-413b-b001-ea4c5ca4a37d
title: D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT-Struktur (D3d9types. h)
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
ms.openlocfilehash: 853488c98687825ab55d642b2e01e569f0d435c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341161"
---
# <a name="d3dauthenticatedchannel_queryinfobustype_output-structure"></a>D3DAUTHENTICATEDCHANNEL \_ queryinfobustype- \_ Ausgabestruktur

Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY \_ accessibilityattributabfrage**](d3dauthenticatedquery-accessibilityattributes.md) .

Um diese Abfrage zu senden, nennen Sie [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

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

Eine [**D3DAUTHENTICATEDCHANNEL \_ Query- \_ Ausgabe**](d3dauthenticatedchannel-query-output.md) Struktur, die eine Nachrichtenauthentifizierungscode (Mac) und andere Daten enthält.

</dd> <dt>

**BusType**
</dt> <dd>

Ein bitweises **or** von-Flags aus der [**D3DBUSTYPE**](d3dbustype.md) -Enumeration.

</dd> <dt>

**baccessiblancontiguousblocks**
</dt> <dd>

**True** gibt an, dass die CPU oder der Bus auf zusammenhängende Blöcke des Video Speichers zugreifen können.

</dd> <dt>

**baccessiblannoncontiguousblocks**
</dt> <dd>

**True** gibt an, dass die CPU oder der Bus auf nicht zusammenhängende Blöcke des Video Speichers zugreifen können.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Video Strukturen](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




