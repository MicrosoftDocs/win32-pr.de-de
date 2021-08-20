---
description: Gibt die Anzahl der geschützten freigegebenen Ressourcen zurück, die von jedem Prozess ohne Einschränkungen geöffnet werden können.
ms.assetid: afbd7bb9-de71-4992-919e-e1517228dc69
title: D3DAUTHENTICATEDQUERY_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a227d8aa23e7f070cebb1c73092bd0af170927eda582e417839375512e891df7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117879744"
---
# <a name="d3dauthenticatedquery_unrestrictedprotectedsharedresourcecount"></a>D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT

Gibt die Anzahl der geschützten freigegebenen Ressourcen zurück, die von jedem Prozess ohne Einschränkungen geöffnet werden können.



| Anforderung | Wert |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Abfrage-GUID  | **D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**                                                                                                    |
| Eingabedaten  | [**D3DAUTHENTICATEDCHANNEL-ABFRAGEEINGABE \_ \_**](d3dauthenticatedchannel-query-input.md)                                                                                   |
| Daten zurückgeben | [**D3DAUTHENTICATEDCHANNEL \_ QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT-AUSGABE \_**](d3dauthenticatedchannel-queryunrestrictedprotectedsharedresourcecount-output.md) |



 

## <a name="remarks"></a>Hinweise

Der einzige Kanaltyp, der diese Abfrage unterstützt, ist **D3DAUTHENTICATEDCHANNEL \_ DRIVER \_ SOFTWARE**.

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

 

 




