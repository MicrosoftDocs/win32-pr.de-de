---
description: Wird an eine DLL-Prozedur der Datei-Manager-Erweiterung gesendet, wenn der Benutzer F1 in einem Menü- oder Symbolleistenbefehlselement drückt. Die Erweiterung sollte WinHelp aufrufen, bei dem der hwnd-Parameter dieser Funktion auf den Wert des hwnd-Parameters der Erweiterung festgelegt ist.
title: FMEVENT_HELPMENUITEM (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_HELPMENUITEM
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 6298061d-7e24-45ab-8bc4-96b28e071080
ms.openlocfilehash: 46cb246e91f9901204432527ba36fd8ac72beba4
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842311"
---
# <a name="fmevent_helpmenuitem-message"></a>FMEVENT \_ HELPMENUITEM-Meldung

Wird an eine DLL-Prozedur der Datei-Manager-Erweiterung gesendet, wenn der Benutzer F1 in einem Menü- oder Symbolleistenbefehlselement drückt. Die Erweiterung sollte [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)aufrufen, bei dem der *hwnd-Parameter* dieser Funktion auf den Wert des *hwnd-Parameters der Erweiterung festgelegt* ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*uItem* 
</dt> <dd>

Ein -Wert, der das Menü- oder Symbolleistenbefehlselement identifiziert, für das Hilfe gewünscht ist. Die Erweiterungsprozedur verwendet diesen Wert, um zu bestimmen, wie WinHelp am besten [**aufruft.**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine DLL-Erweiterungsprozedur sollte 0 (null) zurückgeben, wenn diese Meldung verarbeitet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**FMEVENT \_ HELPSTRING**](fmevent-helpstring.md)
</dt> </dl>

 

 




