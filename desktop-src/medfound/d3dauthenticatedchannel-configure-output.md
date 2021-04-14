---
description: 'Enthält die Antwort auf einen aufzurufenden Befehl der IDirect3DAuthenticatedChannel9:: Configure-Methode.'
ms.assetid: 6f33d3f7-a883-4aca-a058-b656d745f2b1
title: D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT-Struktur (D3d9types. h)
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
ms.openlocfilehash: 6c7a029bd73069795b83b0b2a330835782192683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342538"
---
# <a name="d3dauthenticatedchannel_configure_output-structure"></a>D3DAUTHENTICATEDCHANNEL \_ Konfigurieren der \_ Ausgabestruktur

Enthält die Antwort auf einen aufzurufenden Befehl der [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) -Methode.

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

## <a name="remarks"></a>Bemerkungen

Für die Member "configure **Retype**", " **hchannel**" und " **SequenceNumber** " verwendet der Treiber dieselben Werte, die von der Anwendung in der [**D3DAUTHENTICATEDCHANNEL- \_ \_ Eingabe**](d3dauthenticatedchannel-configure-input.md) Struktur bereitgestellt werden. Die Anwendung sollte überprüfen, ob diese Werte entsprechen.

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

 

 




