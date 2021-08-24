---
title: EM_SETCARETINDEX (CommCtrl.h)
description: Legt den nullbasierten Indexwert der Position des Caretwerts in einem Bearbeitungssteuerpunkt fest.
ms.assetid: 5cb7ff1e-18e8-49c8-8072-872cf32b18b0
keywords:
- EM_SETCARETINDEX meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- EM_SETCARETINDEX
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 8b80202ed5294828441abcfa66a914514e31944902e52926de7fa3af92794b46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799960"
---
# <a name="em_setcaretindex-message"></a>EM \_ SETCARETINDEX-Meldung

Legt den nullbasierten Indexwert der Position des Caretwerts in einem Bearbeitungssteuerpunkt fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der neue nullbasierte Indexwert der Position des Caretpunkts.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn der Index außerhalb des Bereichs des Texts in einem Bearbeitungssteuerfeld liegt, wird der Index so angepasst, dass er in den Textbereich passt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur 1809 \[ Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2019-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**EM \_ GETCARETINDEX**](em-getcaretindex.md)
</dt> </dl>

 

 





