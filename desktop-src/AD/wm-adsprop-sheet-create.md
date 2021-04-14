---
title: WM_ADSPROP_SHEET_CREATE Meldung
description: Wird an das Benachrichtigungs Objekt gesendet, um ein sekundäres Eigenschaften Blatt in einem Active Directory MMC-Snap-in zu erstellen.
ms.assetid: 3efa25f2-cd39-44f8-952e-203f1519ce2c
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_SHEET_CREATE Meldung Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_SHEET_CREATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b540ffd87d4350a323577ff5fa317e94f9271f2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517837"
---
# <a name="wm_adsprop_sheet_create-message"></a>Meldung zum Erstellen eines "WM \_ adsprop"- \_ Blatts \_

Die Meldung " **WM \_ adsprop \_ Sheet \_ Create** " wird an das Benachrichtigungs Objekt gesendet, um ein sekundäres Eigenschaften Blatt in einem Active Directory MMC-Snap-in zu erstellen.

> [!Note]  
> Dieser Nachrichtenwert ist nicht in einer veröffentlichten Header Datei definiert. Wenn Sie diesen Nachrichtenwert verwenden möchten, müssen Sie ihn im exakten Format definieren.

 


```C++
#define WM_ADSPROP_SHEET_CREATE (WM_USER + 1108)
LRESULT SendMessage( (HWND)   hwnd, 
                     (UINT)   WM_ADSPROP_SHEET_CREATE,
                     (WPARAM) wParam, 
                     (LPARAM) lParam);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HWND* 
</dt> <dd>

Das Handle des Benachrichtigungs Objekts. Rufen Sie zum Abrufen dieses Handles [**adspropkreatenotifyobj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)auf.

</dd> <dt>

*wParam* 
</dt> <dd>

Enthält einen Zeiger auf eine [**DSA \_ sec- \_ Seiten \_ Informations**](dsa-sec-page-info.md) Struktur, die die zu Erstell führende sekundäre Seite definiert. Es kann nur ein sekundäres Eigenschaften Blatt mit der Meldung " **WM \_ adsprop \_ Sheet \_ Create** " erstellt werden, sodass die [**dsobjectnames**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) -Struktur nur eine [**dsobject**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) -Struktur enthalten kann.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet. Muss **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Nachricht ist immer 0 (null).

## <a name="remarks"></a>Bemerkungen

Der Aufrufer muss die [**DSA \_ sec- \_ Seiten \_ Informations**](dsa-sec-page-info.md) Struktur, die Titel Zeichenfolge und alle [**dsobject**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) -Zeichen folgen mit einem einzigen Aufruf der [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc) -Funktion zuordnen. Die Meldung " **WM \_ adsprop \_ Sheet \_ Create** " ist eine asynchrone Nachricht und wird daher vor der Erstellung des sekundären Blatts zurückgegeben. Aus diesem Grund muss der Arbeitsspeicher beibehalten werden, nachdem die Nachricht zurückgegeben wurde. Der Empfänger gibt diesen Arbeitsspeicher mit einem einzigen-Befehl der [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) -Funktion frei, nachdem das sekundäre Blatt erstellt wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**cfstr \_ DS- \_ Klammern**](cfstr-ds-parenthwnd.md)
</dt> <dt>

[**\_ \_ Seite \_ Informationen zu DSA sec**](dsa-sec-page-info.md)
</dt> <dt>

[**Dsobjectnames**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[**Dsobject**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> <dt>

[**Localzuweisung**](/windows/desktop/api/winbase/nf-winbase-localalloc)
</dt> <dt>

[**Von LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 

