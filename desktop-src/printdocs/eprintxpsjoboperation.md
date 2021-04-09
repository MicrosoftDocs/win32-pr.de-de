---
description: Gibt an, ob sich ein XPS-Druckauftrag in der spoolingphase oder der Renderingphase befindet.
ms.assetid: 14871d29-59e4-45a2-9697-12550c58396c
title: Eprintxpsjoboperation-Enumeration (winspool. h)
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
ms.openlocfilehash: 917993be2af6e7a78afaec1ad4749dadcaebecba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756391"
---
# <a name="eprintxpsjoboperation-enumeration"></a>Eprintxpsjoboperation-Enumeration

Gibt an, ob sich ein XPS-Druckauftrag in der spoolingphase oder der Renderingphase befindet.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagEPrintXPSJobOperation { 
  kJobProduction,
  kJobConsumption
} EPrintXPSJobOperation;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="kJobProduction"></span><span id="kjobproduction"></span><span id="KJOBPRODUCTION"></span>**kjobproduction**
</dt> <dd>

Der XPS-Auftrag ist Spoolvorgang.

</dd> <dt>

<span id="kJobConsumption"></span><span id="kjobconsumption"></span><span id="KJOBCONSUMPTION"></span>**kjobverbrauch**
</dt> <dd>

Der XPS-Auftrag ist Rendering.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Enumeration wird primär als Parameter für die [**reportjobprocessingprogress**](reportjobprocessingprogress.md) -Funktion verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |



 

 




