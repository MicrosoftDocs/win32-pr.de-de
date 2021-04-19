---
description: Enthält die Antwort auf eine D3DAUTHENTICATEDQUERY \_ CryptoSession-Abfrage.
ms.assetid: df9d9b41-8188-4597-9e83-d14065eb7fc7
title: D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: fb4e6ccad999f183e71f0f57d64544a70cef5534
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343023"
---
# <a name="d3dauthenticatedchannel_querycryptosession_output-structure"></a>D3DAUTHENTICATEDCHANNEL \_ querycryptosession- \_ Ausgabestruktur

Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY \_ CryptoSession**](d3dauthenticatedquery-cryptosession.md) -Abfrage.

Um diese Abfrage zu senden, nennen Sie [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  HANDLE                               DXVA2DecodeHandle;
  HANDLE                               CryptoSessionHandle;
  HANDLE                               DeviceHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT;
```



## <a name="members"></a>Member

<dl> <dt>

**Ausgabe**
</dt> <dd>

Eine [**D3DAUTHENTICATEDCHANNEL \_ Query- \_ Ausgabe**](d3dauthenticatedchannel-query-output.md) Struktur, die eine Nachrichtenauthentifizierungscode (Mac) und andere Daten enthält.

</dd> <dt>

**DXVA2DecodeHandle**
</dt> <dd>

Ein Handle für ein DirectX Video Acceleration 2-Decodergerät (DXVA-2).

</dd> <dt>

**Cryptosessionhandle**
</dt> <dd>

Ein Handle für die Kryptografiesitzung, die dem Decoder-Gerät zugeordnet ist.

</dd> <dt>

**Geräte**
</dt> <dd>

Ein Handle für das Direct3D-Gerät, das dem Decoder-Gerät zugeordnet ist.

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

 

 




