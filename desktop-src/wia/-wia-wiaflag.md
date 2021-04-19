---
description: 'Flags, die von den Methoden iwiadevmgr:: getimagedlg, IWiaDevMgr2:: getimagedlg, iwiaitem::D evicedlg und IWiaItem2::D evicedlg zum Steuern des Dialogfeld Vorgangs verwendet werden.'
ms.assetid: 468a3c9e-64f8-456d-aad9-fa7c6876fbe6
title: Wiaflag (wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DEVICE_DIALOG_SINGLE_IMAGE
- WIA_DEVICE_DIALOG_USE_COMMON_UI
- WIA_SELECT_DEVICE_NODEFAULT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: c906f22e168ca29aadd2e9450fac6225c8b91c17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348410"
---
# <a name="wiaflag"></a>Wiaflag

Flags, die von den Methoden [**iwiadevmgr:: getimagedlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg), [**IWiaDevMgr2:: getimagedlg**](-wia-iwiadevmgr2-getimagedlg.md), [**iwiaitem::D evicedlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg)und [**IWiaItem2::D evicedlg**](-wia-iwiaitem2-devicedlg.md) zum Steuern des Dialogfeld Vorgangs verwendet werden.



| Konstante                                                                                                                                                                                                                | BESCHREIBUNG                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_DEVICE_DIALOG_SINGLE_IMAGE"></span><span id="wia_device_dialog_single_image"></span><dl> <dt>**WIA- \_ Geräte \_ Dialogfeld, \_ einzelnes \_ Bild**</dt> </dl>     | Beschränken Sie die Bildauswahl auf ein einzelnes Bild im Dialogfeld Geräte Abbild Erfassung.<br/>                                                                                                           |
| <span id="WIA_DEVICE_DIALOG_USE_COMMON_UI"></span><span id="wia_device_dialog_use_common_ui"></span><dl> <dt>**Dialog Feld "WIA- \_ Gerät" \_ \_ verwenden \_ allgemeine \_ Benutzeroberfläche**</dt> </dl> | Verwenden Sie die Benutzeroberfläche des Systems, falls verfügbar, anstelle der vom Hersteller bereitgestellten Benutzeroberfläche. Wenn die Benutzeroberfläche des Systems nicht verfügbar ist, wird die Benutzeroberfläche des Anbieters verwendet. Wenn keine Benutzeroberfläche verfügbar ist, gibt die Funktion E \_ notimpl zurück.<br/>      |
| <span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span><dl> <dt>**WIA \_ Select \_ Device \_ NODEFAULT**</dt> </dl>               | Erzwingen Sie die [**iwiadevmgr:: getimagedlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg) -oder [**IWiaDevMgr2:: getimagedlg**](-wia-iwiadevmgr2-getimagedlg.md) -Methode, um das Dialogfeld **Gerät auswählen** anzuzeigen.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




