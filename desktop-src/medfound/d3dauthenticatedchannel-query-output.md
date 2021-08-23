---
description: Enthält die Antwort der IDirect3DAuthenticatedChannel9::Query-Methode.
ms.assetid: b2783b8e-0436-419a-a93e-93dc1b87024d
title: D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT-Struktur (D3d9types.h)
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
ms.openlocfilehash: 2defeaf134db9a2464854554db721586f592fc62110d172e0ac804e010804966
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600830"
---
# <a name="d3dauthenticatedchannel_query_output-structure"></a>D3DAUTHENTICATEDCHANNEL \_ QUERY \_ OUTPUT-Struktur

Enthält die Antwort der [**IDirect3DAuthenticatedChannel9::Query-Methode.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)

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

**omac**
</dt> <dd>

Eine [**\_ D3D-OMAC-Struktur,**](d3d-omac.md) die eine Nachrichtenauthentifizierungscode (MAC) der Daten enthält. Der Treiber verwendet AES-basierten CBC MAC (One-Key CBC MAC, OMAC), um diesen Wert für den Datenblock zu berechnen, der nach diesem Strukturmember angezeigt wird.

</dd> <dt>

**QueryType**
</dt> <dd>

Eine GUID, die die Abfrage angibt. Eine Liste der Werte finden Sie unter [Content Protection Abfragen.](content-protection-queries.md)

</dd> <dt>

**Behandeln**
</dt> <dd>

Ein Handle für den authentifizierten Kanal.

</dd> <dt>

**UINT**
</dt> <dd>

Die Abfragesequenznummer.

</dd> <dt>

**ReturnCode**
</dt> <dd>

Der Ergebniscode für die Abfrage.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Für die Member **QueryType,** **hChannel** und **SequenceNumber** verwendet der Treiber in den gleichen Werten, die die Anwendung in der [**D3DAUTHENTICATEDCHANNEL \_ QUERY \_ INPUT-Struktur**](d3dauthenticatedchannel-query-input.md) bereitgestellt hat. Die Anwendung sollte überprüfen, ob diese Werte übereinstimmen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Videostrukturen](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




