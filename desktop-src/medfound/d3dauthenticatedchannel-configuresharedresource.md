---
description: Enthält Eingabedaten für einen D3DAUTHENTICATEDCONFIGURE \_ SharedResource-Befehl.
ms.assetid: bdeb0cc4-90f0-4174-a859-4b3fecb17bab
title: D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE-Struktur (D3d9types. h)
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
ms.openlocfilehash: 7cbbb1645b232195e1cdb12e859234339ddda287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344017"
---
# <a name="d3dauthenticatedchannel_configuresharedresource-structure"></a>D3DAUTHENTICATEDCHANNEL- \_ Struktur konfigurieren

Enthält Eingabedaten für einen [**D3DAUTHENTICATEDCONFIGURE \_ SharedResource**](d3dauthenticatedconfigure-sharedresource.md) -Befehl.

Um diese Abfrage zu senden, nennen Sie [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).

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

Eine [**D3DAUTHENTICATEDCHANNEL \_ - \_ Eingabe**](d3dauthenticatedchannel-configure-input.md) Struktur, die die Befehls-GUID und andere Daten enthält.

</dd> <dt>

**Processidentifertype**
</dt> <dd>

Ein [**D3DAUTHENTICATEDCHANNEL \_ processidentifiertype**](d3dauthenticatedchannel-processidentifiertype.md) -Wert, der den Typ des Prozesses angibt. Legen Sie diesen Member auf **processidtype \_ DWM** fest, um den Desktopfenster-Manager-Prozess (DWM) anzugeben. Legen Sie diesen Member andernfalls auf **processidtype \_ handle** fest, und legen Sie den **ProcessHandle** -Member auf ein gültiges Handle fest.

</dd> <dt>

**ProcessHandle**
</dt> <dd>

Ein Prozess handle. Wenn das **processidentifier** -Element **\_ mit dem processtidtype-handle** gleich ist, gibt das **ProcessHandle** -Member ein Handle für einen Prozess an. Andernfalls wird der Wert ignoriert.

</dd> <dt>

**Allowaccess**
</dt> <dd>

**True** gibt an, dass der angegebene Prozess Zugriff auf eingeschränkte freigegebene Ressourcen hat.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Video Strukturen](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




