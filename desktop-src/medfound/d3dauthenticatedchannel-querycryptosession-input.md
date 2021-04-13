---
description: Enthält Eingabedaten für eine D3DAUTHENTICATEDQUERY \_ CryptoSession-Abfrage.
ms.assetid: 3a4dead8-fe23-41b4-a167-e0430d09248a
title: D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 76b9d09bcb03dbf3742d551c253d3f4982215757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342528"
---
# <a name="d3dauthenticatedchannel_querycryptosession_input-structure"></a>D3DAUTHENTICATEDCHANNEL \_ querycryptosession- \_ Eingabe Struktur

Enthält Eingabedaten für eine [**D3DAUTHENTICATEDQUERY \_ CryptoSession**](d3dauthenticatedquery-cryptosession.md) -Abfrage.

Um diese Abfrage zu senden, nennen Sie [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  HANDLE                              DXVA2DecodeHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT;
```



## <a name="members"></a>Member

<dl> <dt>

**Input** (Eingabe)
</dt> <dd>

Eine [**D3DAUTHENTICATEDCHANNEL- \_ Abfrage \_ Eingabe**](d3dauthenticatedchannel-query-input.md) Struktur, die die GUID für die Abfrage und andere Daten enthält.

</dd> <dt>

**DXVA2DecodeHandle**
</dt> <dd>

Ein Handle für ein DirectX Video Acceleration 2-Decodergerät (DXVA-2).

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

 

 




