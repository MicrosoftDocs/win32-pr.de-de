---
description: Enthält die Antwort auf eine D3DAUTHENTICATEDQUERY \_ PROTECTION-Abfrage.
ms.assetid: eb99089a-5e8e-4970-9c40-7f6a9662b5ec
title: D3DAUTHENTICATEDCHANNEL_QUERYPROTECTION_OUTPUT-Struktur (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYPROTECTION_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 335cd4115f3b66ede4ce34a6ac6b33c86a8b193b88de4314b4902f8c12417358
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828670"
---
# <a name="d3dauthenticatedchannel_queryprotection_output-structure"></a>D3DAUTHENTICATEDCHANNEL \_ QUERYPROTECTION \_ OUTPUT-Struktur

Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY \_ PROTECTION-Abfrage.**](d3dauthenticatedquery-protection.md)

Rufen Sie [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)auf, um diese Abfrage zu senden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYPROTECTION_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT     Output;
  D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS ProtectionFlags;
} D3DAUTHENTICATEDCHANNEL_QUERYPROTECTION_OUTPUT;
```



## <a name="members"></a>Member

<dl> <dt>

**Ausgabe**
</dt> <dd>

Eine [**D3DAUTHENTICATEDCHANNEL \_ QUERY \_ OUTPUT-Struktur,**](d3dauthenticatedchannel-query-output.md) die eine Nachrichtenauthentifizierungscode (MAC) und andere Daten enthält.

</dd> <dt>

**ProtectionFlags**
</dt> <dd>

Eine [**D3DAUTHENTICATEDCHANNEL \_ PROTECTION \_ FLAGS-Struktur,**](d3dauthenticatedchannel-protection-flags.md) die die Schutzebene angibt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Videostrukturen](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




