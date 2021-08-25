---
title: EM_LINESCROLL (Winuser.h)
description: Führt einen Bildlauf für den Text in einem mehrzeilenigen Bearbeitungssteuerfeld durch.
ms.assetid: 5398082d-f1ef-4a3a-9e5a-83cf286adbf1
keywords:
- EM_LINESCROLL meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- EM_LINESCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6da4adbd789a8d9ae3344a1a49d39c7f5fbe22b7ec1ca51fcc6cead98ea7780
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048640"
---
# <a name="em_linescroll-message"></a>EM \_ LINESCROLL-Nachricht

Führt einen Bildlauf für den Text in einem mehrzeilenigen Bearbeitungssteuerfeld durch.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

**Steuerelemente bearbeiten:** Die Anzahl der Zeichen, die horizontal gescrollt werden soll.

**Umfangreiche Bearbeitungssteuerelemente:** Dieser Parameter wird nicht verwendet. muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Die Anzahl der Zeilen, die vertikal gescrollt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht an ein mehrstufiges Bearbeitungssteuerteil gesendet wird, ist der Rückgabewert **TRUE.**

Wenn die Nachricht an ein einzeilenbasiertes Bearbeitungssteuer steuerelement gesendet wird, ist der Rückgabewert **FALSE.**

## <a name="remarks"></a>Hinweise

Das Steuerelement führt keinen vertikalen Bildlauf über die letzte Textzeile im Bearbeitungssteuerfeld durch. Wenn die aktuelle Zeile plus die Anzahl der vom *lParam-Parameter* angegebenen Zeilen die Gesamtzahl der Zeilen im Bearbeitungssteuerfeld überschreitet, wird der Wert so angepasst, dass die letzte Zeile des Bearbeitungssteuerfelds nach oben im Bearbeitungssteuerfenster gescrollt wird.

**Steuerelemente bearbeiten:** Die **MELDUNG EM \_ LINESCROLL** führt einen vertikalen oder horizontalen Bildlauf des Texts in einem mehrzeigen Bearbeitungssteuerfeld durch. Die **EM \_ LINESCROLL-Meldung** kann verwendet werden, um horizontal nach dem letzten Zeichen einer beliebigen Zeile zu scrollen.

**Umfangreiche Bearbeitung:** Wird in Microsoft Rich Edit 1.0 und höher unterstützt. Die **MELDUNG EM \_ LINESCROLL** führt einen vertikalen Bildlauf des Texts in einem mehrzeigen Bearbeitungssteuerfeld durch. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



 

 





