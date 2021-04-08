---
description: Enthält die Antwort auf eine D3DAUTHENTICATEDQUERY \_ restrictedsharedresourceprocesscount-Abfrage.
ms.assetid: dd6286d8-dfb5-413a-ba38-8b99dc8fe305
title: D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT-Struktur (D3d9types. h)
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
ms.openlocfilehash: 60568e7056ab9df7aafcec1cac7864685c7c6100
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749313"
---
# <a name="d3dauthenticatedchannel_queryrestrictedsharedresourceprocesscount_output-structure"></a>D3DAUTHENTICATEDCHANNEL \_ queryrestrictedsharedresourceprocesscount- \_ Ausgabestruktur

Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY \_ restrictedsharedresourceprocesscount**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md) -Abfrage.

Um diese Abfrage zu senden, nennen Sie [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

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

Eine [**D3DAUTHENTICATEDCHANNEL \_ Query- \_ Ausgabe**](d3dauthenticatedchannel-query-output.md) Struktur, die eine Nachrichtenauthentifizierungscode (Mac) und andere Daten enthält.

</dd> <dt>

**Numrestrictedsharedresourceprocesses**
</dt> <dd>

Die Anzahl der Prozesse, die zum Öffnen von freigegebenen Ressourcen mit eingeschränktem Zugriff zulässig sind. Ein Prozess kann eine solche Ressource nur dann öffnen, wenn dem Prozess der Zugriff gewährt wurde.

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

 

 




