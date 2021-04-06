---
title: CB_GETCUEBANNER Meldung (Winuser. h)
description: Ruft den Hinweis Banner Text ab, der im Bearbeitungs Steuerelement eines Kombinations Felds angezeigt wird. Senden Sie diese Nachricht explizit oder mithilfe des ComboBox \_ getcuebannertext-Makros.
ms.assetid: 38959228-9f07-4636-a1ea-681efe77b9ec
keywords:
- Windows-Steuerelemente für CB_GETCUEBANNER Meldung
topic_type:
- apiref
api_name:
- CB_GETCUEBANNER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866f51df0083c4cd72c3f34bb3ce045e0f577a24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859019"
---
# <a name="cb_getcuebanner-message"></a>CB \_ getcuebanner-Meldung

Ruft den Hinweis Banner Text ab, der im Bearbeitungs Steuerelement eines Kombinations Felds angezeigt wird. Senden Sie diese Nachricht explizit oder mithilfe des [**ComboBox \_ getcuebannertext**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getcuebannertext) -Makros.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Ein Zeiger auf einen Unicode-Zeichen folgen Puffer, der den Hinweis Banner Text empfängt. Die aufrufenden Anwendung ist dafür verantwortlich, den Speicher für den Puffer zuzuweisen. Die Puffergröße muss gleich der Länge der Hinweis Banner Zeichenfolge in **WCHARs** Plus 1 für das abschließende Null-  **WCHAR** sein.

</dd> <dt>

*LPARAM* \[ in\]
</dt> <dd>

Die Größe des Puffers, auf den von *lpcwtext* in **WCHARs** verwiesen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 1 zurück, wenn erfolgreich, oder andernfalls einen Fehlerwert.

Wenn kein Hinweis Banner Text vorhanden ist, ist der Rückgabewert 0. Wenn die aufrufende Anwendung keinen Puffer zuweist oder *LPARAM* vor dem Senden dieser Nachricht festgelegt wird, kann es zu einem nicht definierten Verhalten kommen, und der Rückgabewert ist möglicherweise nicht zuverlässig.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kombinations Feld-Features](combo-box-features.md)
</dt> </dl>

 

 





