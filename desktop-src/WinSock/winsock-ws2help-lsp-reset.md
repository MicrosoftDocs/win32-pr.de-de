---
description: Winsock-Katalogänderungsereignis für einen Winsock-Katalogzurücksetzungsvorgang.
ms.assetid: BE8DC0DB-0F96-4015-87F5-ECF25AE164AA
title: WINSOCK_WS2HELP_LSP_RESET-Ereignis
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
ms.openlocfilehash: 3c9a638d962db908b24387d7baeb2f34d4e09ece561fdd1796a8a44930a5dfb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051288"
---
# <a name="winsock_ws2help_lsp_reset-event"></a>WINSOCK \_ WS2HELP \_ LSP \_ RESET-Ereignis

> [!Note]  
> Mehrschichtige Dienstanbieter sind veraltet. Verwenden Sie ab Windows 8 Windows Server 2012 [Filterplattform Windows Filterplattform](../fwp/windows-filtering-platform-start-page.md).

 

Das **WINSOCK \_ WS2HELP \_ LSP \_ RESET-Ereignis** ist ein Winsock-Katalogänderungsereignis für einen Winsock-Katalogzurücksetzungsvorgang.


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_RESET = {0x4, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Katalog* 
</dt> <dd>

Der Winsock-Katalog (32-Bit oder 64-Bit), der zurückgesetzt wird. Dies ist ein ganzzahliger Wert, der entweder 32 oder 64 ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das **WINSOCK \_ WS2HELP \_ LSP \_ RESET-Ereignis** wird für einen Winsock Layered Service Provider-Vorgang (LSP) nachverfolgt, wenn der Winsock-Katalog zurückgesetzt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Steuerung der Winsock-Ablaufverfolgung](control-of-winsock-tracing.md)
</dt> <dt>

[Winsock-Ablaufverfolgung](winsock-tracing.md)
</dt> <dt>

[Winsock-Ablaufverfolgungsebenen](winsock-tracing-levels.md)
</dt> <dt>

[Details zur Ablaufverfolgung für Winsock-Katalogänderung](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
