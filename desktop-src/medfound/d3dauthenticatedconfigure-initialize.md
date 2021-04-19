---
description: Initialisiert den authentifizierten Kanal.
ms.assetid: a74edbaa-af57-4f8e-9974-f6053f59377f
title: D3DAUTHENTICATEDCONFIGURE_INITIALIZE (D3d9types. h)
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
ms.openlocfilehash: 2cd3238b7a7eea27356ce76ec9c83bf8aea4d7f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343208"
---
# <a name="d3dauthenticatedconfigure_initialize"></a>D3DAUTHENTICATEDCONFIGURE \_ initialisieren

Initialisiert den authentifizierten Kanal.



| Anforderung | Wert |
|--------------|-----------------------------------------------------------------------------------------------------|
| Befehls-GUID | **D3DAUTHENTICATEDCONFIGURE \_ initialisieren**                                                           |
| Eingabedaten   | [**D3DAUTHENTICATEDCHANNEL- \_ Konfiguration erneut initialisieren**](d3dauthenticatedchannel-configureinitialize.md) |



 

## <a name="remarks"></a>Bemerkungen

Senden Sie diesen Befehl einmal am Anfang der Sitzung. Dieser Befehl kann nur ein Mal für jeden authentifizierten Kanal gesendet werden. Die Eingabe Sequenznummer wird für diesen Befehl ignoriert.

Der folgende Kanaltyp unterstützt diesen Befehl:

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

[Content Protection-Befehle](content-protection-commands.md)
</dt> <dt>

[GPU-basiertes Content Protection](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




