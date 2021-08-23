---
description: Enthält die Antwort auf eine D3DAUTHENTICATEDQUERY \_ OUTPUTID-Abfrage.
ms.assetid: 4dfd1d65-b203-456a-bc9b-527906bcf87e
title: D3DAUTHENTICATEDCHANNEL_QUERYROUTPUTID_OUTPUT-Struktur (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 9861de1dc97a606821060fcb7665cac557a08c084271c319c3804740169af7d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600780"
---
# <a name="d3dauthenticatedchannel_queryroutputid_output-structure"></a>D3DAUTHENTICATEDCHANNEL \_ QUERYROUTPUTID \_ OUTPUT-Struktur

Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY \_ OUTPUTID-Abfrage.**](d3dauthenticatedquery-outputid.md)

Rufen Sie [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)auf, um diese Abfrage zu senden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT {
  Output D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
  HANDLE DeviceHandle;
  HANDLE CryptoSessionHandle;
  UINT   OutputIDIndex;
  UINT64 OutputID;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT;
```



## <a name="members"></a>Member

<dl> <dt>

**D3DAUTHENTICATEDCHANNEL-ABFRAGEAUSGABE \_ \_**
</dt> <dd>

Eine [**D3DAUTHENTICATEDCHANNEL \_ QUERY \_ OUTPUT-Struktur,**](d3dauthenticatedchannel-query-output.md) die eine Nachrichtenauthentifizierungscode (MAC) und andere Daten enthält.

</dd> <dt>

**DeviceHandle**
</dt> <dd>

Ein Handle für das Gerät.

</dd> <dt>

**CryptoSessionHandle**
</dt> <dd>

Ein Handle für die kryptografische Sitzung.

</dd> <dt>

**OutputIDIndex**
</dt> <dd>

Der Index der Ausgabe-ID, die im **OutputID-Member** angegeben ist.

</dd> <dt>

**OutputID**
</dt> <dd>

Eine Ausgabe-ID, die dem angegebenen Gerät und der kryptografischen Sitzung zugeordnet ist.

</dd> </dl>

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

 

 




