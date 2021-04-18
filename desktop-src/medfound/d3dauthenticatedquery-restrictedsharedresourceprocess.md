---
description: Gibt Informationen zu einem Prozess zurück, der freigegebene Ressourcen mit eingeschränktem Zugriff öffnen darf.
ms.assetid: 669d9623-3a96-4661-9dae-3f283a990fe8
title: D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESS (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 74bb829510fee4425648412f58d4f7cea74b1f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338939"
---
# <a name="d3dauthenticatedquery_restrictedsharedresourceprocess"></a>D3DAUTHENTICATEDQUERY \_ restrictedsharedresourceprocess

Gibt Informationen zu einem Prozess zurück, der freigegebene Ressourcen mit eingeschränktem Zugriff öffnen darf.



| Anforderung | Wert |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Abfrage-GUID  | **D3DAUTHENTICATEDQUERY \_ restrictedsharedresourceprocess**                                                                                           |
| Eingabedaten  | [**D3DAUTHENTICATEDCHANNEL \_ queryrestrictedsharedresourceprocess- \_ Eingabe**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-input.md)   |
| Daten zurückgeben | [**D3DAUTHENTICATEDCHANNEL \_ queryrestrictedsharedresourceprocess- \_ Ausgabe**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md) |



 

## <a name="remarks"></a>Bemerkungen

Diese Abfrage wird von den folgenden Kanaltypen unterstützt:

-   **D3DAUTHENTICATEDCHANNEL \_ d3d9**
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

 

 




