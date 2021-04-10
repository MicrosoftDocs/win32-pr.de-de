---
description: Änderungs Ereignis für den Winsock-Katalog für einen mehrstufigen Dienstanbieter (LSP).
ms.assetid: 76A3D175-8CDC-486C-8341-D6314BCEC113
title: WINSOCK_WS2HELP_LSP_INSTALL Ereignis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_INSTALL
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2d95a77f68bafd29fde3bbf34336d9b31d2a412e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960304"
---
# <a name="winsock_ws2help_lsp_install-event"></a>Winsock \_ WS2HELP \_ LSP- \_ Installations Ereignis

> [!Note]  
> Mehrstufige Dienstanbieter sind veraltet. Ab Windows 8 und Windows Server 2012 verwenden Sie die [Windows-Filter Plattform](../fwp/windows-filtering-platform-start-page.md).

 

Das **Winsock \_ WS2HELP \_ LSP \_** -Installations Ereignis ist ein Winsock-Katalog Änderungs Ereignis für einen mehrstufigen Dienstanbieter (LSP).


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_INSTALL = {0x1, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*LSP-Name* 
</dt> <dd>

Der Name des LSP, der vom **szprotocol** -Member der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur für den installierten LSP abgerufen wird.

</dd> <dt>

*Katalog* 
</dt> <dd>

Der Winsock-Katalog (32-Bit oder 64-Bit), in dem der LSP installiert wird. Dies ist ein ganzzahliger Wert, der entweder 32 oder 64 ist.

</dd> <dt>

*Installationsprogramm* 
</dt> <dd>

Der Modul Dateiname der Anwendung, die die LSP-Installation aufruft.

</dd> <dt>

*GUID* 
</dt> <dd>

Der GUID-Wert des Winsock-Transport Anbieters, unter dem der LSP installiert wird.

</dd> <dt>

*Kategorie* 
</dt> <dd>

Der **dwcatalogentryid** -Member der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur für das zu installierende LSP.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das **Winsock \_ WS2HELP \_ LSP- \_ Installations** Ereignis wird für einen LSP-Installationsvorgang nachverfolgt, wenn ein Protokolleintrag im Winsock-Katalog installiert wird.

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

 

 
