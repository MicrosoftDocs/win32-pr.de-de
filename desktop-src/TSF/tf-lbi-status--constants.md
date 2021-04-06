---
title: TF_LBI_STATUS_ Konstanten (ctfutb. h)
description: Die TF \_ LBI- \_ Status \_ \-Konstanten geben den Status eines sprach leisten Elements an. Diese Werte werden mit der itflangbaritem GetStatus-Methode verwendet.
ms.assetid: 5f2c0e61-f7e5-4dcc-86a3-7bd1c994b8bc
topic_type:
- apiref
api_name:
- TF_LBI_STATUS_HIDDEN
- TF_LBI_STATUS_DISABLED
- TF_LBI_STATUS_BTN_TOGGLED
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7de9dcf0272eaf79fd001461aa555d78c9d6ae30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742921"
---
# <a name="tf_lbi_status_-constants"></a>TF \_ LBI- \_ Status \_ \* Konstanten

Die "**tf \_ LBI \_ Status \_ \** _-Konstanten" geben den Status eines sprach leisten Elements an. Diese Werte werden mit der [itflangbaritem:: GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) -Methode verwendet.



| Konstante/Wert                                                                                                                                                                                                                                                       | BESCHREIBUNG                                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_STATUS_HIDDEN"></span><span id="tf_lbi_status_hidden"></span><dl> <dt>_ * TF \_ LBI- \_ Status \_ ausgeblendet * *</dt> <dt>0x00000001</dt> </dl>                 | Das Element ist ausgeblendet. Dieser Stil wird ignoriert, wenn das Element den Stil des TF- \_ LBI- \_ Stils " \_ hiddenstatus Control" nicht enthält.<br/>                  |
| <span id="TF_LBI_STATUS_DISABLED"></span><span id="tf_lbi_status_disabled"></span><dl> <dt>**Tf \_ LBI- \_ Status \_ deaktiviert**</dt> <dt>0x00000002</dt> </dl>           | Das Element ist deaktiviert.<br/>                                                                                                                  |
| <span id="TF_LBI_STATUS_BTN_TOGGLED"></span><span id="tf_lbi_status_btn_toggled"></span><dl> <dt>**Tf \_ LBI- \_ Status \_ \_ BTN**</dt> -ein-/ausgeschaltet <dt>0x00010000 bis</dt> </dl> | Das Element befindet sich im UMSCHALT-oder gedrückten Zustand. Dieser Stil wird ignoriert, wenn das Element den TF \_ LBI- \_ Stil \_ BTN- \_ UMSCHALT Stil nicht enthält.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | TSF 1,0 unter Windows 2000 Professional<br/>                                       |
| Header<br/>                   | <dl> <dt>Ctfutb. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Ctfutb. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Itflangbaritem:: GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus)
</dt> </dl>

 

 





