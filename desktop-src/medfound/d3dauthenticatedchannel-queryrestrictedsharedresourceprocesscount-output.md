---
description: Enthält die Antwort auf eine D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT-Abfrage.
ms.assetid: dd6286d8-dfb5-413a-ba38-8b99dc8fe305
title: D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT-Struktur (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 52381f200bc691f47f6a473bd76c5e1b81f345bf0ca955e2d2f9591e95dccd33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880139"
---
# <a name="d3dauthenticatedchannel_queryrestrictedsharedresourceprocesscount_output-structure"></a>D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT \_ OUTPUT-Struktur

Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT-Abfrage.**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md)

Rufen Sie [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)auf, um diese Abfrage zu senden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  UINT                                 NumRestrictedSharedResourceProcesses;
} D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT;
```



## <a name="members"></a>Member

<dl> <dt>

**Ausgabe**
</dt> <dd>

Eine [**D3DAUTHENTICATEDCHANNEL \_ QUERY \_ OUTPUT-Struktur,**](d3dauthenticatedchannel-query-output.md) die eine Nachrichtenauthentifizierungscode (MAC) und andere Daten enthält.

</dd> <dt>

**NumRestrictedSharedResourceProcesses**
</dt> <dd>

Die Anzahl der Prozesse, die zum Öffnen freigegebener Ressourcen mit eingeschränktem Zugriff zulässig sind. Ein Prozess kann eine solche Ressource nur öffnen, wenn dem Prozess Zugriff gewährt wurde.

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

 

 




