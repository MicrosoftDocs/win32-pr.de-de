---
description: Gibt die Anzahl der Prozesse zurück, die freigegebene Ressourcen mit eingeschränktem Zugriff öffnen dürfen.
ms.assetid: e1b9ef18-fd08-4639-9ba9-4bccd33f5d16
title: D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 59ba86a372a7cb505b5b9b3b6a980abbb4de4143f699a44bca015879bea62af2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118064437"
---
# <a name="d3dauthenticatedquery_restrictedsharedresourceprocesscount"></a>D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT

Gibt die Anzahl der Prozesse zurück, die freigegebene Ressourcen mit eingeschränktem Zugriff öffnen dürfen.



| Anforderung | Wert |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Abfrage-GUID  | **D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**                                                                                                |
| Eingabedaten  | [**D3DAUTHENTICATEDCHANNEL-ABFRAGEEINGABE \_ \_**](d3dauthenticatedchannel-query-input.md)                                                                           |
| Daten zurückgeben | [**D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT-AUSGABE \_**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocesscount-output.md) |



 

## <a name="remarks"></a>Hinweise

Die folgenden Kanaltypen unterstützen diese Abfrage:

-   **D3DAUTHENTICATEDCHANNEL \_ D3D9**
-   **D3DAUTHENTICATEDCHANNEL-TREIBERSOFTWARE \_ \_**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Content Protection Abfragen](content-protection-queries.md)
</dt> <dt>

[GPU-basierte Content Protection](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




