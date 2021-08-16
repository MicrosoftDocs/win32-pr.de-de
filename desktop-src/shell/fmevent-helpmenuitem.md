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
ms.openlocfilehash: 69078274ccd8a7a7b91bbd7bd8e8d84b3b033cec6dbcf4ce495ac2ebfd0e8381
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224164"
---
# <a name="fmevent_helpmenuitem-message"></a>FMEVENT \_ HELPMENUITEM-Meldung

Wird an eine DLL-Prozedur der Datei-Manager-Erweiterung gesendet, wenn der Benutzer F1 in einem Menü- oder Symbolleistenbefehlselement drückt. Die Erweiterung sollte [**WinHelp aufrufen,**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)bei dem der *hwnd-Parameter* dieser Funktion auf den Wert des *hwnd-Parameters der Erweiterung festgelegt* ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*uItem* 
</dt> <dd>

Ein -Wert, der das Menü- oder Symbolleistenbefehlselement identifiziert, für das Hilfe gewünscht ist. Die Erweiterungsprozedur verwendet diesen Wert, um zu bestimmen, wie WinHelp am besten [**aufrufen kann.**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine DLL-Erweiterungsprozedur sollte 0 (null) zurückgeben, wenn diese Meldung verarbeitet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**FMEVENT \_ HELPSTRING**](fmevent-helpstring.md)
</dt> </dl>

 

 




