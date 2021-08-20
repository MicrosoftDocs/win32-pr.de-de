---
title: IMemoryAllocator Allocate-Methode
description: Die Allocate-Methode weist Arbeitsspeicher für die StgConvertPropertyToVariant-Funktion zu, wenn die Funktion einen SERIALIZEDPROPERTYVALUE-Datentyp in einen PROPVARIANT-Datentyp konvertiert.
ms.assetid: aa9c9308-fb55-405c-901a-9d5abfac5395
keywords:
- Zuordnen der Methode structured Storage
- Zuordnen der Methode Structured Storage , IMemoryAllocator-Schnittstelle
- IMemoryAllocator-Schnittstelle Structured Storage , Allocate-Methode
topic_type:
- apiref
api_name:
- IMemoryAllocator.Allocate
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b10a924604b0ee299eb1ac5c29a29bba9700f0523be820ffa0cc5bc4a14fd4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961765"
---
# <a name="imemoryallocatorallocate-method"></a>IMemoryAllocator::Allocate-Methode

Die **Allocate-Methode** weist Arbeitsspeicher für die [**StgConvertPropertyToVariant-Funktion**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) zu, wenn die Funktion einen **SERIALIZEDPROPERTYVALUE-Datentyp** in einen **PROPVARIANT-Datentyp** konvertiert.

## <a name="syntax"></a>Syntax


```C++
virtual void* Allocate(
  [in] ULONG cbSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cbSize* \[ In\]
</dt> <dd>

Gibt die Größe des zu reservierten Arbeitsspeichers an.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Bibliothek<br/>                  | <dl> <dt>Ole32.lib</dt> </dl> |



 

