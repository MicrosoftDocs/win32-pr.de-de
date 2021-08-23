---
description: Enthält Eingabedaten für eine D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS-Abfrage.
ms.assetid: a1ceb394-7af9-4f05-9f58-a3103bf0150e
title: D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT -Struktur (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 361b107b527fc1a4ecd37ee564dd440447a9233e55f9ae4027933a57fd715b9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958760"
---
# <a name="d3dauthenticatedchannel_queryrestrictedsharedresourceprocess_input-structure"></a>D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS-EINGABEstruktur \_

Enthält Eingabedaten für eine [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS-Abfrage.**](d3dauthenticatedquery-restrictedsharedresourceprocess.md)

Rufen Sie zum Senden dieser Abfrage [**IDirect3DAuthenticatedChannel9::Query auf.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  UINT                                ProcessIndex;
} D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT;
```



## <a name="members"></a>Member

<dl> <dt>

**Input** (Eingabe)
</dt> <dd>

Eine [**D3DAUTHENTICATEDCHANNEL \_ QUERY \_ INPUT-Struktur,**](d3dauthenticatedchannel-query-input.md) die die GUID für die Abfrage und andere Daten enthält.

</dd> <dt>

**ProcessIndex**
</dt> <dd>

Der Index des Prozesses.

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

 

 




