---
title: EM_SETTABSTOPS Meldung (Winuser. h)
description: Die \_ gesettabstopps-Meldung legt die Tabstopps in einem mehrzeiligen Bearbeitungs Steuerelement fest.
ms.assetid: d6fe2828-4ae9-4652-ace0-2f71e146f777
keywords:
- Windows-Steuerelemente für EM_SETTABSTOPS Meldung
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
ms.openlocfilehash: 48d076dea415f169eff46101fd7cfe632d73d976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104211"
---
# <a name="em_settabstops-message"></a>EM \_ settabstopps-Meldung

Die **\_ gesettabstopps** -Meldung legt die Tabstopps in einem mehrzeiligen Bearbeitungs Steuerelement fest. Wenn Text in das-Steuerelement kopiert wird, bewirkt jedes Tabulator Zeichen im Text, dass der Bereich bis zum nächsten Tabstopp Zeichen generiert wird.

Diese Meldung wird nur von mehrzeiligen Bearbeitungs Steuerelementen verarbeitet. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Anzahl der Tabstopps, die im Array enthalten sind. Wenn dieser Parameter NULL ist, wird der *LPARAM* -Parameter ignoriert, und Standard Tabstopps werden bei jeder 32-Dialogfeld Vorlagen-Einheit festgelegt. Wenn dieser Parameter 1 ist, werden Tabstopps bei allen *n* Dialogfeld Vorlagen Einheiten festgelegt, wobei *n* der Abstand ist, auf den der *LPARAM* -Parameter zeigt. Wenn dieser Parameter größer als 1 ist, ist *LPARAM* ein Zeiger auf ein Array von Tabstopps.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf ein Array von ganzen Zahlen ohne Vorzeichen, das die Tabstopps in Dialogfeld Vorlagen Einheiten angibt. Wenn der *wParam* -Parameter 1 ist, ist dieser Parameter ein Zeiger auf eine ganze Zahl ohne Vorzeichen, die den Abstand zwischen allen Tabstopps in Dialogfeld Vorlagen Einheiten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn alle Registerkarten festgelegt sind, ist der Rückgabewert " **true**".

Wenn nicht alle Registerkarten festgelegt sind, ist der Rückgabewert **false**.

## <a name="remarks"></a>Bemerkungen

Die Meldung " **EM \_ settabstopps** " zeichnet das Bearbeitungs Steuerelement Fenster nicht automatisch neu auf. Wenn die Anwendung die Tabstopps für Text ändert, der sich bereits im Bearbeitungs Steuerelement befindet, sollte Sie die [**invalidatup**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) -Funktion aufrufen, um das Bearbeitungs Steuerelement Fenster neu zu zeichnen.

Die im Array angegebenen Werte befinden sich in Dialogfeld Vorlagen Einheiten, die die geräteunabhängigen Einheiten sind, die in Dialogfeld Vorlagen verwendet werden. Verwenden Sie die [**mapdialogrect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) -Funktion, um Messungen von Dialogfeld Vorlagen-Einheiten in Bildschirm Einheiten (Pixel) zu konvertieren.

Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 3,0 und höher unterstützt. Ein Rich-Edit-Steuerelement kann die maximale Anzahl von Tabstopps aufweisen, die durch maximale \_ \_ Tabstopps angegeben werden. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Invalidateruieren**](/windows/desktop/api/winuser/nf-winuser-invalidaterect)
</dt> <dt>

[**Mapdialogrect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)
</dt> </dl>

 

