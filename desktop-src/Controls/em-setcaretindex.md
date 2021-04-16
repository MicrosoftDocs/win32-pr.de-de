---
title: EM_SETCARETINDEX Meldung (kommstrg. h)
description: Legt den NULL basierten Indexwert der Position der Einfügemarke in einem Bearbeitungs Steuerelement fest.
ms.assetid: 5cb7ff1e-18e8-49c8-8072-872cf32b18b0
keywords:
- Windows-Steuerelemente für EM_SETCARETINDEX Meldung
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
ms.openlocfilehash: ea0c49ebad91532e82dc7e96facb62f38b2abfa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478579"
---
# <a name="em_setcaretindex-message"></a>EM \_ setcaretindex-Meldung

Legt den NULL basierten Indexwert der Position der Einfügemarke in einem Bearbeitungs Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der neue null basierte Indexwert der Position der Einfügemarke.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn der Index außerhalb des Bereichs des Texts in einem Bearbeitungs Steuerelement liegt, wird der Index so angepasst, dass er in den Textbereich passt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10, 1809 \[ Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2019 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**EM \_ getcaretindex**](em-getcaretindex.md)
</dt> </dl>

 

 





