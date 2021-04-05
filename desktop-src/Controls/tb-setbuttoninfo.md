---
title: TB_SETBUTTONINFO Meldung (kommstrg. h)
description: Legt die Informationen für eine vorhandene Schaltfläche in einer Symbolleiste fest.
ms.assetid: ac9b88b9-d0d0-4669-a342-708924d97c8b
keywords:
- Windows-Steuerelemente für TB_SETBUTTONINFO Meldung
topic_type:
- apiref
api_name:
- TB_SETBUTTONINFO
- TB_SETBUTTONINFOA
- TB_SETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70612a90f245a25dde5a487917d7c3b669424ea8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859239"
---
# <a name="tb_setbuttoninfo-message"></a>TB \_ SetButtonInfo-Meldung

Legt die Informationen für eine vorhandene Schaltfläche in einer Symbolleiste fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Schaltflächen Bezeichner.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**tbbuttoninfo**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) -Struktur, die die neuen Schaltflächen Informationen enthält. Die Member **CBSIZE** und **dwMask** dieser Struktur müssen ausgefüllt werden, bevor diese Nachricht gesendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="remarks"></a>Bemerkungen

Text wird normalerweise Schaltflächen zugewiesen, wenn Sie einer Symbolleiste hinzugefügt werden, indem der Index einer Zeichenfolge im Zeichen folgen Pool der Symbolleiste angegeben wird. Wenn Sie eine **TB- \_ SetButtonInfo** verwenden, um einer Schaltfläche neuen Text zuzuweisen, wird der Text dauerhaft aus dem Zeichen folgen Pool überschrieben. Sie können den Text ändern, indem Sie **TB \_ SetButtonInfo** erneut aufrufen, aber Sie können die Zeichenfolge nicht aus dem Zeichen folgen Pool neu zuweisen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TB \_ Setbuttoninfow** (Unicode) und **TB \_ setbuttoninfoa** (ANSI)<br/>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**TB ( \_ AddButtons)**](tb-addbuttons.md)
</dt> <dt>

[**TB \_ getbuttoninfo**](tb-getbuttoninfo.md)
</dt> <dt>

[**TB \_ getbuttontext**](tb-getbuttontext.md)
</dt> <dt>

[**TB \_ GetString**](tb-getstring.md)
</dt> <dt>

[**TB ( \_ InsertButton)**](tb-insertbutton.md)
</dt> </dl>

 

 





