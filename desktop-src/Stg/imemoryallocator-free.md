---
title: Kostenlose Methode für imemoryzucator
description: Die Free-Methode gibt den von der Zuordnungs Methode belegten Arbeitsspeicher frei.
ms.assetid: 41f81cba-4431-4ff7-ac84-8ff5bea71b65
keywords:
- Strukturierter Speicher für die kostenlose Methode
- Kostenlose strukturierte Speichermethode, imemoryzuordnerschnittstelle
- Strukturierte Speicherung der imemoryzuordcator-Schnittstelle, kostenlose Methode
topic_type:
- apiref
api_name:
- IMemoryAllocator.Free
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c07731f60aba7d847c79467b2b2c166b363d807
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040206"
---
# <a name="imemoryallocatorfree-method"></a>Imemoryzuweisung:: Free-Methode

Die **Free** [**-Methode gibt**](imemoryallocator-allocate.md) den von der Zuordnungs Methode belegten Arbeitsspeicher frei.

## <a name="syntax"></a>Syntax


```C++
virtual void Free(
   void* pv
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*teuren* 
</dt> <dd>

Zeiger auf den frei zufügenden Arbeitsspeicher.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Bibliothek<br/>                  | <dl> <dt>Ole32. lib</dt> </dl> |



 

 





