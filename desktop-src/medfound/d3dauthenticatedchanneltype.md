---
description: Gibt den Typ des Direct3D-authentifizierten Kanals an.
ms.assetid: 99a7664e-b0c8-4e66-ad3b-c6ad039ef6eb
title: D3DAUTHENTICATEDCHANNELTYPE-Enumeration (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNELTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5c0cab8a0a208bfb1a005166740dcc64c319c6e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346662"
---
# <a name="d3dauthenticatedchanneltype-enumeration"></a>D3DAUTHENTICATEDCHANNELTYPE-Enumeration

Gibt den Typ des Direct3D-authentifizierten Kanals an.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  D3DAUTHENTICATEDCHANNEL_D3D9             = 1,
  D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE  = 2,
  D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE  = 3
} D3DAUTHENTICATEDCHANNELTYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DAUTHENTICATEDCHANNEL_D3D9"></span><span id="d3dauthenticatedchannel_d3d9"></span>**D3DAUTHENTICATEDCHANNEL \_ d3d9**
</dt> <dd>

Direct3D 9-Kanal. Dieser Kanal ermöglicht die Kommunikation mit der Direct3D-Laufzeit.

</dd> <dt>

<span id="D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE"></span><span id="d3dauthenticatedchannel_driver_software"></span>**D3DAUTHENTICATEDCHANNEL- \_ Treiber \_ Software**
</dt> <dd>

Software Treiber Kanal. Dieser Kanal ermöglicht die Kommunikation mit einem Treiber, der Inhalts Schutzmechanismen in Software implementiert.

</dd> <dt>

<span id="D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE"></span><span id="d3dauthenticatedchannel_driver_hardware"></span>**D3DAUTHENTICATEDCHANNEL- \_ Treiber \_ Hardware**
</dt> <dd>

Hardware Treiber Kanal. Dieser Kanal ermöglicht die Kommunikation mit einem Treiber, der Inhalts Schutzmechanismen in der GPU-Hardware implementiert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>D3d9types. h (Include d3d9. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-videoenumerationen](direct3d-video-enumerations.md)
</dt> <dt>

[**IDirect3DDevice9Video:: kreateauthentiinitiedchannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel)
</dt> </dl>

 

 




