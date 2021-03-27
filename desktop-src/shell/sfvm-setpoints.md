---
description: Legt die Punkte der aktuell ausgewählten Objekte auf das Datenobjekt in den Befehlen zum Kopieren und Ausschneiden fest. Wird von der shshellfolderview- \_ Nachricht verwendet.
title: SFVM_SETPOINTS Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d2c3e06a-19e4-4b78-9b7c-1a256582786e
api_name:
- SFVM_SETPOINTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1df501f162fb19335fcf1672299a74135672db22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218583"
---
# <a name="sfvm_setpoints-message"></a>Sfvm- \_ SetPoints-Meldung

Legt die Punkte der aktuell ausgewählten Objekte auf das Datenobjekt in den Befehlen zum **Kopieren** und **Ausschneiden** fest. Wird von der [**shshellfolderview- \_ Nachricht**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)verwendet.


```C++
SFVM_SETPOINTS 

    lParam = (LPARAM) pdtobj;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdtobj* \[ in\]
</dt> <dd>Ein Zeiger auf ein <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">**IDataObject**</a> der Befehle zum **Kopieren** und **Ausschneiden** .</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es wird immer NULL zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
