---
description: Gibt die Anzahl der Ausgabebezeichner zurück, die einer angegebenen kryptografischen Sitzung und einem Direct3D-Gerät zugeordnet sind.
ms.assetid: a5b17250-6a40-40a9-93b6-3b98b56b09d6
title: D3DAUTHENTICATEDQUERY_OUTPUTIDCOUNT (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_OUTPUTIDCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: c6a3da90d467701decfe5f96383e06026325e86c2622ec0f05f4703b06e2cbe8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828510"
---
# <a name="d3dauthenticatedquery_outputidcount"></a>D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT

Gibt die Anzahl der Ausgabebezeichner zurück, die einer angegebenen kryptografischen Sitzung und einem Direct3D-Gerät zugeordnet sind.



| Anforderung | Wert |
|-------------|------------------------------------------------------------------------------------------------------------------|
| Abfrage-GUID  | **D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**                                                                         |
| Eingabedaten  | [**D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTIDCOUNT \_ INPUT**](d3dauthenticatedchannel-queryoutputidcount-input.md)   |
| Daten zurückgeben | [**D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTIDCOUNT-AUSGABE \_**](d3dauthenticatedchannel-queryoutputidcount-output.md) |



 

## <a name="remarks"></a>Hinweise

Diese Abfrage wird von den folgenden Kanaltypen unterstützt:

-   **D3DAUTHENTICATEDCHANNEL-TREIBERHARDWARE \_ \_**
-   **D3DAUTHENTICATEDCHANNEL-TREIBERSOFTWARE \_ \_**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Content Protection Abfragen](content-protection-queries.md)
</dt> <dt>

[GPU-basierte Content Protection](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




