---
description: Wird von der Standard Implementierung des Kontextmenüs gesendet, um einem Menübefehl einen Namen zuzuweisen.
title: DFM_MAPCOMMANDNAME Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8aa764f7-d5d4-4a84-94d2-993265e1eb5a
api_name:
- DFM_MAPCOMMANDNAME
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 312817e5c530078b906af63e4e8c3d00595d3a04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525358"
---
# <a name="dfm_mapcommandname-message"></a>DFM- \_ mapcommandname-Meldung

Wird von der Standard Implementierung des Kontextmenüs gesendet, um einem Menübefehl einen Namen zuzuweisen.


```C++
DFM_MAPCOMMANDNAME

    lParam = (LPARAM)(int*) defaultID;

    wparam = (WPARAM)(LPTSTR) pszCommandName;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DefaultID* \[ in, out\]
</dt> <dd>

Ein Zeiger auf die ID des ausgewählten Menübefehls.

</dd> <dt>

*pszcommandname* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Unicode-Zeichenfolge, die den Namen des Befehls enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Nachricht wird entweder an die Rückruffunktion oder an das Rückruf Objekt gesendet, je nachdem, wie das Standardkontext Menü-Objekt implementiert wird. Es gibt zwei APIs für die Implementierung, [**cdeffoldermenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**shkreatedefaultcontextmenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ Invokecommandex**](dfm-invokecommandex.md) ist eine erweiterte Version dieser Nachricht und bietet weitere Informationen für den Rückruf. Verwenden Sie **DFM \_ invokecommandex** , wenn die zusätzlichen Informationen, die von dieser Schnittstelle bereitgestellt werden, in der Implementierung benötigt werden.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




