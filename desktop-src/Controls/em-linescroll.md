---
title: EM_LINESCROLL Meldung (Winuser. h)
description: Scrollt den Text in einem mehrzeiligen Bearbeitungs Steuerelement.
ms.assetid: 5398082d-f1ef-4a3a-9e5a-83cf286adbf1
keywords:
- Windows-Steuerelemente für EM_LINESCROLL Meldung
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
ms.openlocfilehash: 646e225ef269ccddca2cdc29caf635d94c1671e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040803"
---
# <a name="em_linescroll-message"></a>EM \_ linescroll-Nachricht

Scrollt den Text in einem mehrzeiligen Bearbeitungs Steuerelement.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Steuer **Elemente bearbeiten:** Die Anzahl der Zeichen, die horizontal durchlaufen werden sollen.

**Rich Edit-Steuerelemente:** Dieser Parameter wird nicht verwendet. Er muss NULL sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Die Anzahl der Zeilen, für die vertikale Bildläufe durchführen

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht an ein mehrzeilige Bearbeitungs Steuerelement gesendet wird, ist der Rückgabewert " **true**".

Wenn die Nachricht an ein einzeilige Bearbeitungs Steuerelement gesendet wird, ist der Rückgabewert **false**.

## <a name="remarks"></a>Bemerkungen

Das-Steuerelement scrollt nicht vertikal nach der letzten Textzeile im Bearbeitungs Steuerelement. Wenn die aktuelle Zeile zuzüglich der durch den *LPARAM* -Parameter angegebenen Anzahl von Zeilen die Gesamtzahl der Zeilen im Bearbeitungs Steuerelement überschreitet, wird der Wert so angepasst, dass die letzte Zeile des Bearbeitungs Steuer Elements auf den oberen Rand des Fensters zum Bearbeiten von Steuerelementen gescrollt wird.

Steuer **Elemente bearbeiten:** Die **\_ gelinescroll** -Nachricht scrollt den Text vertikal oder horizontal in einem mehrzeiligen Bearbeitungs Steuerelement. Die **EM \_ linescroll** -Nachricht kann verwendet werden, um einen horizontalen Bildlauf nach dem letzten Zeichen einer beliebigen Zeile durchführen.

Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt. Die **\_ gelinescroll** -Nachricht führt einen vertikalen Bildlauf in einem mehrzeiligen Bearbeitungs Steuerelement aus. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



 

 





