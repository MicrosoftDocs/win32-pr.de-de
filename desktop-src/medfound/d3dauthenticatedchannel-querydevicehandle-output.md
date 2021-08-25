---
description: Enthält die Antwort auf eine D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE-Abfrage.
ms.assetid: f2e0ae6c-dc97-46f7-933f-6c14d83adf18
title: D3DAUTHENTICATEDCHANNEL_QUERYDEVICEHANDLE_OUTPUT -Struktur (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYDEVICEHANDLE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: bf3879051a2fee3e60850d6d2a8290c924ababd6ef591d76f56f23642d646826
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828720"
---
# <a name="d3dauthenticatedchannel_querydevicehandle_output-structure"></a>D3DAUTHENTICATEDCHANNEL \_ QUERYDEVICEHANDLE \_ OUTPUT-Struktur

Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE-Abfrage.**](d3dauthenticatedquery-devicehandle.md)

Rufen Sie zum Senden dieser Abfrage [**IDirect3DAuthenticatedChannel9::Query auf.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYDEVICEHANDLE_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  HANDLE                               DeviceHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYDEVICEHANDLE_OUTPUT;
```



## <a name="members"></a>Member

<dl> <dt>

**Ausgabe**
</dt> <dd>

Eine [**D3DAUTHENTICATEDCHANNEL-ABFRAGEAUSGABEstruktur, \_ \_**](d3dauthenticatedchannel-query-output.md) die einen Nachrichtenauthentifizierungscode (MAC) und andere Daten enthält.

</dd> <dt>

**DeviceHandle**
</dt> <dd>

Ein Handle für das Gerät.

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

 

 




