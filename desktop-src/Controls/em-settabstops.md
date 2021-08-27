---
title: EM_SETTABSTOPS (Winuser.h)
description: Die Meldung EM \_ SETTABSTOPS legt die Registerkartenstopps in einem mehrstufigen Bearbeitungssteuerfeld fest.
ms.assetid: d6fe2828-4ae9-4652-ace0-2f71e146f777
keywords:
- EM_SETTABSTOPS von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- EM_SETTABSTOPS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2bf8285bbc8830f784b6cf2cf6671634bf4339a418c163bc3962150d6cb6674
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048080"
---
# <a name="em_settabstops-message"></a>EM \_ SETTABSTOPS-Meldung

Die **Meldung EM \_ SETTABSTOPS legt** die Registerkartenstopps in einem mehrstufigen Bearbeitungssteuerfeld fest. Wenn Text in das Steuerelement kopiert wird, bewirkt jedes Tabstoppzeichen im Text, dass bis zum nächsten Tabstopp Leerzeichen generiert werden.

Diese Meldung wird nur von mehrline-Bearbeitungssteuerelementen verarbeitet. Sie können diese Nachricht entweder an ein Bearbeitungssteuer steuerelement oder an ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Anzahl der Registerkartenstopps, die im Array enthalten sind. Wenn dieser Parameter 0 (null) ist, wird der *lParam-Parameter* ignoriert, und standardmäßige Tabstopps werden bei jeder 32 Dialogvorlageneinheit festgelegt. Wenn dieser Parameter 1 ist, werden Tabstopps bei jeder *n* Dialogvorlageneinheiten festgelegt, wobei *n* der Abstand ist, auf den der *lParam-Parameter* zeigt. Wenn dieser Parameter größer als 1 ist, *ist lParam* ein Zeiger auf ein Array von Tabstopps.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf ein Array von ganzen Zahlen ohne Vorzeichen, die die Tabstopps angeben, in Dialogvorlageneinheiten. Wenn der *wParam-Parameter* 1 ist, ist dieser Parameter ein Zeiger auf eine ganze Zahl ohne Vorzeichen, die den Abstand zwischen allen Tabstopps in Dialogvorlageneinheiten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn alle Registerkarten festgelegt sind, ist der Rückgabewert **TRUE.**

Wenn nicht alle Registerkarten festgelegt sind, ist der Rückgabewert **FALSE.**

## <a name="remarks"></a>Hinweise

Die **MELDUNG \_ EM SETTABSTOPS** wird nicht automatisch im Bearbeitungssteuerungsfenster neu gezeichnet. Wenn die Anwendung die Registerkartenstopps für Text ändert, der sich bereits im Bearbeitungssteuerfeld befindet, sollte sie die [**InvalidateRect-Funktion**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) aufrufen, um das Bearbeitungssteuersteuerfenster neu zu zeichnet.

Die im Array angegebenen Werte befinden sich in Dialogvorlageneinheiten, bei denen es sich um geräteunabhängige Einheiten handelt, die in Dialogfeldvorlagen verwendet werden. Um Messungen von Dialogvorlageneinheiten in Bildschirmeinheiten (Pixel) zu konvertieren, verwenden Sie die [**MapDialogRect-Funktion.**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)

**Umfangreiche Bearbeitung:** Wird in Microsoft Rich Edit 3.0 und höher unterstützt. Bei einem Rich-Edit-Steuerelement kann die maximale Anzahl von Tabstopps angegeben werden, die von MAX \_ TAB \_ STOPS angegeben wird. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Andere Ressourcen**
</dt> <dt>

[**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect)
</dt> <dt>

[**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)
</dt> </dl>

 

