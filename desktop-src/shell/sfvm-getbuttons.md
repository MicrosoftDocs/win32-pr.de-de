---
description: 'Ermöglicht dem Rückruf Objekt die Angabe der Schaltflächen, die der Symbolleiste hinzugefügt werden sollen. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
ms.assetid: 0c0dbf61-9da9-4bcc-bad9-92c3f78db78f
title: SFVM_GETBUTTONS Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ad4ced86909c37ec77bf0470b46a40954f5b61c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866780"
---
# <a name="sfvm_getbuttons-message"></a>Sfvm \_ getButtons-Meldung

Ermöglicht dem Rückruf Objekt die Angabe der Schaltflächen, die der Symbolleiste hinzugefügt werden sollen. Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.


```C++
SFVM_GETBUTTONS 

    wParam = (WPARAM)(DWORD) idCmdFirst,cbtnMax;

    lParam = (LPARAM)(LPTBBUTTON) pbtn;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*idcmdfirst \_ cbtnmax* \[ in\]
</dt> <dd>

Enthält 2 16-Bit-Werte, die mit dem [**makewparam**](/windows/win32/api/winuser/nf-winuser-makewparam) -Makro in den-Parameter gepackt wurden. Das nieder wertige Wort enthält die anfängliche Befehls-ID. Das höchst wertige Wort enthält die Anzahl der hinzu zufügenden Schaltflächen, wie in der vorstehenden [**sfvm \_ getbuttoninfo**](sfvm-getbuttoninfo.md) -Meldung angegeben.

</dd> <dt>

*pbtn* \[ vorgenommen\]
</dt> <dd>

Die Adresse eines Arrays von [**TBBUTTON**](/windows/win32/api/commctrl/ns-commctrl-tbbutton) -Strukturen, eines für jede Schaltfläche, die der Symbolleiste hinzugefügt werden soll.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Dieser Nachricht wird eine [**sfvm \_ getbuttoninfo**](sfvm-getbuttoninfo.md) -Meldung vorangestellt. Das Rückruf Objekt muss diese Nachricht verarbeiten, um die Anzahl der Schaltflächen und die Position anzugeben, an der Sie auf der Symbolleiste platziert werden sollen. Abhängig davon, wie das Rückruf Objekt auf die **sfvm \_ getbuttoninfo** -Nachricht antwortet, werden die durch den *pbtn* -Parameter angegebenen Schaltflächen den Standard Schaltflächen des Systemordner Ansichts Objekts angefügt oder der Standardgruppe ersetzt.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
