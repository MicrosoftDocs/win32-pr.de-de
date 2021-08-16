---
title: EM_SETHANDLE Meldung (Winuser.h)
description: Legt das Handle des Arbeitsspeichers fest, der von einem mehrzeiligen Bearbeitungssteuerelement verwendet wird.
ms.assetid: 0eae9365-62af-4040-8a51-273997a00b81
keywords:
- EM_SETHANDLE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_SETHANDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3ece3eb9c385b5f4d468a7dd2f08ff3335a4314b4c90569cdba453c4815728f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412591"
---
# <a name="em_sethandle-message"></a>EM \_ SETHANDLE-Meldung

Legt das Handle des Arbeitsspeichers fest, der von einem mehrzeiligen Bearbeitungssteuerelement verwendet wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für den Speicherpuffer, den das Bearbeitungssteuerelement verwendet, um den aktuell angezeigten Text zu speichern, anstatt seinen eigenen Arbeitsspeicher zuzuweisen. Bei Bedarf weist das Steuerelement diesen Speicher neu zu.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Bevor eine Anwendung ein neues Speicherhandle festlegt, sollte sie eine [**\_ EM-GETHANDLE-Nachricht**](em-gethandle.md) senden, um das Handle des aktuellen Speicherpuffers abzurufen, und diesen Arbeitsspeicher freigeben.

Ein Bearbeitungssteuerelement weist den angegebenen Puffer automatisch neu zu, wenn es zusätzlichen Platz für Text benötigt, oder entfernt genügend Text, sodass kein zusätzlicher Speicherplatz mehr benötigt wird.

Beim Senden einer **EM \_ SETHANDLE-Nachricht** werden der Rückgängigpuffer [**(EM \_ CANUNDO**](em-canundo.md) gibt 0 zurück) und das interne Änderungsflag [**(EM \_ GETMODIFY**](em-getmodify.md) gibt 0 zurück). Das Bearbeitungssteuerelementfenster wird neu gezeichnet.

**Rich Edit:** Die **EM \_ SETHANDLE-Nachricht** wird nicht unterstützt. Rich-Edit-Steuerelemente speichern Text nicht als einfaches Array von Zeichen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**EM \_ CANUNDO**](em-canundo.md)
</dt> <dt>

[**EM \_ GETHANDLE**](em-gethandle.md)
</dt> <dt>

[**EM \_ GETMODIFY**](em-getmodify.md)
</dt> </dl>

 

 





