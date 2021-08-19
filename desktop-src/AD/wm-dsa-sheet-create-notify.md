---
title: WM_DSA_SHEET_CREATE_NOTIFY-Nachricht
description: Wird im Active Directory-MMC-Snap-In veröffentlicht, um ein sekundäres Eigenschaftenblatt zu erstellen.
ms.assetid: 878878bf-fb78-4669-b282-1dd3349f35d5
ms.tgt_platform: multiple
keywords:
- WM_DSA_SHEET_CREATE_NOTIFY Active Directory-Nachricht
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CREATE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51fc850504eb4455a41b881aed1109554d0482a8f889fafa2eaf7050488e450
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024188"
---
# <a name="wm_dsa_sheet_create_notify-message"></a>WM \_ DSA \_ SHEET CREATE \_ NOTIFY \_ message

Die **MELDUNG WM \_ DSA SHEET CREATE \_ \_ \_ NOTIFY** wird an das Active Directory MMC-Snap-In gesendet, um ein sekundäres Eigenschaftenblatt zu erstellen.

> [!Note]  
> Dieser Nachrichtenwert ist in einer veröffentlichten Headerdatei nicht definiert. Um diesen Nachrichtenwert zu verwenden, definieren Sie ihn im genauen angezeigten Format.

 


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

*Hwnd* 
</dt> <dd>

Das Fensterhand handle des Snap-In-Fensters, das diese Meldung verarbeitet. Dieses Handle wird vom **hwndHidden-Member** der [**PROPSHEETCFG-Struktur**](propsheetcfg.md) erhalten.

</dd> <dt>

*wParam* 
</dt> <dd>

Enthält einen Zeiger auf eine [**DSA \_ SEC PAGE \_ \_ INFO-Struktur,**](dsa-sec-page-info.md) die das zu erstellende sekundäre Eigenschaftenblatt definiert. Der Nachrichtenempfänger muss diesen Arbeitsspeicher mit der [**LocalFree-Funktion**](/windows/desktop/api/winbase/nf-winbase-localfree) frei geben, wenn er nicht mehr benötigt wird.

</dd> <dt>

*lParam* 
</dt> <dd>

Wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wird nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PROPSHEETCFG**](propsheetcfg.md)
</dt> <dt>

[**DSA \_ \_ SEC-SEITENINFORMATIONEN \_**](dsa-sec-page-info.md)
</dt> <dt>

[**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 

