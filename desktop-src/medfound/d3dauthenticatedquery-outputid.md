---
description: Gibt einen der Ausgabebezeichner zurück, der einer angegebenen kryptografischen Sitzung und einem Direct3D-Gerät zugeordnet ist.
ms.assetid: 7b56055a-fb36-4e54-9bee-ab9401b09267
title: D3DAUTHENTICATEDQUERY_OUTPUTID (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_OUTPUTID
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7e8d735cf23ed5bac26ca26b779ba440f7a48301bf33f7de34d1986e75241324
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942750"
---
# <a name="d3dauthenticatedquery_outputid"></a>D3DAUTHENTICATEDQUERY \_ OUTPUTID

Gibt einen der Ausgabebezeichner zurück, der einer angegebenen kryptografischen Sitzung und einem Direct3D-Gerät zugeordnet ist.



| Anforderung | Wert |
|-------------|--------------------------------------------------------------------------------------------------------|
| Abfrage-GUID  | **D3DAUTHENTICATEDQUERY \_ OUTPUTID**                                                                    |
| Eingabedaten  | [**D3DAUTHENTICATEDCHANNEL \_ \_ QUERYOUTPUTID-EINGABE**](d3dauthenticatedchannel-queryoutputid-input.md)   |
| Daten zurückgeben | [**D3DAUTHENTICATEDCHANNEL \_ \_ QUERYOUTPUTID-AUSGABE**](d3dauthenticatedchannel-queryoutputid-output.md) |



 

## <a name="remarks"></a>Hinweise

Die folgenden Kanaltypen unterstützen diese Abfrage:

-   **D3DAUTHENTICATEDCHANNEL-TREIBERHARDWARE \_ \_**
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

 

 




