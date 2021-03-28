---
description: Ermöglicht dem Rückruf Objekt, eine Hilfe Text Zeichenfolge anzugeben.
title: DFM_GETHELPTEXTW Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 85bdd1d0-5b68-44a5-a1b0-4845b5be34d0
api_name:
- DFM_GETHELPTEXTW
- DFM_GETHELPTEXTW
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7ac1e41046b2d757df96e9acf5722710ae832bf4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977296"
---
# <a name="dfm_gethelptextw-message"></a>DFM- \_ gethelptextw-Meldung

Ermöglicht dem Rückruf Objekt, eine Hilfe Text Zeichenfolge anzugeben.


```C++
DFM_GETHELPTEXTW 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(WPTSTR) pszText;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*idcmd \_ cchmax* \[ in\]
</dt> <dd>

Das nieder wertige Wort dieses Parameters enthält die Befehls-ID. Das höchst wertige Wort enthält die Anzahl der Zeichen im *pszText* -Puffer.

</dd> <dt>

*pszText* \[ vorgenommen\]
</dt> <dd>

Eine NULL-terminierte Unicode-Zeichenfolge mit dem Hilfetext.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Nachricht wird entweder an die Rückruffunktion oder an das Rückruf Objekt gesendet, je nachdem, wie das standardmäßige Kontextmenü Objekt erstellt wird. Es gibt zwei APIs für die Erstellung, [**cdeffoldermenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**shkreatedefaultcontextmenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ Invokecommandex**](dfm-invokecommandex.md) ist eine erweiterte Version dieser Nachricht und bietet weitere Informationen für den Rückruf. Verwenden Sie **DFM \_ invokecommandex** , wenn die zusätzlichen Informationen, die von dieser Schnittstelle bereitgestellt werden, in der Implementierung benötigt werden.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **DFM \_ Gethelptextw** (Unicode)<br/>                                          |



 

 




