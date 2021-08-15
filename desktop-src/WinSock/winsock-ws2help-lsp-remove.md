---
description: Winsock-Katalogänderungsereignis für einen LSP-Entfernungsvorgang (Layered Service Provider).
ms.assetid: 86FF17F7-8CCF-4A03-899F-42BFACDF3F54
title: WINSOCK_WS2HELP_LSP_REMOVE-Ereignis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_REMOVE
api_type:
- NA
api_location: ''
ms.openlocfilehash: b0ac13a5404dcbbfe5fb5f5d8c2a5f17d43edeb72ba135abfc7e85ad9e5227a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118321592"
---
# <a name="winsock_ws2help_lsp_remove-event"></a>WINSOCK \_ WS2HELP \_ LSP \_ REMOVE-Ereignis

> [!Note]  
> Mehrschichtige Dienstanbieter sind veraltet. Verwenden Sie ab Windows 8 Windows Server 2012 Filterplattform [Windows Filterplattform](../fwp/windows-filtering-platform-start-page.md).

 

Das **WINSOCK \_ WS2HELP \_ LSP \_ REMOVE-Ereignis** ist ein Winsock-Katalogänderungsereignis für einen mehrschichtigen Dienstanbieter-Entfernungsvorgang (Layered Service Provider, LSP).


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_REMOVE = {0x2, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*LSP-Name* 
</dt> <dd>

Der Name des LSP, der vom **szProtocol-Member** der [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) für den zu entfernenden LSP erhalten wurde.

</dd> <dt>

*Katalog* 
</dt> <dd>

Der Winsock-Katalog (32-Bit oder 64-Bit), in dem der LSP entfernt wird. Dies ist ein ganzzahliger Wert, der entweder 32 oder 64 ist.

</dd> <dt>

*Installationsprogramm* 
</dt> <dd>

Der Moduldateiname der Anwendung, die den LSP-Entfernungsaufruf abhebt.

</dd> <dt>

*GUID* 
</dt> <dd>

Der GUID-Wert des Winsock-Transportanbieters, aus dem der LSP entfernt wird.

</dd> <dt>

*Kategorie* 
</dt> <dd>

Das **dwCatalogEntryId-Member** der [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) für den zu entfernenden LSP.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das **WINSOCK \_ WS2HELP \_ LSP \_ REMOVE-Ereignis** wird für einen LSP-Entfernungsvorgang nachverfolgt, wenn ein Protokolleintrag aus dem Winsock-Katalog entfernt wird.

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

 

 
