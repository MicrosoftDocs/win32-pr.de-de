---
description: Legt die Verschlüsselungsebene fest, die vor dem Zugriff auf geschützte Inhalte für die CPU oder den Bus ausgeführt wird.
ms.assetid: 6de6c4a3-705a-4420-b9f4-8d4d442b23bf
title: D3DAUTHENTICATEDCONFIGURE_ENCRYPTIONWHENACCESSIBLE (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_ENCRYPTIONWHENACCESSIBLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: f785931cf70ae48082cb45c436dd1c50b7c329fef61619738a3ef0a08240d7b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742647"
---
# <a name="d3dauthenticatedconfigure_encryptionwhenaccessible"></a>D3DAUTHENTICATEDCONFIGURE \_ ENCRYPTIONWHENACCESSIBLE

Legt die Verschlüsselungsebene fest, die vor dem Zugriff auf geschützte Inhalte für die CPU oder den Bus ausgeführt wird.



| Anforderung | Wert |
|--------------|-----------------------------------------------------------------------------------------------------------------------------|
| Befehls-GUID | **D3DAUTHENTICATEDCONFIGURE \_ ENCRYPTIONWHENACCESSIBLE**                                                                     |
| Eingabedaten   | [**D3DAUTHENTICATEDCHANNEL \_ CONFIGUREUNCOMGABEDENCRYPTION**](d3dauthenticatedchannel-configureuncompressedencryption.md) |



 

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Content Protection-Befehle](content-protection-commands.md)
</dt> <dt>

[GPU-basierte Content Protection](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




