---
title: LB_SETTABSTOPS Meldung (Winuser. h)
description: Legt die Position der Tabstopps in einem Listenfeld fest.
ms.assetid: b96b974e-b1e6-4361-98bb-4dc21c752690
keywords:
- Windows-Steuerelemente für LB_SETTABSTOPS Meldung
topic_type:
- apiref
api_name:
- LB_SETTABSTOPS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f21927aaf82624242e8d42ef4a7459f1e36cdf74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859160"
---
# <a name="lb_settabstops-message"></a>LB- \_ settabstopps-Meldung

Legt die Position der Tabstopps in einem Listenfeld fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt die Anzahl der Tabstopps an.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf den ersten Member eines Arrays von ganzen Zahlen, das die Tabstopps enthält. Die ganzen Zahlen stellen die Anzahl von Quartalen der durchschnittlichen Zeichenbreite für die Schriftart dar, die im Listenfeld ausgewählt wird. Beispielsweise wird ein Tabstopp von 4 bei 1,0 Zeicheneinheiten platziert, und ein Tabstopp von 6 wird bei 1,5 durchschnittlichen Zeicheneinheiten platziert. Wenn das Listenfeld jedoch Teil eines Dialog Felds ist, befinden sich die ganzen Zahlen in den Dialogfeld Vorlagen Einheiten. Die Tabstopps müssen in aufsteigender Reihenfolge sortiert werden. rückwärts Registerkarten sind nicht zulässig.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn alle angegebenen Registerkarten festgelegt sind, ist der Rückgabewert " **true**". Andernfalls ist Sie **false**.

## <a name="remarks"></a>Bemerkungen

Um auf die **lb- \_ settabstopps** -Nachricht zu reagieren, muss das Listenfeld mit dem [**lbs- \_ UseTabStops**](list-box-styles.md) -Stil erstellt worden sein.

Wenn *wParam* den Wert 0 hat und *LPARAM* den Wert **null** hat, handelt es sich beim Standard-Tabstopp um zwei Dialogfeld Vorlagen Einheiten. Wenn *wParam* den Wert 1 hat, werden Tabstopps im Listenfeld durch die durch *LPARAM* angegebene Entfernung getrennt.

Wenn *LPARAM* auf mehr als einen einzelnen Wert verweist, wird für jeden Wert in *LPARAM* ein Tabstopp festgelegt, bis zu der von *wParam* angegebenen Zahl.

Die von *LPARAM* angegebenen Werte befinden sich in Dialogfeld Vorlagen Einheiten, bei denen es sich um die geräteunabhängigen Einheiten handelt, die in Dialogfeld Vorlagen verwendet werden. Verwenden Sie die [**mapdialogrect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) -Funktion, um Messungen von Dialogfeld Vorlagen-Einheiten in Bildschirm Einheiten (Pixel) zu konvertieren.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der Puffer, auf den *LPARAM* zeigt, muss sich in einem beschreibbaren Speicher befinden, auch wenn die Nachricht das Array nicht ändert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mapdialogrect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)
</dt> </dl>

 

