---
title: Imemoryallocator-Zuordnungs Methode
description: Die Zuordnungs Methode belegt Arbeitsspeicher für die stgconvertpropertytovariant-Funktion, wenn die Funktion einen serializedpropertyvalue-Datentyp in einen PROPVARIANT-Datentyp konvertiert.
ms.assetid: aa9c9308-fb55-405c-901a-9d5abfac5395
keywords:
- Zuordnen von strukturiertem Speicher
- Zuordnen von strukturiertem Speicher, imemoryallocator-Schnittstelle
- Strukturierter Speicher der imemoryallocator-Schnittstelle, Methode zuordnen
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
ms.openlocfilehash: d7ee4b220e1c1e14ceed685e9b2adc694a44d2e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339929"
---
# <a name="imemoryallocatorallocate-method"></a>Imemoryallocator:: Zuordnungs Methode

Die **Zuordnungs Methode belegt** Arbeitsspeicher für die [**stgconvertpropertytovariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) -Funktion, wenn die Funktion einen **serializedpropertyvalue** -Datentyp in einen **PROPVARIANT** -Datentyp konvertiert.

## <a name="syntax"></a>Syntax


```C++
virtual void* Allocate(
  [in] ULONG cbSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*CBSIZE* \[ in\]
</dt> <dd>

Gibt die Größe des zugeordneten Arbeitsspeichers an.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Bibliothek<br/>                  | <dl> <dt>Ole32. lib</dt> </dl> |



 

