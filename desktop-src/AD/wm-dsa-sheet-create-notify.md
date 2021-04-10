---
title: WM_DSA_SHEET_CREATE_NOTIFY Meldung
description: Wird im Active Directory MMC-Snap-in zum Erstellen eines sekundären Eigenschaften Blatts gepostet.
ms.assetid: 878878bf-fb78-4669-b282-1dd3349f35d5
ms.tgt_platform: multiple
keywords:
- WM_DSA_SHEET_CREATE_NOTIFY Meldung Active Directory
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CREATE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77f08424e7b39449861ec654f1ff7891c6e9c60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956546"
---
# <a name="wm_dsa_sheet_create_notify-message"></a>WM- \_ DSA- \_ Blatt " \_ \_ Nachricht benachrichtigen" erstellen

Das **WM- \_ DSA- \_ Blatt \_ Create \_ Notify** Message wird im Active Directory MMC-Snap-in zum Erstellen eines sekundären Eigenschaften Blatts gepostet.

> [!Note]  
> Dieser Nachrichtenwert ist nicht in einer veröffentlichten Header Datei definiert. Um diesen Nachrichtenwert zu verwenden, definieren Sie ihn im exakten Format.

 


```C++
#define WM_DSA_SHEET_CREATE_NOTIFY (WM_USER + 6)
LRESULT SendMessage(
    (HWND) hwnd, 
    WM_DSA_SHEET_CREATE_NOTIFY,
    (WPARAM) wParam, 
    (LPARAM) lParam);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HWND* 
</dt> <dd>

Das Fenster Handle des Snap-in-Fensters, das diese Nachricht verarbeitet. Dieses Handle wird vom **hwndhidden** -Member der [**propsheetcfg**](propsheetcfg.md) -Struktur abgerufen.

</dd> <dt>

*wParam* 
</dt> <dd>

Enthält einen Zeiger auf eine [**DSA \_ sec- \_ Seiten \_ Informations**](dsa-sec-page-info.md) Struktur, die das zu Erstell führende sekundäre Eigenschaften Blatt definiert. Der Nachrichtenempfänger muss diesen Arbeitsspeicher mit der [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) -Funktion freigeben, wenn er nicht mehr benötigt wird.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Propsheetcfg**](propsheetcfg.md)
</dt> <dt>

[**\_ \_ Seite \_ Informationen zu DSA sec**](dsa-sec-page-info.md)
</dt> <dt>

[**Von LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 

