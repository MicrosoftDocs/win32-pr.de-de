---
description: Gibt Handles an die kryptografische Sitzung und das Direct3D-Gerät zurück, die einem angegebenen DXVA-2-Decodergerät (DirectX Video Acceleration 2) zugeordnet sind.
ms.assetid: 90b3bcf3-2988-48de-8acd-62e385d4fdf0
title: D3DAUTHENTICATEDQUERY_CRYPTOSESSION (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_CRYPTOSESSION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 3ee1cabc69122ebd7eb7d81c64eb761439e6a3c0cde20dd376c3581b9aed0738
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974669"
---
# <a name="d3dauthenticatedquery_cryptosession"></a>D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION

Gibt Handles an die kryptografische Sitzung und das Direct3D-Gerät zurück, die einem angegebenen DXVA-2-Decodergerät (DirectX Video Acceleration 2) zugeordnet sind.



| Anforderung | Wert |
|-------------|------------------------------------------------------------------------------------------------------------------|
| Abfrage-GUID  | **D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**                                                                         |
| Eingabedaten  | [**D3DAUTHENTICATEDCHANNEL-ABFRAGEEINGABE \_ \_**](d3dauthenticatedchannel-query-input.md)                             |
| Daten zurückgeben | [**D3DAUTHENTICATEDCHANNEL \_ \_ QUERYCRYPTOSESSION-AUSGABE**](d3dauthenticatedchannel-querycryptosession-output.md) |



 

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

 

 




