---
description: Gibt einen der Verschlüsselungstypen zurück, die zum Verschlüsseln von Inhalten verwendet werden können, bevor die CPU oder der Bus darauf zugreifen können.
ms.assetid: 263c6f00-8bc9-4e9c-8b98-fb8f87c6c008
title: D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUID (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUID
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b5755a2707ec9d7440cda9b4692eed36ac6deff1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344014"
---
# <a name="d3dauthenticatedquery_encryptionwhenaccessibleguid"></a>D3DAUTHENTICATEDQUERY \_ Verschlüsselung-accessibleguid

Gibt einen der Verschlüsselungstypen zurück, die zum Verschlüsseln von Inhalten verwendet werden können, bevor die CPU oder der Bus darauf zugreifen können.



| Anforderung | Wert |
|-------------|------------------------------------------------------------------------------------------------------------------------------------|
| Abfrage-GUID  | **D3DAUTHENTICATEDQUERY \_ Verschlüsselung-accessibleguid**                                                                            |
| Eingabedaten  | [**D3DAUTHENTICATEDCHANNEL \_ queryevictionverschlüsseltionguid- \_ Eingabe**](d3dauthenticatedchannel-queryevictionencryptionguid-input.md)   |
| Daten zurückgeben | [**D3DAUTHENTICATEDCHANNEL \_ queryevictionverschlüsseltionguid- \_ Ausgabe**](d3dauthenticatedchannel-queryevictionencryptionguid-output.md) |



 

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

 

 




