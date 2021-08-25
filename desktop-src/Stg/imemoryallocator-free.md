---
title: IMemoryAllocator Free-Methode
description: Die Free-Methode gibt den von der Allocate-Methode belegten Arbeitsspeicher frei.
ms.assetid: 41f81cba-4431-4ff7-ac84-8ff5bea71b65
keywords:
- Kostenlose strukturierte Storage
- Free-Methode Structured Storage , IMemoryAllocator-Schnittstelle
- IMemoryAllocator-Schnittstelle Structured Storage , Free-Methode
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
ms.openlocfilehash: f78690a37b5500f5e540cf4c2ef516b7c3ea89c219ba475dc5e5ac030f775d81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906170"
---
# <a name="imemoryallocatorfree-method"></a>IMemoryAllocator::Free-Methode

Die **Free-Methode** gibt den von der [**Allocate-Methode**](imemoryallocator-allocate.md) belegten Arbeitsspeicher frei.

## <a name="syntax"></a>Syntax


```C++
virtual void Free(
   void* pv
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pv* 
</dt> <dd>

Zeiger auf den freizugebenden Arbeitsspeicher.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Bibliothek<br/>                  | <dl> <dt>Ole32.lib</dt> </dl> |



 

 





