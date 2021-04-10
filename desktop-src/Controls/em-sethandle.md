---
title: EM_SETHANDLE Meldung (Winuser. h)
description: Legt das Handle des Arbeitsspeichers fest, der von einem mehrzeiligen Bearbeitungs Steuerelement verwendet wird.
ms.assetid: 0eae9365-62af-4040-8a51-273997a00b81
keywords:
- Windows-Steuerelemente für EM_SETHANDLE Meldung
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
ms.openlocfilehash: ac8f918d056db1000c6018f55d89095a73a15109
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105573"
---
# <a name="em_sethandle-message"></a>EM- \_ Nachricht

Legt das Handle des Arbeitsspeichers fest, der von einem mehrzeiligen Bearbeitungs Steuerelement verwendet wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für den Arbeitsspeicher Puffer, den das Bearbeitungs Steuerelement verwendet, um den aktuell angezeigten Text zu speichern, anstatt seinen eigenen Arbeitsspeicher zuzuordnen. Falls erforderlich, ordnet das-Steuerelement diesen Arbeitsspeicher neu zu.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Bevor eine Anwendung ein neues Speicher handle festlegt, sollte Sie eine [**EM \_ GetHandle**](em-gethandle.md) -Nachricht senden, um das Handle des aktuellen Speicherpuffers abzurufen, und diesen Arbeitsspeicher freigeben.

Ein Bearbeitungs Steuerelement ordnet den angegebenen Puffer automatisch neu zu, wenn ein zusätzlicher Platz für Text benötigt wird, oder er entfernt ausreichend Text, sodass zusätzlicher Speicherplatz nicht mehr benötigt wird.

Beim Senden einer **EM- \_ SetHandle** -Nachricht wird der Rückgängig-Puffer gelöscht ([**EM \_ CanUndo**](em-canundo.md) gibt NULL zurück), und das Flag für die interne Änderung ([**EM \_ getmodify**](em-getmodify.md) gibt NULL zurück). Das Bearbeitungs Steuerelement-Fenster wird neu gezeichnet.

Umfassende **Bearbeitung:** Die **EM \_** -Abmeldung wird nicht unterstützt. Rich Edit-Steuerelemente speichern Text nicht als einfaches Zeichen Array.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**EM \_ CanUndo**](em-canundo.md)
</dt> <dt>

[**EM \_ GetHandle**](em-gethandle.md)
</dt> <dt>

[**EM \_ getmodify**](em-getmodify.md)
</dt> </dl>

 

 





