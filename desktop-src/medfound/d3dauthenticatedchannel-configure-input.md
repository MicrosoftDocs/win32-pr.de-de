---
description: 'Enthält Eingabedaten für die IDirect3DAuthenticatedChannel9:: Configure-Methode.'
ms.assetid: 7646100e-f768-4935-9e71-1d9db0d69c52
title: D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 82cd60dbb65517beb65a3a7cb413e1d93ac72062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214328"
---
# <a name="d3dauthenticatedchannel_configure_input-structure"></a>D3DAUTHENTICATEDCHANNEL \_ Konfigurieren der \_ Eingabe Struktur

Enthält Eingabedaten für die [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) -Methode.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT {
  D3D_OMAC omac;
  GUID     ConfigureType;
  HANDLE   hChannel;
  UINT     SequenceNumber;
} D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT;
```



## <a name="members"></a>Member

<dl> <dt>

**OMAC**
</dt> <dd>

Eine [**D3D \_ OMAC**](d3d-omac.md) -Struktur, die einen Nachrichtenauthentifizierungscode (Mac) der Daten enthält. Der Treiber verwendet einen AES-basierten, einstufigen CBC-MAC (OMAC), um diesen Wert für den Datenblock zu berechnen, der nach diesem Strukturmember angezeigt wird.

</dd> <dt>

**Konfiguriertyp**
</dt> <dd>

Eine GUID, die den Befehl angibt. Eine Liste der Werte finden Sie unter [Content Protection-Befehle](content-protection-commands.md).

</dd> <dt>

**hchannel**
</dt> <dd>

Ein Handle für den authentifizierten Kanal. Um das Handle abzurufen, nennen Sie [**IDirect3DDevice9Video:: kreateauthentiinitiedchannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).

</dd> <dt>

**SequenceNumber**
</dt> <dd>

Die Abfrage Sequenznummer. Generieren Sie zu Beginn der Sitzung eine kryptografisch sichere 32-Bit-Zufallszahl, die als Startsequenz Nummer verwendet wird. Erhöhen Sie die Sequenznummer für jeden Befehl um 1.

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

 

 




