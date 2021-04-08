---
description: Gibt einen der Ausgabe Bezeichner zurück, der einer angegebenen Kryptografiesitzung und einem Direct3D-Gerät zugeordnet ist.
ms.assetid: 7b56055a-fb36-4e54-9bee-ab9401b09267
title: D3DAUTHENTICATEDQUERY_OUTPUTID (D3d9types. h)
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
ms.openlocfilehash: fa970ae6e7b10f553679376d7a924d1c8b67c595
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749296"
---
# <a name="d3dauthenticatedquery_outputid"></a>D3DAUTHENTICATEDQUERY \_ OutputID

Gibt einen der Ausgabe Bezeichner zurück, der einer angegebenen Kryptografiesitzung und einem Direct3D-Gerät zugeordnet ist.



| Anforderung | Wert |
|-------------|--------------------------------------------------------------------------------------------------------|
| Abfrage-GUID  | **D3DAUTHENTICATEDQUERY \_ OutputID**                                                                    |
| Eingabedaten  | [**D3DAUTHENTICATEDCHANNEL \_ queryoutputid- \_ Eingabe**](d3dauthenticatedchannel-queryoutputid-input.md)   |
| Daten zurückgeben | [**D3DAUTHENTICATEDCHANNEL \_ queryoutputid- \_ Ausgabe**](d3dauthenticatedchannel-queryoutputid-output.md) |



 

## <a name="remarks"></a>Bemerkungen

Diese Abfrage wird von den folgenden Kanaltypen unterstützt:

-   **D3DAUTHENTICATEDCHANNEL- \_ Treiber \_ Hardware**
-   **D3DAUTHENTICATEDCHANNEL- \_ Treiber \_ Software**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Content Protection Abfragen](content-protection-queries.md)
</dt> <dt>

[GPU-basiertes Content Protection](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




