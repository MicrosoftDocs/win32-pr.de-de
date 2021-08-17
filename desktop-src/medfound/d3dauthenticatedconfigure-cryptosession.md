---
description: Ordnet eine kryptografische Sitzung einem DirectX Video Acceleration 2-Decodergerät (DXVA-2) und einem Direct3D-Gerät zu.
ms.assetid: d40fead7-8a86-426e-933e-13df21cdf50b
title: D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION (D3d9types.h)
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
ms.openlocfilehash: 3e1df4b58750d5b2d82eb518d5dfc0ef24bdbe4e5569ebcaf708b8df60691d04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449440"
---
# <a name="d3dauthenticatedconfigure_cryptosession"></a>D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION

Ordnet eine kryptografische Sitzung einem DirectX Video Acceleration 2-Decodergerät (DXVA-2) und einem Direct3D-Gerät zu.



| Anforderung | Wert |
|--------------|-----------------------------------------------------------------------------------------------------------|
| Befehls-GUID | **D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION**                                                              |
| Eingabedaten   | [**D3DAUTHENTICATEDCHANNEL \_ CONFIGURECRYPTOSESSION**](d3dauthenticatedchannel-configurecryptosession.md) |



 

## <a name="remarks"></a>Hinweise

Nachdem dieser Befehl gesendet wurde, können Sie die [D3DAUTHENTICATEDQUERY \_ OUTPUTID-Abfrage](d3dauthenticatedquery-outputid.md) senden, um herauszufinden, welche Videoausgaben der kryptografischen Sitzung zugeordnet sind.

Die folgenden Kanaltypen unterstützen diesen Befehl:

-   **D3DAUTHENTICATEDCHANNEL \_ D3D9**
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

 

 




