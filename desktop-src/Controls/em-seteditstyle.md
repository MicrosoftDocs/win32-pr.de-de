---
title: EM_SETEDITSTYLE Meldung (RichEdit. h)
description: Legt die aktuellen Flags für Bearbeitungs Stile für ein Rich-Edit-Steuerelement fest.
ms.assetid: e48de6b3-0fd2-4791-9863-a6dcdafa3642
keywords:
- Windows-Steuerelemente für EM_SETEDITSTYLE Meldung
topic_type:
- apiref
api_name:
- EM_SETEDITSTYLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14c7b7e1d3990a00fb6931ed39bbd28aa6f8c2ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518671"
---
# <a name="em_seteditstyle-message"></a>EM- \_ Nachricht

Legt die aktuellen Flags für Bearbeitungs Stile für ein Rich-Edit-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt ein oder mehrere Bearbeitungs Stil Flags an. Eine Liste möglicher Werte finden Sie unter [**EM \_ GetEditStyle**](em-geteditstyle.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Eine Maske, die aus einem oder mehreren der *wParam* -Werte besteht. Nur die in dieser Maske angegebenen Werte werden festgelegt oder gelöscht. Dadurch kann ein einzelnes Flag festgelegt oder gelöscht werden, ohne die aktuellen flagzustände zu lesen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der Zustand der Flags zum Bearbeiten des Stils, nachdem das Rich Edit-Steuerelement versucht hat, ihre Bearbeitungs Stiländerungen zu implementieren. Die formatierungsflags zum Bearbeiten sind ein Satz von Flags, die den aktuellen Bearbeitungs Stil angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | Rich Edit 3,0<br/>                                                              |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ GetEditStyle**](em-geteditstyle.md)
</dt> </dl>

 

 





