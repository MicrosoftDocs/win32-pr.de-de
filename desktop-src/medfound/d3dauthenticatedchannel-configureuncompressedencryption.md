---
description: Enthält Eingabedaten für den Befehl D3DAUTHENTICATEDCONFIGURE \_ ENCRYPTIONWHENACCESSIBLE.
ms.assetid: d2d0adff-5d4d-4af3-b6b8-b8c60a506142
title: D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION-Struktur (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 661f4cd043a2337aa499aaa165c16d2e1fdf41f8e87826412250ea0fe85c47a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062000"
---
# <a name="d3dauthenticatedchannel_configureuncompressedencryption-structure"></a>D3DAUTHENTICATEDCHANNEL \_ CONFIGUREUNCOMGABEDENCRYPTION-Struktur

Enthält Eingabedaten für den Befehl [**D3DAUTHENTICATEDCONFIGURE \_ ENCRYPTIONWHENACCESSIBLE.**](d3dauthenticatedconfigure-encryptionwhenaccessible.md)

Rufen Sie [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)auf, um diese Abfrage zu senden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT Parameters;
  GUID                                    EncryptionGuid;
} D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION;
```



## <a name="members"></a>Member

<dl> <dt>

**Parameter**
</dt> <dd>

Eine [**D3DAUTHENTICATEDCHANNEL \_ CONFIGURE \_ INPUT-Struktur,**](d3dauthenticatedchannel-configure-input.md) die die Befehls-GUID und andere Daten enthält.

</dd> <dt>

**EncryptionGuid**
</dt> <dd>

Eine GUID, die den Typ der anzuwendenden Verschlüsselung angibt.

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

[**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




