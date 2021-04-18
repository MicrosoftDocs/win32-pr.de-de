---
description: Stellt einen Hardwarebeschleuniger für die DirectX-Video Beschleunigung (DXVA) 1,0 dar.
ms.assetid: 63f77cf9-4c04-4ddb-9582-cfcf86f66a2a
title: IDirect3DDXVADevice9-Schnittstelle (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 192f47b8161893f9517bc976452eb8836da4bb53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347114"
---
# <a name="idirect3ddxvadevice9-interface"></a>IDirect3DDXVADevice9-Schnittstelle

Stellt einen Hardwarebeschleuniger für die DirectX-Video Beschleunigung (DXVA) 1,0 dar.

## <a name="members"></a>Member

Die **IDirect3DDXVADevice9** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **IDirect3DDXVADevice9** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IDirect3DDXVADevice9** -Schnittstelle verfügt über diese Methoden.



| Methode                                                  | BESCHREIBUNG                                                           |
|:--------------------------------------------------------|:----------------------------------------------------------------------|
| [**BeginFrame**](idirect3ddxvadevice9-beginframe.md)   | Startet die Verarbeitung zum Erstellen eines decodierten Bilds.<br/>         |
| [**Endframe**](idirect3ddxvadevice9-endframe.md)       | Beendet die Verarbeitung zum Erstellen eines decodierten Bilds.<br/>           |
| [**Auszuführen**](idirect3ddxvadevice9-execute.md)         | Führt einen DXVA-Decodierungs Vorgang aus. <br/>                       |
| [**QueryStatus**](idirect3ddxvadevice9-querystatus.md) | Fragt den Lese-/Schreibstatus einer DXVA-Decodierungs Oberfläche ab. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Um einen Zeiger auf diese Schnittstelle abzurufen, nennen Sie [**IDirect3DVideoDevice9:: kreatedxvadevice**](idirect3dvideodevice9-createdxvadevice.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Video Schnittstellen](direct3d-video-interfaces.md)
</dt> </dl>

 

 
