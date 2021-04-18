---
title: Windows-Ereignis Sammler Datentypen (evcoll. h)
description: Die Datentypen für die Windows-Ereignis Sammlung werden als Objektvariablen Typen für Ereignis Abonnements, Funktionsparameter Typen und Funktions Rückgabe Typen verwendet.
ms.assetid: b78bdaf8-e034-40fe-acf8-632313e4fd94
ms.tgt_platform: multiple
keywords:
- EC_HANDLE
- EC_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ccec141317644aa091eac44033b87b9e4495ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340556"
---
# <a name="windows-event-collector-data-types"></a>Windows-Ereignis Sammler Datentypen

Die Datentypen für die Windows-Ereignis Sammlung werden als Objektvariablen Typen für Ereignis Abonnements, Funktionsparameter Typen und Funktions Rückgabe Typen verwendet.


```C++
typedef HANDLE EC_HANDLE;
typedef HANDLE EC_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

**EC- \_ handle**
</dt> <dd>

Handle für ein Abonnement Objekt. Wird zur Darstellung eines Ereignis Sammler Abonnements verwendet.

</dd> <dt>

**Eigenschaften Handle für EC- \_ Objekt \_ array \_ \_**
</dt> <dd>

Handle für ein Array von Eigenschafts Werten für die Ereignis Quellen eines Abonnements. Das Array Handle wird von der [**ecgetabonneptionproperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) -Methode zurückgegeben, wenn der **ecabonptioneventsources** -Wert an den *PropertyId* -Parameter übergeben wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                      |
| Header<br/>                   | <dl> <dt>Evcoll. h</dt> </dl> |



 

 





