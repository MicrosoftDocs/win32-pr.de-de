---
description: Ermöglicht dem Rückrufobjekt anzugeben, dass eine Animation angezeigt wird, während Elemente in einem Hintergrundthread aufzählt werden. Wird von IShellFolderViewCB::MessageSFVCB verwendet.
ms.assetid: 6f8b3894-f08f-4ebf-a645-87869e7d1b20
title: SFVM_GETANIMATION (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 746d8bc9bc4a6d4e15d9cd5190d7cfcb7d1362daba8ec5478b333458f62787da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008990"
---
# <a name="sfvm_getanimation-message"></a>SFVM \_ GETANIMATION-Nachricht

Ermöglicht dem Rückrufobjekt anzugeben, dass eine Animation angezeigt wird, während Elemente in einem Hintergrundthread aufzählt werden. Wird von [**IShellFolderViewCB::MessageSFVCB verwendet.**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)


```C++
SFVM_GETANIMATION 

    wParam = (WPARAM)(HINSTANCE*) phinst;

    lParam = (LPARAM)(WCHAR*) pwszName;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*phinst* \[ out\]
</dt> <dd>

Das Instanzhand handle des Moduls, aus dem die Ressource geladen werden soll.

</dd> <dt>

*pwszName* \[ out\]
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Unicode-Zeichenfolge, die den Pfad der .avi datei oder den Namen einer AVI-Ressource enthält. Alternativ kann dieser Parameter aus dem Ressourcenbezeichner im niedrigwertig angegebenen Wort und 0 im hohen Wort bestehen. Verwenden Sie zum Erstellen dieses Werts das [**MAKEINTRESOURCE-Makro.**](/windows/win32/api/winuser/nf-winuser-makeintresourcea) Das Steuerelement lädt die Ressource aus dem durch hinst angegebenen Modul. Eine AVI-Ressource muss den Typ "AVI" haben.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Standardmäßig zeigt das Ansichtsobjekt des Systemordners die "Taschenlampenanimation" während einer Hintergrundenumeration an.

*phinst und* *pwszName* werden [](../controls/animation-control-overview.md) mit einer ACM OPEN-Nachricht an das [**\_ Animationssteuersystem**](../controls/acm-open.md) übergeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
