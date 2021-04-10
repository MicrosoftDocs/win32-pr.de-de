---
description: 'Enthält Eingabedaten für die IDirect3DAuthenticatedChannel9:: Query-Methode.'
ms.assetid: 6a484652-8da2-4074-96b2-6fe49f4d4200
title: D3DAUTHENTICATEDCHANNEL_QUERY_INPUT-Struktur (D3d9types. h)
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
ms.openlocfilehash: a0bec356b20569b5638848407eff27e930ef76b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214326"
---
# <a name="d3dauthenticatedchannel_query_input-structure"></a>D3DAUTHENTICATEDCHANNEL- \_ Abfrage \_ Eingabe Struktur

Enthält Eingabedaten für die [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) -Methode.

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

Eine GUID, die die Abfrage angibt. Eine Liste der-Werte finden Sie unter [Content Protection-Abfragen](content-protection-queries.md).

</dd> <dt>

**Bewältigen**
</dt> <dd>

Ein Handle für den authentifizierten Kanal. Um das Handle abzurufen, nennen Sie [**IDirect3DDevice9Video:: kreateauthentiinitiedchannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).

</dd> <dt>

**UINT**
</dt> <dd>

Die Abfrage Sequenznummer. Generieren Sie zu Beginn der Sitzung eine kryptografisch sichere 32-Bit-Zufallszahl, die als Startsequenz Nummer verwendet wird. Erhöhen Sie für jede Abfrage die Sequenznummer um 1.

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

 

 




