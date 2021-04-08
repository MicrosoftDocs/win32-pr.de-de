---
title: PSM_SETTITLE Meldung (prsht. h)
description: Legt den Titel eines Eigenschaften Blatts fest. Sie können diese Nachricht explizit oder mithilfe des propsheet- \_ Makros SetTitle senden.
ms.assetid: 53ce8e20-4554-41f4-bad9-fb24c2c93c34
keywords:
- Windows-Steuerelemente für PSM_SETTITLE Meldung
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
ms.openlocfilehash: 1a848a5bdaeaae64b6f1825740d1e8ade07a5a22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949457"
---
# <a name="psm_settitle-message"></a>PSM- \_ SetTitle-Nachricht

Legt den Titel eines Eigenschaften Blatts fest. Sie können diese Nachricht explizit oder mithilfe des [**propsheet-Makros \_ SetTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Flag, das angibt, ob das Präfix "Eigenschaften für" oder das Suffix "Properties" (abhängig von der Version) mit der angegebenen Titel Zeichenfolge eingeschlossen werden soll. Wenn dieser Wert "PSH \_ proptitle" ist, ist das Präfix oder Suffix enthalten.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf einen Puffer, der die Titel Zeichenfolge enthält. Wenn das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) dieses Parameters **null** ist, lädt das Eigenschaften Blatt die im [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))angegebene Zeichen folgen Ressource.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

In einem Aero-Assistenten kann diese Meldung verwendet werden, um den Titel einer inneren Seite dynamisch zu ändern. Dies ist beispielsweise der Fall, wenn die " [PSN \_ SETACTIVE](psn-setactive.md) "-Benachrichtigung

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **PSM \_ Settitlew** (Unicode) und **PSM \_ settitlea** (ANSI)<br/>              |



 

