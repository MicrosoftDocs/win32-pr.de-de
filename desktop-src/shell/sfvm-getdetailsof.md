---
description: SFVM \_ GETDETAILSOF kann geändert werden oder nicht verfügbar sein.
ms.assetid: 46a81a7b-527c-4d41-8d25-ce65fd87416e
title: SFVM_GETDETAILSOF Nachricht (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6fd850a3f500a1d259ebdcae9e5c549ef76a8eab0d5e1d14c1385fbba8d27ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118048449"
---
# <a name="sfvm_getdetailsof-message"></a>SFVM \_ GETDETAILSOF-Nachricht

\[**SFVM \_ GETDETAILSOF** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]

Ermöglicht dem Rückrufobjekt das Angeben der Details für ein Element in einem Shell-Ordner. Verwenden Sie nur, wenn ein Aufruf von [**IShellFolder2::GetDetailsOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsof) fehlschlägt und keine [**IShellDetails::GetDetailsOf-Methode**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishelldetails-getdetailsof) zum Aufrufen verfügbar ist. Wird von [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.


```C++
SFVM_GETDETAILSOF
    wParam = (WPARAM)(int) iColumn;
    lParam = (LPARAM)(DETAILSINFO*) pDi;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*iColumn* \[ In\]
</dt> <dd>

Die nullbasierte ID der Spalte.

</dd> <dt>

*pDi* \[ out\]
</dt> <dd>

Ein Zeiger auf eine [**DETAILSINFO-Struktur,**](/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo) die mit den angeforderten Informationen gefüllt ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                |
| Ende des Supports (Client)<br/>    | Windows XP mit SP2<br/>                                                      |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                      |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
