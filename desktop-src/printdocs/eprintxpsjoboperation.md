---
description: Gibt an, ob sich ein XPS-Druckauftrag in der Spooling- oder Renderingphase befindet.
ms.assetid: 14871d29-59e4-45a2-9697-12550c58396c
title: EPrintXPSJobOperation-Enumeration (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EPrintXPSJobOperation
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 44f1f7ed80cd1de071633de37c5f0e91e913841388754a65c0194665bd3084de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971539"
---
# <a name="eprintxpsjoboperation-enumeration"></a>EPrintXPSJobOperation-Enumeration

Gibt an, ob sich ein XPS-Druckauftrag in der Spooling- oder Renderingphase befindet.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagEPrintXPSJobOperation { 
  kJobProduction,
  kJobConsumption
} EPrintXPSJobOperation;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="kJobProduction"></span><span id="kjobproduction"></span><span id="KJOBPRODUCTION"></span>**kJobProduction**
</dt> <dd>

Der XPS-Auftrag wird gepoolt.

</dd> <dt>

<span id="kJobConsumption"></span><span id="kjobconsumption"></span><span id="KJOBCONSUMPTION"></span>**kJobConsumption**
</dt> <dd>

Der XPS-Auftrag wird gerendert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Enumeration wird hauptsächlich als Parameter für die [**ReportJobProcessingProgress-Funktion**](reportjobprocessingprogress.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |



 

 




