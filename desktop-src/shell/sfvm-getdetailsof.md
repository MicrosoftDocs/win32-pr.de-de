---
description: Sfvm \_ GetDetailsOf kann geändert werden oder ist nicht verfügbar.
ms.assetid: 46a81a7b-527c-4d41-8d25-ce65fd87416e
title: SFVM_GETDETAILSOF Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6170c0fc8dc29435b2c6f2bb033f30706ccb7b33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980217"
---
# <a name="sfvm_getdetailsof-message"></a>Sfvm \_ GetDetailsOf-Meldung

\[**Sfvm \_ "GetDetailsOf** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]

Ermöglicht dem Rückruf Objekt, die Details für ein Element in einem Shellordner bereitzustellen. Verwenden Sie nur, wenn ein Rückruf [**von IShellFolder2:: GetDetailsOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsof) fehlschlägt und keine [**ishelldetails:: GetDetailsOf**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishelldetails-getdetailsof) -Methode zum Aufrufen verfügbar ist. Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.


```C++
SFVM_GETDETAILSOF
    wParam = (WPARAM)(int) iColumn;
    lParam = (LPARAM)(DETAILSINFO*) pDi;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*icolumn* \[ in\]
</dt> <dd>

Die null basierte ID der Spalte.

</dd> <dt>

*PDI* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine [**detailsinfo**](/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo) -Struktur, die mit den angeforderten Informationen gefüllt ist.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                |
| Ende des Supports (Client)<br/>    | Windows XP mit SP2<br/>                                                      |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                      |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
