---
description: Ermöglicht dem Rückruf Objekt, eine Hilfe Text Zeichenfolge anzugeben.
title: DFM_GETHELPTEXT Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 40ed981b-6d03-4c4f-9e70-1a01d49edcb0
api_name:
- DFM_GETHELPTEXT
- DFM_GETHELPTEXT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b9aefb1c3a12ff00294ccc536464794a17fccfc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525364"
---
# <a name="dfm_gethelptext-message"></a>DFM- \_ GetHelpText-Nachricht

Ermöglicht dem Rückruf Objekt, eine Hilfe Text Zeichenfolge anzugeben.


```C++
DFM_GETHELPTEXT 

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

Eine mit NULL endende ANSI-Zeichenfolge, die den Hilfe Text enthält.

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
| Unicode- und ANSI-Name<br/>   | **DFM \_ GetHelpText** (ANSI)<br/>                                              |



 

 




