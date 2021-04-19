---
description: Das Änderungs Ereignis für den Winsock-Katalog für einen Winsock-Katalog Zurücksetzungs Vorgang.
ms.assetid: BE8DC0DB-0F96-4015-87F5-ECF25AE164AA
title: WINSOCK_WS2HELP_LSP_RESET Ereignis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_RESET
api_type:
- NA
api_location: ''
ms.openlocfilehash: 219eb85dec0cdda77ca8741ae42df1f63d1a7dbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364106"
---
# <a name="winsock_ws2help_lsp_reset-event"></a>Winsock \_ WS2HELP \_ LSP \_ Reset-Ereignis

> [!Note]  
> Mehrstufige Dienstanbieter sind veraltet. Ab Windows 8 und Windows Server 2012 verwenden Sie die [Windows-Filter Plattform](../fwp/windows-filtering-platform-start-page.md).

 

Das **Winsock \_ WS2HELP \_ LSP \_ Reset** -Ereignis ist ein Winsock-Katalog Änderungs Ereignis für einen Winsock-Katalog Zurücksetzungs Vorgang.


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_RESET = {0x4, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Katalog* 
</dt> <dd>

Der Winsock-Katalog (32-Bit oder 64-Bit), der zurückgesetzt wird. Dies ist ein ganzzahliger Wert, der entweder 32 oder 64 ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das **Winsock \_ WS2HELP \_ LSP \_ Reset** -Ereignis wird für einen LSP-Vorgang (Winsock-Schicht-Dienstanbieter) nachverfolgt, wenn der Winsock-Katalog zurückgesetzt wird.

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

 

 
