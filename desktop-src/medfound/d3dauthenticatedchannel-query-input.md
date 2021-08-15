---
description: Enthält Eingabedaten für die IDirect3DAuthenticatedChannel9::Query-Methode.
ms.assetid: 6a484652-8da2-4074-96b2-6fe49f4d4200
title: D3DAUTHENTICATEDCHANNEL_QUERY_INPUT -Struktur (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERY_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 50f9c781ca6d495acd06d3aa67c337dee76b2310f5399615599a52e15000382c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974688"
---
# <a name="d3dauthenticatedchannel_query_input-structure"></a>D3DAUTHENTICATEDCHANNEL-ABFRAGEEINGABEstruktur \_ \_

Enthält Eingabedaten für die [**IDirect3DAuthenticatedChannel9::Query-Methode.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERY_INPUT {
  GUID           QueryType;
  hChannel       HANDLE;
  SequenceNumber UINT;
} D3DAUTHENTICATEDCHANNEL_QUERY_INPUT;
```



## <a name="members"></a>Member

<dl> <dt>

**QueryType**
</dt> <dd>

Eine GUID, die die Abfrage angibt. Eine Liste der Werte finden Sie unter [Content Protection Abfragen](content-protection-queries.md).

</dd> <dt>

**Behandeln**
</dt> <dd>

Ein Handle für den authentifizierten Kanal. Um das Handle zu erhalten, rufen [**Sie IDirect3DDevice9Video::CreateAuthenticatedChannel auf.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel)

</dd> <dt>

**UINT**
</dt> <dd>

Die Abfragesequenznummer. Generieren Sie zu Beginn der Sitzung eine kryptografisch sichere 32-Bit-Zufallszahl, die als Startsequenznummer verwendet werden soll. Erhöhen Sie für jede Abfrage die Sequenznummer um 1.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Videostrukturen](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




