---
description: Gibt die Anzahl von Ausgabe Bezeichner zurück, die einer angegebenen Kryptografiesitzung und einem Direct3D-Gerät zugeordnet sind.
ms.assetid: a5b17250-6a40-40a9-93b6-3b98b56b09d6
title: D3DAUTHENTICATEDQUERY_OUTPUTIDCOUNT (D3d9types. h)
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
ms.openlocfilehash: 624b9ca0ee96f71fb9d3cb655aa9c10030a40efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749289"
---
# <a name="d3dauthenticatedquery_outputidcount"></a>D3DAUTHENTICATEDQUERY \_ outputidcount

Gibt die Anzahl von Ausgabe Bezeichner zurück, die einer angegebenen Kryptografiesitzung und einem Direct3D-Gerät zugeordnet sind.



| Anforderung | Wert |
|-------------|------------------------------------------------------------------------------------------------------------------|
| Abfrage-GUID  | **D3DAUTHENTICATEDQUERY \_ outputidcount**                                                                         |
| Eingabedaten  | [**D3DAUTHENTICATEDCHANNEL \_ queryoutputidcount- \_ Eingabe**](d3dauthenticatedchannel-queryoutputidcount-input.md)   |
| Daten zurückgeben | [**D3DAUTHENTICATEDCHANNEL \_ queryoutputidcount- \_ Ausgabe**](d3dauthenticatedchannel-queryoutputidcount-output.md) |



 

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

 

 




