---
title: TB_GETBUTTONTEXT Meldung (kommstrg. h)
description: Ruft den Anzeige Text einer Schaltfläche auf einer Symbolleiste ab.
ms.assetid: 16dd7181-a404-4056-b084-05f49f5a4b14
keywords:
- Windows-Steuerelemente für TB_GETBUTTONTEXT Meldung
topic_type:
- apiref
api_name:
- TB_GETBUTTONTEXT
- TB_GETBUTTONTEXTA
- TB_GETBUTTONTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ac0b238574cc136f41959b57f3f0e1ec13e3ea1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104181"
---
# <a name="tb_getbuttontext-message"></a>TB \_ getbuttontext-Nachricht

Ruft den Anzeige Text einer Schaltfläche auf einer Symbolleiste ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Befehls Bezeichner der Schaltfläche, deren Text abgerufen werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf einen Puffer, der den Schaltflächen Text empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Länge der Zeichenfolge, auf die *LPARAM* zeigt, in Zeichen zurück. Die Länge enthält nicht das abschließende Null Zeichen. Wenn nicht erfolgreich, ist der Rückgabewert-1.

## <a name="remarks"></a>Bemerkungen

**Sicherheitswarnung:** Wenn Sie diese Meldung falsch verwenden, kann dies die Sicherheit des Programms beeinträchtigen. Diese Meldung bietet keine Möglichkeit, die Größe des Puffers zu kennen. Wenn Sie diese Meldung verwenden, müssen Sie zuerst die Nachricht mit der Übergabe von **null** im *LPARAM*-Element aufzurufen. Dadurch wird die Anzahl der Zeichen zurückgegeben, ausgenommen **null** . Rufen Sie dann die Nachricht ein zweites Mal auf, um die Zeichenfolge abzurufen. Überprüfen Sie die [Sicherheitsaspekte: Microsoft Windows](sec-comctls.md) -Steuerelemente, bevor Sie fortfahren.

Die zurückgegebene Zeichenfolge entspricht dem Text, der derzeit von der Schaltfläche angezeigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TB \_ Getbuttontextw** (Unicode) und **TB \_ getbuttontexta** (ANSI)<br/>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**TB \_ getbuttoninfo**](tb-getbuttoninfo.md)
</dt> <dt>

[**TB \_ GetString**](tb-getstring.md)
</dt> <dt>

[**TB \_ SetButtonInfo**](tb-setbuttoninfo.md)
</dt> </dl>

 

 





