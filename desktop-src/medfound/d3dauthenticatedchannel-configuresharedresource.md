---
description: Enthält Eingabedaten für einen D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE-Befehl.
ms.assetid: bdeb0cc4-90f0-4174-a859-4b3fecb17bab
title: D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE-Struktur (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 0dbff67921f2ec6ad634c20b11b86b0384923db5548bcef113128fe5ede6bdd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742906"
---
# <a name="d3dauthenticatedchannel_configuresharedresource-structure"></a>D3DAUTHENTICATEDCHANNEL \_ CONFIGURESHAREDRESOURCE-Struktur

Enthält Eingabedaten für einen [**D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE-Befehl.**](d3dauthenticatedconfigure-sharedresource.md)

Rufen Sie [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)auf, um diese Abfrage zu senden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT       Parameters;
  D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE ProcessIdentiferType;
  HANDLE                                        ProcessHandle;
  BOOL                                          AllowAccess;
} D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE;
```



## <a name="members"></a>Member

<dl> <dt>

**Parameter**
</dt> <dd>

Eine [**D3DAUTHENTICATEDCHANNEL \_ CONFIGURE \_ INPUT-Struktur,**](d3dauthenticatedchannel-configure-input.md) die die Befehls-GUID und andere Daten enthält.

</dd> <dt>

**ProcessIdentiferType**
</dt> <dd>

Ein [**D3DAUTHENTICATEDCHANNEL \_ PROCESSIDENTIFIERTYPE-Wert,**](d3dauthenticatedchannel-processidentifiertype.md) der den Prozesstyp angibt. Legen Sie diesen Member auf PROCESSIDTYPE DWM fest, um den prozess Desktopfenster-Manager **\_ (DWM)** anzugeben. Legen Sie andernfalls diesen Member auf **PROCESSIDTYPE \_ HANDLE** und den **ProcessHandle-Member** auf ein gültiges Handle fest.

</dd> <dt>

**ProcessHandle**
</dt> <dd>

Ein Prozesshandle. Wenn der **ProcessIdentifier-Member** **dem PROCESSTIDTYPE \_ HANDLE** entspricht, gibt der **ProcessHandle-Member** ein Handle für einen Prozess an. Andernfalls wird der Wert ignoriert.

</dd> <dt>

**AllowAccess**
</dt> <dd>

**True** gibt an, dass der angegebene Prozess Zugriff auf eingeschränkte freigegebene Ressourcen hat.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Videostrukturen](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




