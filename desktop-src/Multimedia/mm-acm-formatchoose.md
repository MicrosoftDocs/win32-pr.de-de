---
title: MM_ACM_FORMATCHOOSE Meldung (MSACM. h)
description: Die mm \_ ACM \_ formatchoose-Meldung benachrichtigt eine acmformatchoose-Dialog Hook-Funktion, bevor ein Element zu einem der drei Dropdown-Listenfelder hinzugefügt wird.
ms.assetid: f77e41c6-14e9-45c0-971e-4d6325145f1c
keywords:
- MM_ACM_FORMATCHOOSE-Nachricht (Multimedia)
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
ms.openlocfilehash: 35808e06521cbd83d07f8d6c799779a16f50236b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743921"
---
# <a name="mm_acm_formatchoose-message"></a>MM- \_ ACM \_ formatchoose-Meldung

Die **mm \_ ACM \_ formatchoose** -Meldung benachrichtigt eine [**acmformatchoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) -Dialog Hook-Funktion, bevor ein Element zu einem der drei Dropdown-Listenfelder hinzugefügt wird. Diese Meldung ermöglicht es einer Anwendung, die auf der Benutzeroberfläche verfügbare Auswahl weiter anzupassen.


```C++
MM_ACM_FORMATCHOOSE 
wParam = (WPARAM) wDropDown 
lParam = (LONG) lCustom 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wdropdown*
</dt> <dd>

Dropdown-Listenfeld, das initialisiert wird, und ein Vorgang zum Überprüfen oder hinzufügen.



| Anforderung | Wert |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| formatchoose \_ Custom \_ Verify    | Der *LPARAM* -Parameter ist ein Zeiger auf eine [**WaveFormatEx**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) -Struktur, die dem Dropdown-Listenfeld benutzerdefinierter Name hinzugefügt wird.                                                                                                   |
| formatchoose- \_ Format \_ Hinzufügen       | Der *LPARAM* -Parameter ist ein Zeiger auf einen Puffer, der dem Dropdown-Listenfeld Format eine [**WaveFormatEx**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) -Struktur zuweist. Die Anwendung muss die Format Struktur kopieren, die in diesen Puffer eingefügt werden soll. |
| formatchoose- \_ Format \_ überprüfen    | Der *LPARAM* -Parameter ist ein Zeiger auf eine [**WaveFormatEx**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) -Struktur, die dem Dropdown-Listenfeld Format hinzugefügt wird.                                                                                                        |
| Formattag \_ Formattag \_ Hinzufügen    | Der *LPARAM* -Parameter ist ein Zeiger auf eine Variable, die ein Waveform-audioformattag akzeptiert, das dem Dropdown-Listenfeld Formattag hinzugefügt wird.                                                                                             |
| formatchoose \_ Formattag \_ Verify | Der *LPARAM* -Parameter ist ein Waveform-audioformattag, das im Dropdown-Listenfeld Formattag aufgeführt wird.                                                                                                                                     |



 

</dd> <dt>

<span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lcustom*
</dt> <dd>

Der Wert, der durch das im **wParam** -Parameter angegebene ListBox-Element definiert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt " **true** " zurück, wenn eine Anwendung diese Nachricht behandelt, andernfalls " **false** ".

## <a name="remarks"></a>Bemerkungen

Wenn die Anwendung den Vorgang zum Hinzufügen des filterchoose- \_ Formats verarbeitet \_ , wird die Größe des in *LPARAM* angegebenen Speicherpuffers aus der [**acmmetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) -Funktion bestimmt.

Wenn Ihre Anwendung einen Verifizierungs Vorgang verarbeitet, kann Sie verhindern, dass das Dialogfeld diese Auswahl auflistet, indem Sie die **SetWindowLong** -Funktion aufruft, wobei *nIndex* auf DWL \_ msgresult und *lnewlong* auf **false** festgelegt ist (in einen **Long** -Datentyp umgewandelt). Damit das Dialogfeld diese Auswahl auflisten kann, wird diese Funktion aufgerufen, wenn *lnewlong* auf **true** festgelegt ist.

Wenn Ihre Anwendung einen Add-Vorgang verarbeitet, kann Sie angeben, dass keine weiteren Ergänzungen erforderlich sind, indem Sie die **SetWindowLong** -Funktion aufrufen, wobei *nIndex* auf DWL \_ msgresult und *lnewlong* auf **false** festgelegt ist (in einen **Long** -Datentyp umgewandelt). Um anzugeben, dass weitere Ergänzungen erforderlich sind, können Sie diese Funktion mit " *lnewlong* " auf " **true**" setzen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>MSACM. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Audiokomprimierungs-Manager](audio-compression-manager.md)
</dt> <dt>

[Audiokomprimierungs Meldungen](audio-compression-messages.md)
</dt> </dl>

 

