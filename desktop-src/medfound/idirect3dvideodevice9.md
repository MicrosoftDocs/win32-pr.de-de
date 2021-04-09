---
description: Ermöglicht die hardwarebeschleunigte Decodierung von einem Direct3D 9-Gerät mithilfe von DirectX Video Acceleration (DXVA) Version 1,0.
ms.assetid: abe3beac-f3f8-413d-8b83-9da3340b19ac
title: IDirect3DVideoDevice9-Schnittstelle (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 89afef6f39b3aa196d8b1013e3d8873e329ce6ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130340"
---
# <a name="idirect3dvideodevice9-interface"></a>IDirect3DVideoDevice9-Schnittstelle

Ermöglicht die hardwarebeschleunigte Decodierung von einem Direct3D 9-Gerät mithilfe von DirectX Video Acceleration (DXVA) Version 1,0.

## <a name="when-to-use"></a>Verwendung

Diese Schnittstelle ist nicht für die allgemeine Anwendungs Verwendung vorgesehen. DirectShow-Decoderfilter sollten die [**iamvideoaccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) -Schnittstelle verwenden, nicht **IDirect3DVideoDevice9**. Die Eingabe Pins des Filters für den Video Mischungs-Renderer (VMR) und der Überlagerungs-Mixer-Filter machen **iamvideoaccelerator** verfügbar.

## <a name="members"></a>Member

Die **IDirect3DVideoDevice9** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **IDirect3DVideoDevice9** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IDirect3DVideoDevice9** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                   | BESCHREIBUNG                                                                                                                       |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**"Kreatedxvadevice"**](idirect3dvideodevice9-createdxvadevice.md)                       | Erstellt ein DXVA-Decodergerät.<br/>                                                                                         |
| [**"Kreatesurface"**](idirect3dvideodevice9-createsurface.md)                             | Erstellt eine komprimierte Oberfläche für die DXVA-Decodierung.<br/>                                                                        |
| [**Getdxvacompressedbufferinfo**](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) | Ruft Informationen zu den für die Hardware beschleunigten Decodierung benötigten komprimierten Puffern ab.<br/>                                |
| [**Getdxvage IDs**](idirect3dvideodevice9-getdxvaguids.md)                               | Ruft eine Liste der DXVA-Profile ab, die vom Anzeigetreiber unterstützt werden.<br/>                                             |
| [**Getdxvainternalinfo**](idirect3dvideodevice9-getdxvainternalinfo.md)                 | Fragt den von der Hardware Abstraktionsschicht (HAL) für die private Verwendung zugewiesenen Speicherplatz ab. <br/> |
| [**Getuncompresseddxvaformats**](idirect3dvideodevice9-getuncompresseddxvaformats.md)   | Ruft eine Liste nicht komprimierter Pixel Formate ab, die mithilfe eines angegebenen DXVA-Profils gerendert werden können.<br/>                         |



 

## <a name="remarks"></a>Bemerkungen

Um einen Zeiger auf diese Schnittstelle abzurufen, nennen Sie **QueryInterface** für einen [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -oder [**IDirect3DDevice9Ex**](/windows/win32/api/d3d9/nn-d3d9-idirect3ddevice9ex) -Zeiger.

Diese Schnittstelle unterstützt nur DXVA 1,0. DXVA 2,0 wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Video Schnittstellen](direct3d-video-interfaces.md)
</dt> <dt>

[DirectX-Video Beschleunigung 2,0](directx-video-acceleration-2-0.md)
</dt> <dt>

[DXVA 1,0-Spezifikation](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
