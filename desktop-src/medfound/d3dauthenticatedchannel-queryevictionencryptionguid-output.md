---
description: Enthält die Antwort auf eine D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID-Abfrage.
ms.assetid: afe73f8e-3304-470c-a37a-17b6c767b2c0
title: D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT-Struktur (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 01624b35b7c1b29267b490204a2d814adec1c7075eaf23e746e6ade04ceb0c6a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942770"
---
# <a name="d3dauthenticatedchannel_queryevictionencryptionguid_output-structure"></a>D3DAUTHENTICATEDCHANNEL \_ QUERYEVICTIONENCRYPTIONGUID-AUSGABEstruktur \_

Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID-Abfrage.**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md)

Rufen Sie [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)auf, um diese Abfrage zu senden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT {
  Output D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
  UINT   EncryptionGuidIndex;
  GUID   EncryptionGuid;
} D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT;
```



## <a name="members"></a>Member

<dl> <dt>

**D3DAUTHENTICATEDCHANNEL-ABFRAGEAUSGABE \_ \_**
</dt> <dd>

Eine [**D3DAUTHENTICATEDCHANNEL \_ QUERY \_ OUTPUT-Struktur,**](d3dauthenticatedchannel-query-output.md) die eine Nachrichtenauthentifizierungscode (MAC) und andere Daten enthält.

</dd> <dt>

**EncryptionGuidIndex**
</dt> <dd>

Der Index der Verschlüsselungs-GUID.

</dd> <dt>

**EncryptionGuid**
</dt> <dd>

Eine GUID, die einen unterstützten Verschlüsselungstyp angibt.

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

 

 




