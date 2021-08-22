---
description: Initialisiert den authentifizierten Kanal.
ms.assetid: a74edbaa-af57-4f8e-9974-f6053f59377f
title: D3DAUTHENTICATEDCONFIGURE_INITIALIZE (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_INITIALIZE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5685bb995f23fc85ed52bc5d03e269669e6e5b7bb4221f8880c97d6c7ce517e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974679"
---
# <a name="d3dauthenticatedconfigure_initialize"></a>D3DAUTHENTICATEDCONFIGURE \_ INITIALIZE

Initialisiert den authentifizierten Kanal.



| Anforderung | Wert |
|--------------|-----------------------------------------------------------------------------------------------------|
| Befehls-GUID | **D3DAUTHENTICATEDCONFIGURE \_ INITIALIZE**                                                           |
| Eingabedaten   | [**D3DAUTHENTICATEDCHANNEL \_ CONFIGUREINITIALIZE**](d3dauthenticatedchannel-configureinitialize.md) |



 

## <a name="remarks"></a>Hinweise

Senden Sie diesen Befehl einmal am Anfang der Sitzung. Dieser Befehl kann nur einmal für jeden authentifizierten Kanal gesendet werden. Die Eingabesequenznummer wird für diesen Befehl ignoriert.

Die folgenden Kanaltypen unterstützen diesen Befehl:

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

 

 




