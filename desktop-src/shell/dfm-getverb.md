---
description: Wird von der standardmäßigen Kontextmenü Implementierung gesendet, um das Verb für die angegebene Befehls-ID im Kontextmenü zu erhalten.
title: DFM_GETVERB Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bd12a38e-4d50-43ad-9d1f-8fefa90b44f9
api_name:
- DFM_GETVERB
- DFM_GETVERBA
- DFM_GETVERBW
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bbb1b2fb54aa2b0e4b66cf8fc559c56eb279504d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214430"
---
# <a name="dfm_getverb-message"></a>DFM \_ getverb-Nachricht

Wird von der standardmäßigen Kontextmenü Implementierung gesendet, um das Verb für die angegebene Befehls-ID im Kontextmenü zu erhalten.


```C++

                DFM_GETVERB 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*idcmd \_ cchmax* \[ in\]
</dt> <dd>

Das nieder wertige Wort dieses Parameters enthält die Befehls-ID. Das höchst wertige Wort enthält die Anzahl der Zeichen im *pszText* -Puffer.

</dd> <dt>

*pszText* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Verb Text enthält.

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
| Unicode- und ANSI-Name<br/>   | **DFM \_ Getverbw** (Unicode) und **DFM \_ getverba** (ANSI)<br/>                 |



 

 




