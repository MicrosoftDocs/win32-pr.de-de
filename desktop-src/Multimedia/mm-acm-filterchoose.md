---
title: MM_ACM_FILTERCHOOSE Meldung (MSACM. h)
description: Die mm \_ ACM \_ filterchoose-Meldung benachrichtigt eine acmfilterchoose-Dialogfeld-Hookfunktion, bevor ein Element zu einem der drei Dropdown-Listenfelder hinzugefügt wird.
ms.assetid: f3c68240-a9aa-4771-96b9-1cb3bb5ea906
keywords:
- MM_ACM_FILTERCHOOSE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_ACM_FILTERCHOOSE
api_location:
- Msacm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1df28ad7f950b8ce995fd308622db8c429393cb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103038"
---
# <a name="mm_acm_filterchoose-message"></a>MM \_ ACM \_ filterchoose-Meldung

Die **mm \_ ACM \_ filterchoose** -Meldung benachrichtigt eine [**acmfilterchoose**](/windows/desktop/api/Msacm/nf-msacm-acmfilterchoose) -Dialogfeld-Hookfunktion, bevor ein Element zu einem der drei Dropdown-Listenfelder hinzugefügt wird. Diese Meldung ermöglicht es einer Anwendung, die auf der Benutzeroberfläche verfügbare Auswahl weiter anzupassen.


```C++
        MM_ACM_FILTERCHOOSE
        wParam = (WPARAM) wDropDown
        lParam = (LONG) lCustom
      
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wdropdown*
</dt> <dd>

Dropdown-Listenfeld, das initialisiert wird, und ein Vorgang zum Überprüfen oder hinzufügen.



| Anforderung | Wert |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filter Choose \_ Custom \_ Verify    | Der *LPARAM* -Parameter ist ein Zeiger auf eine [**Wellen Filter**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) Struktur, die dem Dropdown-Listenfeld benutzerdefinierter Name hinzugefügt wird.                                                                                                   |
| \_Filter Auswahl Filter \_ Hinzufügen       | Der *LPARAM* -Parameter ist ein Zeiger auf einen Puffer, der eine [**Wellen Filter**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) -Struktur akzeptiert, die dem Dropdown-Listenfeld Filter hinzugefügt wird. Die Anwendung muss die Filter Struktur kopieren, die in diesen Puffer eingefügt werden soll. |
| \_Filter Auswahl Filter \_ überprüfen    | Der *LPARAM* -Parameter ist ein Zeiger auf eine [**Wellen Filter**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) Struktur, die dem Dropdown-Listenfeld Filter hinzugefügt wird.                                                                                                        |
| filterchoose \_ Filtertag \_ Hinzufügen    | Der *LPARAM* -Parameter ist ein Zeiger auf ein **DWORD** , das ein Waveform-audiofiltertag akzeptiert, das dem Dropdown-Listenfeld für den Filtertag hinzugefügt wird.                                                                                        |
| filterchoose \_ Filtertag \_ verify überprüfen | Der *LPARAM* -Parameter ist ein Waveform-audiofiltertag, das im Dropdown-Listenfeld für den Filtertag aufgeführt wird.                                                                                                                                 |



 

</dd> <dt>

<span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lcustom*
</dt> <dd>

Der Wert, der durch das im **wParam** -Parameter angegebene Listenfeld definiert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt " **true** " zurück, wenn eine Anwendung diese Nachricht behandelt, andernfalls " **false** ".

## <a name="remarks"></a>Bemerkungen

Wenn die Anwendung den filterchoose- \_ Filter \_ Add-Vorgang verarbeitet, wird die Größe des in *LPARAM* angegebenen Speicherpuffers aus der [**acmmetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) -Funktion bestimmt.

Wenn die Anwendung einen Verifizierungs Vorgang verarbeitet, die Anwendung muss dem Rückgabewert mit **SetWindowLong** (HWND, DWL \_ msgresult, (Long) **false**) vorangestellt sein, um zu verhindern, dass das Dialogfeld diese Auswahl auflistet, oder mit **SetWindowLong** (HWND, DWL \_ msgresult, (Long)**true**), damit das Dialogfeld diese Auswahl auflisten kann. Wenn Sie einen Add-Vorgang verarbeiten, muss die Anwendung vor der Rückgabe mit **SetWindowLong** (HWND, DWL \_ msgresult, (Long)**false**) stehen, um anzugeben, dass keine weiteren Ergänzungen erforderlich sind, oder mit **SetWindowLong** (HWND, DWL \_ msgresult, (Long)**true**), wenn weitere Ergänzungen erforderlich sind.

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

 

 





