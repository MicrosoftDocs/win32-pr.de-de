---
title: MM_ACM_FORMATCHOOSE (Msacm.h)
description: Die Meldung MM ACM FORMATCHOOSE benachrichtigt eine \_ acmFormatChoose-Dialoghookfunktion, bevor einem der drei \_ Dropdownlistenfelder ein Element hinzugefügt wird.
ms.assetid: f77e41c6-14e9-45c0-971e-4d6325145f1c
keywords:
- MM_ACM_FORMATCHOOSE von Windows Multimedia
topic_type:
- apiref
api_name:
- MM_ACM_FORMATCHOOSE
api_location:
- Msacm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cceaa67bc0ce4ee922b48d1cff20eb2bf6414f93506dcc70ccd6e0e912211544
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119782960"
---
# <a name="mm_acm_formatchoose-message"></a>MM \_ ACM \_ FORMATCHOOSE-Meldung

Die **Meldung MM \_ ACM \_ FORMATCHOOSE** benachrichtigt eine [**acmFormatChoose-Dialoghookfunktion,**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) bevor einem der drei Dropdownlistenfelder ein Element hinzugefügt wird. Diese Meldung ermöglicht einer Anwendung, die über die Benutzeroberfläche verfügbare Auswahl weiter anzupassen.


```C++
MM_ACM_FORMATCHOOSE 
wParam = (WPARAM) wDropDown 
lParam = (LONG) lCustom 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*
</dt> <dd>

Das dropdown-Listenfeld, das initialisiert wird, und ein Überprüfungs- oder Add-Vorgang.



| Anforderung | Wert |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FORMATCHOOSE \_ CUSTOM \_ VERIFY    | Der *lParam-Parameter* ist ein Zeiger auf eine [**WAVEFORMATEX-Struktur,**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) die dem benutzerdefinierten Dropdownlistenfeld Name hinzugefügt werden soll.                                                                                                   |
| FORMATCHOOSE \_ FORMAT \_ HINZUFÜGEN       | Der *lParam-Parameter* ist ein Zeiger auf einen Puffer, der eine [**WAVEFORMATEX-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) akzeptiert, die dem Dropdown-Listenfeld Format hinzugefügt werden soll. Die Anwendung muss die Formatstruktur kopieren, die diesem Puffer hinzugefügt werden soll. |
| FORMATCHOOSE \_ FORMAT \_ VERIFY    | Der *lParam-Parameter* ist ein Zeiger auf eine [**WAVEFORMATEX-Struktur,**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) die dem Dropdownlistenfeld Format hinzugefügt werden soll.                                                                                                        |
| FORMATCHOOSE \_ FORMATTAG \_ ADD    | Der *lParam-Parameter* ist ein Zeiger auf eine Variable, die ein Waveform-Audio-Formattag akzeptiert, das dem Dropdownlistenfeld Formattag hinzugefügt werden soll.                                                                                             |
| FORMATCHOOSE \_ FORMATTAG \_ VERIFY | Der *lParam-Parameter* ist ein Waveform-Audio-Formattag, das im Dropdown-Listenfeld Formattag aufgeführt werden soll.                                                                                                                                     |



 

</dd> <dt>

<span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*
</dt> <dd>

Der Wert, der durch das im **wParam-Parameter angegebene Listenfeld definiert** wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn eine Anwendung diese Meldung verarbeitet, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Wenn die Anwendung den VORGANG FILTERCHOOSE FORMAT ADD verarbeitet, wird die Größe des in lParam bereitgestellten Speicherpuffers von der \_ \_ [**acmMetrics-Funktion**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) bestimmt. 

Wenn Ihre Anwendung einen Überprüfungsvorgang verarbeitet, kann sie verhindern, dass das Dialogfeld diese Auswahl auflistet, indem die **SetWindowLong-Funktion** aufgerufen wird, bei der *nIndex* auf DWL \_ MSGRESULT und *lNewLong* auf **FALSE** festgelegt ist (in einen **LONG-Datentyp** cast). Damit das Dialogfeld diese Auswahl auflisten kann, rufen Sie diese Funktion auf, und *legen Sie lNewLong* auf **TRUE fest.**

Wenn Ihre Anwendung einen Add-Vorgang verarbeitet, kann dies darauf hindeuten, dass keine weiteren Ergänzungen erforderlich sind, indem die **SetWindowLong-Funktion** aufgerufen wird, bei der *nIndex* auf DWL \_ MSGRESULT und *lNewLong* auf **FALSE** festgelegt ist (in einen **LONG-Datentyp** cast). Um anzugeben, dass weitere Ergänzungen erforderlich sind, rufen Sie diese Funktion auf, bei der *lNewLong* auf **TRUE festgelegt ist.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Msacm.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Audiokomprimierungs-Manager](audio-compression-manager.md)
</dt> <dt>

[Audiokomprimierungsmeldungen](audio-compression-messages.md)
</dt> </dl>

 

