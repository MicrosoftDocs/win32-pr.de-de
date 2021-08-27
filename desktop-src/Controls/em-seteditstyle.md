---
title: EM_SETEDITSTYLE-Nachricht (Richedit.h)
description: Legt die aktuellen Bearbeitungsformatflags für ein Rich Edit-Steuerelement fest.
ms.assetid: e48de6b3-0fd2-4791-9863-a6dcdafa3642
keywords:
- EM_SETEDITSTYLE Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 06789b1d1fedfc76af205ac46aac7d3ea4bb882f2460676df96cd018d5a216b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048590"
---
# <a name="em_seteditstyle-message"></a>EM \_ SETEDITSTYLE-Meldung

Legt die aktuellen Bearbeitungsformatflags für ein Rich Edit-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt ein oder mehrere Bearbeitungsformatflags an. Eine Liste der möglichen Werte finden Sie unter [**EM \_ GETEDITSTYLE**](em-geteditstyle.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Eine Maske, die aus einem oder mehreren *wParam-Werten* besteht. Nur die in dieser Maske angegebenen Werte werden festgelegt oder gelöscht. Dadurch kann ein einzelnes Flag festgelegt oder gelöscht werden, ohne die aktuellen Flagzustände zu lesen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der Status der Bearbeitungsformatflags, nachdem das Rich Edit-Steuerelement versucht hat, Ihre Änderungen am Bearbeitungsstil zu implementieren. Die Bearbeitungsformatflags sind eine Gruppe von Flags, die den aktuellen Bearbeitungsstil angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | Rich Edit 3.0<br/>                                                              |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ GETEDITSTYLE**](em-geteditstyle.md)
</dt> </dl>

 

 





