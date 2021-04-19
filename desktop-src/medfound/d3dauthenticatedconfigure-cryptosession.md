---
description: Verknüpft eine Kryptografiesitzung mit einem DXVA-2-Decodergerät (DirectX Video Acceleration 2) und einem Direct3D-Gerät.
ms.assetid: d40fead7-8a86-426e-933e-13df21cdf50b
title: D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 4b6fda19aef9629214aaa410fd43c4d64f16dd29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346046"
---
# <a name="d3dauthenticatedconfigure_cryptosession"></a>D3DAUTHENTICATEDCONFIGURE \_ CryptoSession

Verknüpft eine Kryptografiesitzung mit einem DXVA-2-Decodergerät (DirectX Video Acceleration 2) und einem Direct3D-Gerät.



| Anforderung | Wert |
|--------------|-----------------------------------------------------------------------------------------------------------|
| Befehls-GUID | **D3DAUTHENTICATEDCONFIGURE \_ CryptoSession**                                                              |
| Eingabedaten   | [**D3DAUTHENTICATEDCHANNEL \_ Konfigurations Sitzung**](d3dauthenticatedchannel-configurecryptosession.md) |



 

## <a name="remarks"></a>Bemerkungen

Nachdem dieser Befehl gesendet wurde, können Sie die [D3DAUTHENTICATEDQUERY \_ OutputID](d3dauthenticatedquery-outputid.md) -Abfrage senden, um herauszufinden, welche Video Ausgaben der Kryptografiesitzung zugeordnet sind.

Der folgende Kanaltyp unterstützt diesen Befehl:

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

[Content Protection-Befehle](content-protection-commands.md)
</dt> <dt>

[GPU-basiertes Content Protection](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




