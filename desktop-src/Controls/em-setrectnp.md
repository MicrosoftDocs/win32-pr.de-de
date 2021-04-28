---
title: EM_SETRECTNP (Winuser.h)
description: 'EM_SETRECTNP Meldung: Legt das Formatierungsrechteck eines mehrzweckigen Bearbeitungssteuer steuerelements fest.'
ms.assetid: 1ab497ca-023f-4c26-b92d-b441a0d7b90c
keywords:
- EM_SETRECTNP Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- EM_SETRECTNP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9a8c85d4f7abd58ed3adb33ede66254c190a7bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085988"
---
# <a name="em_setrectnp-message"></a>EM \_ SETRECTNP-Nachricht

Legt das [Formatierungsrechteck eines](about-edit-controls.md) mehrzweckigen Bearbeitungssteuer steuerelements fest. Die **EM \_ SETRECTNP-Nachricht** ist mit der [**EM \_ SETRECT-Nachricht**](em-setrect.md) identisch, außer dass **EM \_ SETRECTNP** das Bearbeitungssteuersteuerfenster nicht neu gezeichnet hat. 

Das Formatierungrechteck ist das einschränkende Rechteck, in das das Steuerelement den Text zeichnet. Das einschränkende Rechteck ist unabhängig von der Größe des Bearbeitungssteuerfensters.

Diese Meldung wird nur von mehrline-Bearbeitungssteuerelementen verarbeitet. Sie können diese Nachricht entweder an ein Bearbeitungssteuer steuerelement oder an ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

**Rich Edit 3.0 und höher:** Gibt an, ob das neue Rechteck absolute oder relative Koordinaten enthält. Der Wert 0 (null) gibt absolute Koordinaten an. Der Wert 1 gibt Offsets relativ zum aktuellen Formatierungsrechteck an. (Die Offsets können positiv oder negativ sein.)

**Steuerelemente bearbeiten:** Dieser Parameter wird nicht verwendet und muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) die die neuen Dimensionen des Rechtecks angibt. Wenn dieser Parameter **NULL ist,** wird das Formatierungsrechteck auf seine Standardwerte festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

**Umfangreiche Bearbeitung:** Wird in Microsoft Rich Edit 3.0 und höher unterstützt. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (windows.h einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Verweis**
</dt> <dt>

[**EM \_ SETRECT**](em-setrect.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Rect**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

