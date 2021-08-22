---
title: LVM_GETSUBITEMRECT (Commctrl.h)
description: Ruft Informationen über das umgebundene Rechteck für ein Unterem in einem Listenansicht-Steuerelement ab.
ms.assetid: 985876b2-6eb3-4c96-88ea-ddec67ef5b5a
keywords:
- LVM_GETSUBITEMRECT von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- LVM_GETSUBITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 651be72c23113940fc30adb2e7a9de581289a8f4ddf580f27d01e2edf337c053
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119293890"
---
# <a name="lvm_getsubitemrect-message"></a>LVM \_ GETSUBITEMRECT-Nachricht

Ruft Informationen über das umgebundene Rechteck für ein Unterem in einem Listenansicht-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des [**\_ ListView-Makros GetSubItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getsubitemrect) senden (empfohlen). Diese Meldung ist nur für die Verwendung mit Listenansichtssteuerelementen vorgesehen, die den [**LVS \_ REPORT-Stil**](list-view-window-styles.md) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Index des übergeordneten Elements des Unterelements.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) die die Informationen des untergeordneten begrenzungsgebundenen Rechtecks erhält. Die Member müssen gemäß den folgenden Member-Wert-Beziehungen initialisiert werden:



| Wert                                                                                                                             | Bedeutung                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <dt>**Nach oben**</dt> </dl>    | Der 1-basierte Index des Unteremems.<br/>                                                                                    |
| <span id="left"></span><span id="LEFT"></span><dl> <dt>**Links**</dt> </dl> | Flagwert (siehe Hinweise). Gibt den Teil des Listenansichtsunteritems an, für den das umgebundene Rechteck abgerufen werden soll.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) oder andernfalls 0 (null) zurück.

## <a name="remarks"></a>Hinweise

Im Folgenden finden Sie die Flagwerte, die festgelegt werden können.



| Anforderung | Wert |
|----------------|---------------------------------------------------------------------------------------------------------------------|
| **Flagwert** | **Bedeutung**                                                                                                         |
| \_LVIR-GRENZEN   | Gibt das umgebundene Rechteck des gesamten Elements zurück, einschließlich des Symbols und der Bezeichnung.                                    |
| \_LVIR-SYMBOL     | Gibt das umgebundene Rechteck des Symbols oder kleinen Symbols zurück.                                                           |
| \_LVIR-BEZEICHNUNG    | Gibt das umgebundene Rechteck des gesamten Elements zurück, einschließlich des Symbols und der Bezeichnung. Dies ist identisch mit LVIR \_ BOUNDS. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

