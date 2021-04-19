---
description: Enthält Eingabedaten für den D3DAUTHENTICATEDCONFIGURE- \_ Befehl verschlüsselungszugreif barkeit.
ms.assetid: d2d0adff-5d4d-4af3-b6b8-b8c60a506142
title: D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION-Struktur (D3d9types. h)
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
ms.openlocfilehash: 6c8ea4360ff7f2bbcf2c03040671013473e9873a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339722"
---
# <a name="d3dauthenticatedchannel_configureuncompressedencryption-structure"></a>D3DAUTHENTICATEDCHANNEL \_ Konfiguration reuncompressedencryption-Struktur

Enthält Eingabedaten für den [**D3DAUTHENTICATEDCONFIGURE-Befehl \_ verschlüsselungszugreif**](d3dauthenticatedconfigure-encryptionwhenaccessible.md) barkeit.

Um diese Abfrage zu senden, nennen Sie [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).

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

Eine [**D3DAUTHENTICATEDCHANNEL \_ - \_ Eingabe**](d3dauthenticatedchannel-configure-input.md) Struktur, die die Befehls-GUID und andere Daten enthält.

</dd> <dt>

**Verschlüsselungs-GUID**
</dt> <dd>

Eine GUID, die den Typ der anzuwendenden Verschlüsselung angibt.

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

[**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




