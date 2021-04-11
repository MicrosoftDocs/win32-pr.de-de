---
description: 'Enthält die Antwort der IDirect3DAuthenticatedChannel9:: Query-Methode.'
ms.assetid: b2783b8e-0436-419a-a93e-93dc1b87024d
title: D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 79fe02a483ade1ff60107287799624017496887b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127936"
---
# <a name="d3dauthenticatedchannel_query_output-structure"></a>D3DAUTHENTICATEDCHANNEL- \_ Abfrage \_ Ausgabestruktur

Enthält die Antwort der [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) -Methode.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT {
  D3D_OMAC       omac;
  GUID           QueryType;
  hChannel       HANDLE;
  SequenceNumber UINT;
  HRESULT        ReturnCode;
} D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
```



## <a name="members"></a>Member

<dl> <dt>

**OMAC**
</dt> <dd>

Eine [**D3D \_ OMAC**](d3d-omac.md) -Struktur, die einen Nachrichtenauthentifizierungscode (Mac) der Daten enthält. Der Treiber verwendet einen AES-basierten, einstufigen CBC-MAC (OMAC), um diesen Wert für den Datenblock zu berechnen, der nach diesem Strukturmember angezeigt wird.

</dd> <dt>

**QueryType**
</dt> <dd>

Eine GUID, die die Abfrage angibt. Eine Liste der-Werte finden Sie unter [Content Protection-Abfragen](content-protection-queries.md).

</dd> <dt>

**Bewältigen**
</dt> <dd>

Ein Handle für den authentifizierten Kanal.

</dd> <dt>

**UINT**
</dt> <dd>

Die Abfrage Sequenznummer.

</dd> <dt>

**ReturnCode**
</dt> <dd>

Der Ergebniscode für die Abfrage.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Bei den **memytype**-, **hchannel**-und **sequencenenumdermembern** verwendet der Treiber die gleichen Werte, die von der Anwendung in der [**D3DAUTHENTICATEDCHANNEL- \_ Abfrage \_ Eingabe**](d3dauthenticatedchannel-query-input.md) Struktur bereitgestellt werden. Die Anwendung sollte überprüfen, ob diese Werte entsprechen.

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

 

 




