---
description: Enthält Eingabedaten für die IDirect3DAuthenticatedChannel9::Configure-Methode.
ms.assetid: 7646100e-f768-4935-9e71-1d9db0d69c52
title: D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT -Struktur (D3d9types.h)
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
ms.openlocfilehash: de968c83fee7ae68dcd756bdf83d529593eeb30b3c2776b03cda812bcd442c50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974739"
---
# <a name="d3dauthenticatedchannel_configure_input-structure"></a>D3DAUTHENTICATEDCHANNEL: \_ KONFIGURIEREN DER \_ EINGABESTRUKTUR

Enthält Eingabedaten für die [**IDirect3DAuthenticatedChannel9::Configure-Methode.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)

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

**omac**
</dt> <dd>

Eine [**\_ D3D-OMAC-Struktur,**](d3d-omac.md) die Nachrichtenauthentifizierungscode (MAC) der Daten enthält. Der Treiber verwendet den AES-basierten CBC MAC (OMAC) mit einem Schlüssel, um diesen Wert für den Datenblock zu berechnen, der nach diesem Strukturmitglied angezeigt wird.

</dd> <dt>

**ConfigureType**
</dt> <dd>

Eine GUID, die den Befehl angibt. Eine Liste der Werte finden Sie unter [Content Protection Befehle](content-protection-commands.md).

</dd> <dt>

**hChannel**
</dt> <dd>

Ein Handle für den authentifizierten Kanal. Um das Handle zu erhalten, rufen [**Sie IDirect3DDevice9Video::CreateAuthenticatedChannel auf.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel)

</dd> <dt>

**SequenceNumber**
</dt> <dd>

Die Abfragesequenznummer. Generieren Sie zu Beginn der Sitzung eine kryptografisch sichere 32-Bit-Zufallszahl, die als Startsequenznummer verwendet werden soll. Erhöhen Sie für jeden Befehl die Sequenznummer um 1.

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

 

 




