---
title: TF_MOD_ Konstanten (msctf. h)
description: Die TF \_ mod \_ \-Konstanten geben schlüsselmodifizierer in der TF \_ preservedkey-Struktur an.
ms.assetid: 4642ef17-34bd-4482-a9e9-0fbed7b574b1
topic_type:
- apiref
api_name:
- TF_MOD_ALT
- TF_MOD_CONTROL
- TF_MOD_SHIFT
- TF_MOD_RALT
- TF_MOD_RCONTROL
- TF_MOD_RSHIFT
- TF_MOD_LALT
- TF_MOD_LCONTROL
- TF_MOD_LSHIFT
- TF_MOD_ON_KEYUP
- TF_MOD_IGNORE_ALL_MODIFIER
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e67e081d9a0f8714410861c7c36f9f751bad8d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040569"
---
# <a name="tf_mod_-constants"></a>TF- \_ mod- \_ \* Konstanten

Die TF \_ mod- \_ \* Konstanten geben schlüsselmodifizierer in der [tf \_ preservedkey](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey) -Struktur an.



| Konstante/Wert                                                                                                                                                                                                                                                      | BESCHREIBUNG                                                                                                                                                                          |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_MOD_ALT"></span><span id="tf_mod_alt"></span><dl> <dt>**Tf \_ MOD \_ alt**</dt> <dt>0x0001</dt> </dl>                                                   | Jeder der Alt-Taste wird gedrückt.<br/>                                                                                                                                         |
| <span id="TF_MOD_CONTROL"></span><span id="tf_mod_control"></span><dl> <dt>**Tf \_ MOD- \_ Steuer**</dt> Element <dt>0x0002</dt> </dl>                                       | Eine der STRG-Taste wird gedrückt.<br/>                                                                                                                                        |
| <span id="TF_MOD_SHIFT"></span><span id="tf_mod_shift"></span><dl> <dt>**Tf \_ MOD \_ Shift**</dt> <dt>0x0004</dt> </dl>                                             | Beide Umschalt Tasten werden gedrückt.<br/>                                                                                                                                       |
| <span id="TF_MOD_RALT"></span><span id="tf_mod_ralt"></span><dl> <dt>**Tf \_ MOD \_ Ralt**</dt> <dt>0x0008</dt> </dl>                                                | Die Rechte ALT-Taste wird gedrückt.<br/>                                                                                                                                              |
| <span id="TF_MOD_RCONTROL"></span><span id="tf_mod_rcontrol"></span><dl> <dt>**Tf \_ MOD \_ rcontrol**</dt> <dt>0x0010</dt> </dl>                                    | Die Rechte STRG-Taste wird gedrückt.<br/>                                                                                                                                             |
| <span id="TF_MOD_RSHIFT"></span><span id="tf_mod_rshift"></span><dl> <dt>**Tf \_ MOD \_ rshift**</dt> <dt>0x0020</dt> </dl>                                          | Die Rechte UMSCHALTTASTE wird gedrückt.<br/>                                                                                                                                            |
| <span id="TF_MOD_LALT"></span><span id="tf_mod_lalt"></span><dl> <dt>**Tf \_ MOD \_ LAlt**</dt> <dt>0x0040</dt> </dl>                                                | Die linke ALT-Taste wird gedrückt.<br/>                                                                                                                                               |
| <span id="TF_MOD_LCONTROL"></span><span id="tf_mod_lcontrol"></span><dl> <dt>**Tf \_ MOD \_ lcontrol**</dt> <dt>0x0080</dt> </dl>                                    | Die linke STRG-Taste wird gedrückt.<br/>                                                                                                                                              |
| <span id="TF_MOD_LSHIFT"></span><span id="tf_mod_lshift"></span><dl> <dt>**Tf \_ MOD \_ LShift**</dt> <dt>0x0100</dt> </dl>                                          | Die Linke UMSCHALTTASTE wird gedrückt.<br/>                                                                                                                                             |
| <span id="TF_MOD_ON_KEYUP"></span><span id="tf_mod_on_keyup"></span><dl> <dt>**Tf \_ MOD \_ für \_ KeyUp**</dt> <dt>0x0200</dt> </dl>                                   | Das Ereignis wird ausgelöst, wenn der Schlüssel freigegeben wird. Ohne dieses Flag wird das-Ereignis ausgelöst, wenn die Taste gedrückt wird.<br/>                                                          |
| <span id="TF_MOD_IGNORE_ALL_MODIFIER"></span><span id="tf_mod_ignore_all_modifier"></span><dl> <dt>**Tf \_ MOD \_ \_ alle \_ Modifizierer**</dt> <dt>0x0400</dt> ignorieren </dl> | Der Zustand der Alt-Taste, der STRG-Taste und der UMSCHALTTASTE wird ignoriert. Dies bedeutet, dass das Ereignis beim Drücken der virtuellen Taste ausgelöst wird, unabhängig davon, welche Modifizierertasten gedrückt werden.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Verteilbare Komponente<br/>          | TSF 1,0 unter Windows 2000 Professional<br/>                                      |
| Header<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[TF \_ preservedkey](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey)
</dt> </dl>

 

 





