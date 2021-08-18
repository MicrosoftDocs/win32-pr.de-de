---
title: WM_ADSPROP_SHEET_CREATE Meldung
description: Wird an das Benachrichtigungsobjekt gesendet, um ein sekundäres Eigenschaftenblatt in einem Active Directory-MMC-Snap-In zu erstellen.
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
ms.openlocfilehash: e0ec88eaed682fd16fecb717b851b902d5ba52ce08d5360aa78b881a4b8cb4f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024198"
---
# <a name="wm_adsprop_sheet_create-message"></a>WM \_ ADSPROP \_ SHEET \_ CREATE-Nachricht

Die **WM \_ ADSPROP SHEET \_ \_ CREATE-Nachricht** wird an das Benachrichtigungsobjekt gesendet, um ein sekundäres Eigenschaftenblatt in einem Active Directory-MMC-Snap-In zu erstellen.

> [!Note]  
> Dieser Meldungswert ist in einer veröffentlichten Headerdatei nicht definiert. Um diesen Meldungswert zu verwenden, müssen Sie ihn selbst im genauen angezeigten Format definieren.

 


```C++
#define WM_ADSPROP_SHEET_CREATE (WM_USER + 1108)
LRESULT SendMessage( (HWND)   hwnd, 
                     (UINT)   WM_ADSPROP_SHEET_CREATE,
                     (WPARAM) wParam, 
                     (LPARAM) lParam);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Hwnd* 
</dt> <dd>

Das Handle des Benachrichtigungsobjekts. Rufen Sie [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)auf, um dieses Handle abzurufen.

</dd> <dt>

*wParam* 
</dt> <dd>

Enthält einen Zeiger auf eine [**DSA \_ SEC PAGE \_ \_ INFO-Struktur,**](dsa-sec-page-info.md) die die zu erstellende sekundäre Seite definiert. Mit der **WM \_ ADSPROP \_ SHEET \_ CREATE-Meldung** kann nur ein sekundäres Eigenschaftenblatt erstellt werden, sodass die [**DSOBJECTNAMES-Struktur**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) nur eine [**DSOBJECT-Struktur**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) enthalten kann.

</dd> <dt>

*lParam* 
</dt> <dd>

Wird nicht verwendet. Muss **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Nachricht ist immer 0 (null).

## <a name="remarks"></a>Hinweise

Der Aufrufer muss die [**DSA \_ SEC PAGE \_ \_ INFO-Struktur,**](dsa-sec-page-info.md) die Titelzeichenfolge und alle [**DSOBJECT-Zeichenfolgen**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) mithilfe eines einzelnen Aufrufs der [**LocalAlloc-Funktion**](/windows/desktop/api/winbase/nf-winbase-localalloc) zuordnen. Die **WM \_ ADSPROP SHEET \_ \_ CREATE-Nachricht** ist eine asynchrone Nachricht, daher wird sie zurückgegeben, bevor das sekundäre Blatt erstellt wird. Aus diesem Grund muss der Arbeitsspeicher intakt bleiben, nachdem die Nachricht zurückgegeben wurde. Der Empfänger gibt diesen Arbeitsspeicher mit einem einzigen Aufruf der [**LocalFree-Funktion**](/windows/desktop/api/winbase/nf-winbase-localfree) frei, nachdem das sekundäre Blatt erstellt wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CFSTR \_ DS \_ PARENTHWND**](cfstr-ds-parenthwnd.md)
</dt> <dt>

[**DSA \_ SEC \_ PAGE \_ INFO**](dsa-sec-page-info.md)
</dt> <dt>

[**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> <dt>

[**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc)
</dt> <dt>

[**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 

