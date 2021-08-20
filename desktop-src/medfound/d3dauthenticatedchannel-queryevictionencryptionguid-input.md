---
description: Enthält Eingabedaten für eine D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID-Abfrage.
ms.assetid: 0e24e393-3f63-4c6f-aca1-f73ced3490ba
title: D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_INPUT -Struktur (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: d1fed28e4ff36fbd7798870d7fcdfff4d3a90d77d4d43b859ae2f6f754af4e2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880149"
---
# <a name="d3dauthenticatedchannel_queryevictionencryptionguid_input-structure"></a>D3DAUTHENTICATEDCHANNEL \_ QUERYEVICTIONENCRYPTIONGUID \_ INPUT-Struktur

Enthält Eingabedaten für eine [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID-Abfrage.**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md)

Rufen Sie zum Senden dieser Abfrage [**IDirect3DAuthenticatedChannel9::Query auf.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  UINT                                EncryptionGuidIndex;
} D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_INPUT;
```



## <a name="members"></a>Member

<dl> <dt>

**Input** (Eingabe)
</dt> <dd>

Eine [**D3DAUTHENTICATEDCHANNEL \_ QUERY \_ INPUT-Struktur,**](d3dauthenticatedchannel-query-input.md) die die GUID für die Abfrage und andere Daten enthält.

</dd> <dt>

**EncryptionGuidIndex**
</dt> <dd>

Der Index der Verschlüsselungs-GUID.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Videostrukturen](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




