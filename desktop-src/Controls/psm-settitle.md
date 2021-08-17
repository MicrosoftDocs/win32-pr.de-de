---
title: PSM_SETTITLE-Nachricht (Prsht.h)
description: Legt den Titel eines Eigenschaftenblatts fest. Sie können diese Nachricht explizit oder mit dem PropSheet \_ SetTitle-Makro senden.
ms.assetid: 53ce8e20-4554-41f4-bad9-fb24c2c93c34
keywords:
- PSM_SETTITLE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- PSM_SETTITLE
- PSM_SETTITLEA
- PSM_SETTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 782d5ebf3e7fe0850b89d9f52f0dc5c406dbd41c9bdad694b41b8ae9ea4c8b0e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985450"
---
# <a name="psm_settitle-message"></a>PSM \_ SETTITLE-Nachricht

Legt den Titel eines Eigenschaftenblatts fest. Sie können diese Nachricht explizit oder mit dem [**PropSheet \_ SetTitle-Makro**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Flag, das angibt, ob das Präfix "Properties for" oder das Suffix "Properties" (abhängig von der Version) mit der angegebenen Titelzeichenfolge eingeschlossen werden soll. Wenn dieser Wert PSH \_ PROPTITLE ist, wird das Präfix oder Suffix eingeschlossen.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf einen Puffer, der die Titelzeichenfolge enthält. Wenn das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) dieses Parameters **NULL** ist, lädt das Eigenschaftenblatt die zeichenfolgenressource, die im [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))angegeben ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

In einem Assistenten kann diese Meldung verwendet werden, um den Titel einer inneren Seite dynamisch zu ändern. beispielsweise bei der Behandlung der [PSN \_ SETACTIVE-Benachrichtigung.](psn-setactive.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **PSM \_ SETTITLEW** (Unicode) und **PSM \_ SETTITLEA** (ANSI)<br/>              |



 

