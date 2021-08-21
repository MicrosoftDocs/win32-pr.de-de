---
title: TB_SAVERESTORE Meldung (Commctrl.h)
description: Senden Sie diese Meldung, um das Speichern oder Wiederherstellen eines Symbolleistenzustands zu initiieren.
ms.assetid: 59f51d07-cd08-4d6f-9d19-614064ba6f20
keywords:
- TB_SAVERESTORE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TB_SAVERESTORE
- TB_SAVERESTOREA
- TB_SAVERESTOREW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94d04c16fda40bf66736431a684398eddf313529c669cc6db9ec49fbaad4f6f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168023"
---
# <a name="tb_saverestore-message"></a>\_TB SAVERESTORE-Nachricht

Senden Sie diese Meldung, um das Speichern oder Wiederherstellen eines Symbolleistenzustands zu initiieren.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Speicher- oder Wiederherstellungsflag. Wenn dieser Parameter **TRUE** ist, werden die Informationen gespeichert. Wenn false **ist,** werden die Informationen wiederhergestellt.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**TBSAVEPARAMS-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-tbsaveparamsa) die den Registrierungsschlüssel, den Unterschlüssel und den Wertnamen für die Symbolleistenzustandsinformationen angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Für Version 4.72 und früher muss das übergeordnete Fenster des Symbolleistensteuerelements einen Handler für den [TBN \_ GETBUTTONINFO-Benachrichtigungscode](tbn-getbuttoninfo.md) implementieren, um diese Meldung zum Speichern oder Wiederherstellen einer Symbolleiste zu verwenden. Die Symbolleiste gibt diese Benachrichtigung aus, um Informationen zu jeder Schaltfläche abzurufen, während sie wiederhergestellt wird.

Version 5.80 enthält eine neue Speicher-/Wiederherstellungsoption. Zu Beginn des Prozesses und wenn jede Schaltfläche gespeichert oder wiederhergestellt wird, erhält Ihre Anwendung eine [TBN \_ SAVE-](tbn-save.md) oder [TBN \_ RESTORE-Benachrichtigung.](tbn-restore.md) Um diese Option verwenden zu können, müssen Sie Benachrichtigungshandler implementieren, um der Shell die Bitmap- und Zustandsinformationen bereitzustellen, die sie zum erfolgreichen Speichern oder Wiederherstellen des Symbolleistenzustands benötigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TB \_ SAVERESTOREW** (Unicode) und **TB \_ SAVERESTOREA** (ANSI)<br/>             |



 

 





