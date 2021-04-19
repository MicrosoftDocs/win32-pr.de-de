---
description: Änderungs Ereignis für den Winsock-Katalog für einen mehrstufigen Dienstanbieter (LSP).
ms.assetid: 6BCEECB1-92AD-47D8-952B-D0FD2A78EB45
title: WINSOCK_WS2HELP_LSP_DISABLE Ereignis
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
ms.openlocfilehash: 6d785bfbd96d35717be7bbf76dab8f28f41c9fc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350006"
---
# <a name="winsock_ws2help_lsp_disable-event"></a>Winsock \_ WS2HELP \_ LSP-Deaktivierungs \_ Ereignis

> [!Note]  
> Mehrstufige Dienstanbieter sind veraltet. Ab Windows 8 und Windows Server 2012 verwenden Sie die [Windows-Filter Plattform](../fwp/windows-filtering-platform-start-page.md).

 

Das **Winsock \_ WS2HELP \_ LSP \_** -Deaktivierungs Ereignis ist ein Winsock-Katalog Änderungs Ereignis für einen aktivierten Dienstanbieter (LSP).


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_DISABLE = {0x3, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*LSP-Name* 
</dt> <dd>

Der Name des LSP, der vom **szprotocol** -Member der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur für das deaktivierte LSP abgerufen wird.

</dd> <dt>

*Katalog* 
</dt> <dd>

Der Winsock-Katalog (32 Bit oder 64 Bit), in dem der LSP deaktiviert wird. Dies ist ein ganzzahliger Wert, der entweder 32 oder 64 ist.

</dd> <dt>

*Installationsprogramm* 
</dt> <dd>

Der Modul Dateiname der Anwendung, die die LSP-Deaktivierung aufruft.

</dd> <dt>

*GUID* 
</dt> <dd>

Der GUID-Wert des Winsock-Transport Anbieters, für den der LSP deaktiviert wird.

</dd> <dt>

*Kategorie* 
</dt> <dd>

Der **dwcatalogentryid** -Member der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur für das deaktivierte LSP.

</dd> </dl>

Dieses Ereignis weist keine Parameter auf.

## <a name="remarks"></a>Bemerkungen

Das **Winsock \_ WS2HELP \_ LSP \_** -Deaktivierungs Ereignis wird für einen LSP-Deaktivierungs Vorgang nachverfolgt, wenn ein Protokolleintrag im Winsock-Katalog deaktiviert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kontrolle über die Winsock-Ablauf Verfolgung](control-of-winsock-tracing.md)
</dt> <dt>

[Winsock-Ablauf Verfolgung](winsock-tracing.md)
</dt> <dt>

[Winsock-Ablauf Verfolgungs Ebenen](winsock-tracing-levels.md)
</dt> <dt>

[Details zur Änderung der Winsock-Katalog Änderung](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
