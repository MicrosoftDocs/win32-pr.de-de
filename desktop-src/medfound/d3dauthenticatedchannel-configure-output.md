---
description: Enthält die Antwort auf einen Aufruf der IDirect3DAuthenticatedChannel9::Configure-Methode.
ms.assetid: 6f33d3f7-a883-4aca-a058-b656d745f2b1
title: D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT -Struktur (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a849967e798db0ae0364e843221bfe2bf0f3305f773a784b6330a21bb84e5427
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942930"
---
# <a name="d3dauthenticatedchannel_configure_output-structure"></a>D3DAUTHENTICATEDCHANNEL: \_ \_ AUSGABEstruktur konfigurieren

Enthält die Antwort auf einen Aufruf der [**IDirect3DAuthenticatedChannel9::Configure-Methode.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT {
  D3D_OMAC omac;
  GUID     ConfigureType;
  HANDLE   hChannel;
  UINT     SequenceNumber;
  HRESULT  ReturnCode;
} D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT;
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

Ein Handle für den authentifizierten Kanal.

</dd> <dt>

**SequenceNumber**
</dt> <dd>

Die Sequenznummer des Befehls.

</dd> <dt>

**ReturnCode**
</dt> <dd>

Der Ergebniscode für den Befehl.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Für **die ConfigureType-,** **hChannel-** und **SequenceNumber-Member** verwendet der Treiber dieselben Werte, die die Anwendung in der [**D3DAUTHENTICATEDCHANNEL \_ CONFIGURE \_ INPUT-Struktur**](d3dauthenticatedchannel-configure-input.md) bereitgestellt hat. Die Anwendung sollte überprüfen, ob diese Werte übereinstimmen.

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

 

 




