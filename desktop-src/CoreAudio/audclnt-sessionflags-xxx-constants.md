---
description: Die Konstanten "audclnt \_ sessionflags \_ xxx" geben Merkmale einer Audiositzung an, die dem Stream zugeordnet ist.
ms.assetid: 5745d5bc-71e8-4b33-8227-c1c84226b6ee
title: AUDCLNT_SESSIONFLAGS_XXX Konstanten (audiosessiontypes. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e2152c33103ca3366399995b7d11bb072f2bdd2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483923"
---
# <a name="audclnt_sessionflags_xxx-constants"></a>Audclnt \_ sessionflags \_ xxx-Konstanten

Die Konstanten "audclnt \_ sessionflags \_ xxx" geben Merkmale einer Audiositzung an, die dem Stream zugeordnet ist. Diese Optionen können von einem Client während der Initialisierung des Datenstroms durch den *StreamFlags* -Parameter der [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) -Methode angegeben werden.



| Konstante/Wert                                                                                                                                                                                                                                                                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AUDCLNT_SESSIONFLAGS_EXPIREWHENUNOWNED"></span><span id="audclnt_sessionflags_expirewhenunowned"></span><dl> " <dt>**Audclnt \_ " Sessionflags \_ expireexpinicht im Besitz**</dt> von <dt>0x10000000</dt> </dl>                       | Die Sitzung läuft ab, wenn keine zugeordneten Streams vorhanden sind und die besitzenden Sitzungs Steuerungs Objekte Verweise enthalten.<br/>                                                                                                                                                                                       |
| <span id="AUDCLNT_SESSIONFLAGS_DISPLAY_HIDE"></span><span id="audclnt_sessionflags_display_hide"></span><dl> " <dt>**Audclnt \_ " Sessionflags- \_ Anzeige \_ Ausblenden**</dt> <dt>0x20000000</dt> </dl>                                     | Wenn die Audiositzung erstellt wird, wird das Volume-Steuerelement auf der volumemixer-Benutzeroberfläche ausgeblendet. Wenn die mit dem Stream verknüpfte Sitzung bereits vorhanden ist, bevor [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) den Stream öffnet, wird das volumesteuerelement im volumemixer angezeigt.<br/> |
| <span id="_AUDCLNT_SESSIONFLAGS_DISPLAY_HIDEWHENEXPIRED"></span><span id="_audclnt_sessionflags_display_hidewhenexpired"></span><dl> <dt> **Audclnt \_ sessionflags \_ Display \_ hideabgelaufabgelaufenes**</dt> <dt>0x40000000</dt> </dl> | Das volumesteuerelement ist in der volumemixer-Benutzeroberfläche ausgeblendet, nachdem die Sitzung abgelaufen ist. <br/>                                                                                                                                                                                                           |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Audiosessiontypes. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kernaudiokonstanten](core-audio-constants.md)
</dt> <dt>

[**Iaudiosessioncontrol**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
</dt> </dl>

 

 




