---
description: Winsock-Katalogänderungsereignis für einen mehrschichtigen Dienstanbieter (Layered Service Provider, LSP) – Deaktivierungsvorgang.
ms.assetid: 6BCEECB1-92AD-47D8-952B-D0FD2A78EB45
title: WINSOCK_WS2HELP_LSP_DISABLE-Ereignis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_DISABLE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 578479710856e149760202699be13d4b30b50709f6ea9b389e055793a8b0ca94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733130"
---
# <a name="winsock_ws2help_lsp_disable-event"></a>WINSOCK \_ WS2HELP \_ LSP \_ DISABLE-Ereignis

> [!Note]  
> Mehrschichtige Dienstanbieter sind veraltet. Verwenden Sie ab Windows 8 Windows Server 2012 [Filterplattform Windows Filterplattform](../fwp/windows-filtering-platform-start-page.md).

 

Das **WINSOCK \_ WS2HELP \_ LSP \_ DISABLE-Ereignis** ist ein Winsock-Katalogänderungsereignis für einen mehrschichtigen Dienstanbieter-Deaktivierungsvorgang (Layered Service Provider, LSP).


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_DISABLE = {0x3, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*LSP-Name* 
</dt> <dd>

Der Name des LSP, der vom **szProtocol-Member** der [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) für den deaktivierten LSP erhalten wurde.

</dd> <dt>

*Katalog* 
</dt> <dd>

Der Winsock-Katalog (32-Bit oder 64-Bit), in dem der LSP deaktiviert wird. Dies ist ein ganzzahliger Wert, der entweder 32 oder 64 ist.

</dd> <dt>

*Installationsprogramm* 
</dt> <dd>

Der Moduldateiname der Anwendung, die den LSP-Deaktivierungsaufruf vor sich hat.

</dd> <dt>

*GUID* 
</dt> <dd>

Der GUID-Wert des Winsock-Transportanbieters, dass der LSP deaktiviert wird.

</dd> <dt>

*Kategorie* 
</dt> <dd>

Das **dwCatalogEntryId-Member** der [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) für den deaktivierten LSP.

</dd> </dl>

Dieses Ereignis verfügt über keine Parameter.

## <a name="remarks"></a>Hinweise

Das **WINSOCK \_ WS2HELP \_ LSP \_ DISABLE-Ereignis** wird für einen LSP-Deaktivierungsvorgang nachverfolgt, wenn ein Protokolleintrag im Winsock-Katalog deaktiviert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Steuerung der Winsock-Ablaufverfolgung](control-of-winsock-tracing.md)
</dt> <dt>

[Winsock-Ablaufverfolgung](winsock-tracing.md)
</dt> <dt>

[Winsock-Ablaufverfolgungsebenen](winsock-tracing-levels.md)
</dt> <dt>

[Details zur Ablaufverfolgung für Winsock-Katalogänderung](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
