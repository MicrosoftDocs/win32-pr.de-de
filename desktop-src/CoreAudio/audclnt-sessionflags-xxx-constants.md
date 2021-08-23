---
description: Die AUDCLNT \_ SESSIONFLAGS XXX-Konstanten geben Merkmale einer Audiositzung an, \_ die dem Stream zugeordnet ist.
ms.assetid: 5745d5bc-71e8-4b33-8227-c1c84226b6ee
title: AUDCLNT_SESSIONFLAGS_XXX Konstanten (Audiosessiontypes.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15423d24d48a98b69c4ab1651941fba639885c03e27cf9df8b1834aab830bb6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018498"
---
# <a name="audclnt_sessionflags_xxx-constants"></a>AUDCLNT \_ SESSIONFLAGS \_ XXX-Konstanten

Die AUDCLNT \_ SESSIONFLAGS XXX-Konstanten geben Merkmale einer Audiositzung an, \_ die dem Stream zugeordnet ist. Ein Client kann diese Optionen während der Initialisierung des Streams über den *StreamFlags-Parameter* der [**IAudioClient::Initialize-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) angeben.



| Konstante/Wert                                                                                                                                                                                                                                                                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AUDCLNT_SESSIONFLAGS_EXPIREWHENUNOWNED"></span><span id="audclnt_sessionflags_expirewhenunowned"></span><dl> <dt>**AUDCLNT \_ SESSIONFLAGS \_ EXPIREWHENUNOWNED**</dt> <dt>0x10000000</dt> </dl>                       | Die Sitzung läuft ab, wenn keine zugeordneten Streams und besitzenden Sitzungssteuerungsobjekte mit Verweisen enthalten sind.<br/>                                                                                                                                                                                       |
| <span id="AUDCLNT_SESSIONFLAGS_DISPLAY_HIDE"></span><span id="audclnt_sessionflags_display_hide"></span><dl> <dt>**AUDCLNT \_ SESSIONFLAGS \_ DISPLAY \_ HIDE**</dt> <dt>0X20000000</dt> </dl>                                     | Das Volumesteuergerät wird auf der Benutzeroberfläche des Volumemixers ausgeblendet, wenn die Audiositzung erstellt wird. Wenn die dem Stream zugeordnete Sitzung bereits vorhanden ist, bevor [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) den Stream öffnet, wird das Volumesteuerobjekt im Volumemixer angezeigt.<br/> |
| <span id="_AUDCLNT_SESSIONFLAGS_DISPLAY_HIDEWHENEXPIRED"></span><span id="_audclnt_sessionflags_display_hidewhenexpired"></span><dl> <dt> **AUDCLNT \_ SESSIONFLAGS \_ DISPLAY \_ HIDEWHENEXPIRED**</dt> <dt>0x40000000</dt> </dl> | Das Volumesteuergerät wird auf der Benutzeroberfläche des Volumemixers ausgeblendet, nachdem die Sitzung abgelaufen ist. <br/>                                                                                                                                                                                                           |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Audiosessiontypes.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kernaudiokonstten](core-audio-constants.md)
</dt> <dt>

[**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
</dt> </dl>

 

 




