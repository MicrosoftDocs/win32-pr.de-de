---
description: 'Ermöglicht dem Rückruf Objekt anzugeben, dass eine Animation angezeigt werden soll, während Elemente in einem Hintergrund Thread aufgelistet werden. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
ms.assetid: 6f8b3894-f08f-4ebf-a645-87869e7d1b20
title: SFVM_GETANIMATION Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60e4281689556e8315da7a9550fd69acc1a327a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131949"
---
# <a name="sfvm_getanimation-message"></a>Sfvm- \_ getanimationsmeldung

Ermöglicht dem Rückruf Objekt anzugeben, dass eine Animation angezeigt werden soll, während Elemente in einem Hintergrund Thread aufgelistet werden. Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.


```C++
SFVM_GETANIMATION 

    wParam = (WPARAM)(HINSTANCE*) phinst;

    lParam = (LPARAM)(WCHAR*) pwszName;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*phinst* \[ vorgenommen\]
</dt> <dd>

Der Instanzhandle des Moduls, aus dem die Ressource geladen werden soll.

</dd> <dt>

*pwszName* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Unicode-Zeichenfolge, die den Pfad der AVI-Datei oder den Namen einer AVI-Ressource enthält. Alternativ kann dieser Parameter aus dem Ressourcen Bezeichner im nieder wertigen Wort und 0 im höherwertigen Wort bestehen. Verwenden Sie das [**makeintresource**](/windows/win32/api/winuser/nf-winuser-makeintresourcea) -Makro, um diesen Wert zu erstellen. Das-Steuerelement lädt die Ressource aus dem durch hInst angegebenen Modul. Eine AVI-Ressource muss den Typ "AVI" aufweisen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Standardmäßig zeigt das Systemordner Ansicht-Objekt während einer hintergrundenumeration die "Taschen Taschen"-Animation an.

*phinst* und *pwszName* werden mit einer [**\_ geöffneten ACM**](../controls/acm-open.md) -Meldung an das [Animations Steuer](../controls/animation-control-overview.md) Element übergeben.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
