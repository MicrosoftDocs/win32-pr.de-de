---
title: TB_SAVERESTORE Meldung (kommstrg. h)
description: Senden Sie diese Nachricht, um das Speichern oder Wiederherstellen eines Symbolleisten Zustands zu initiieren.
ms.assetid: 59f51d07-cd08-4d6f-9d19-614064ba6f20
keywords:
- Windows-Steuerelemente für TB_SAVERESTORE Meldung
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
ms.openlocfilehash: 5e87e4ddbed87e81a88c8711c9931dcf95cf9e59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858637"
---
# <a name="tb_saverestore-message"></a>TB \_ saverestore-Nachricht

Senden Sie diese Nachricht, um das Speichern oder Wiederherstellen eines Symbolleisten Zustands zu initiieren.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Flag zum Speichern oder wiederherstellen. Wenn dieser Parameter **true** ist, werden die Informationen gespeichert. Wenn der Wert **false** ist, werden die Informationen wieder hergestellt.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**tbsaveparameams**](/windows/win32/api/commctrl/ns-commctrl-tbsaveparamsa) -Struktur, die den Registrierungsschlüssel, den Unterschlüssel und den Wert Namen für die Statusinformationen der Symbolleiste angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Damit diese Meldung in Version 4,72 und früher zum Speichern oder Wiederherstellen einer Symbolleiste verwendet werden kann, muss das übergeordnete Fenster des Toolbar-Steuer Elements einen Handler für den [TBN \_ getbuttoninfo](tbn-getbuttoninfo.md) -Benachrichtigungs Code implementieren. Diese Benachrichtigung wird von der Symbolleiste ausgegeben, um Informationen zu jeder Schaltfläche abzurufen, während Sie wieder hergestellt wird.

Version 5,80 enthält eine neue Option zum Speichern/Wiederherstellen. Zu Beginn des Vorgangs wird für die Anwendung eine TBN-oder [TBN- \_ Wiederherstellungs](tbn-restore.md) Benachrichtigung angezeigt, sobald die Schaltfläche gespeichert oder wieder hergestellt wird. [ \_ ](tbn-save.md) Um diese Option verwenden zu können, müssen Sie Benachrichtigungs Handler implementieren, um der Shell die Bitmap-und Zustandsinformationen zur Verfügung zu stellen, die Sie zum erfolgreichen speichern oder Wiederherstellen des Toolbar-Zustands benötigen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TB \_ Saverestorew** (Unicode) und **TB \_ saverestorea** (ANSI)<br/>             |



 

 





