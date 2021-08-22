---
description: Enthält Eingabedaten für einen D3DAUTHENTICATEDCONFIGURE \_ PROTECTION-Befehl.
ms.assetid: 44f37e78-7218-42be-a07a-5ab911f2ba21
title: D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION -Struktur (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 3f7c202a29347d59bfaf79792806fcab56532637045985440c899eeae304a4e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828770"
---
# <a name="d3dauthenticatedchannel_configureprotection-structure"></a>D3DAUTHENTICATEDCHANNEL \_ CONFIGUREPROTECTION-Struktur

Enthält Eingabedaten für einen [**D3DAUTHENTICATEDCONFIGURE \_ PROTECTION-Befehl.**](d3dauthenticatedconfigure-protection.md)

Rufen Sie zum Senden dieser Abfrage [**IDirect3DAuthenticatedChannel9::Configure auf.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT  Parameters;
  D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS Protections;
} D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION;
```



## <a name="members"></a>Member

<dl> <dt>

**Parameter**
</dt> <dd>

Eine [**D3DAUTHENTICATEDCHANNEL \_ CONFIGURE \_ INPUT-Struktur,**](d3dauthenticatedchannel-configure-input.md) die die Befehls-GUID und andere Daten enthält.

</dd> <dt>

**Schutz**
</dt> <dd>

Eine [**D3DAUTHENTICATEDCHANNEL \_ PROTECTION \_ FLAGS-Struktur,**](d3dauthenticatedchannel-protection-flags.md) die die Schutzebene angibt.

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

[**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




