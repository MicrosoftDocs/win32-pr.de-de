---
description: Enthält Eingabedaten für eine D3DAUTHENTICATEDQUERY \_ restrictedsharedresourceprocess-Abfrage.
ms.assetid: a1ceb394-7af9-4f05-9f58-a3103bf0150e
title: D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT-Struktur (D3d9types. h)
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
ms.openlocfilehash: 06c4421f048af80186077da022fdecfaea79dca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346047"
---
# <a name="d3dauthenticatedchannel_queryrestrictedsharedresourceprocess_input-structure"></a>D3DAUTHENTICATEDCHANNEL \_ queryrestrictedsharedresourceprocess- \_ Eingabe Struktur

Enthält Eingabedaten für eine [**D3DAUTHENTICATEDQUERY \_ restrictedsharedresourceprocess**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) -Abfrage.

Um diese Abfrage zu senden, nennen Sie [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

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

Eine [**D3DAUTHENTICATEDCHANNEL- \_ Abfrage \_ Eingabe**](d3dauthenticatedchannel-query-input.md) Struktur, die die GUID für die Abfrage und andere Daten enthält.

</dd> <dt>

**Processindex**
</dt> <dd>

Der Index des Prozesses.

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

[**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




