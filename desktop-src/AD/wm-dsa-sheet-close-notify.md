---
title: WM_DSA_SHEET_CLOSE_NOTIFY-Nachricht
description: Wird im Active Directory-MMC-Snap-In veröffentlicht, wenn ein sekundäres Eigenschaftenblatt zerstört wird.
ms.assetid: 74271550-e1f7-4576-a04f-52d5b7c619cb
ms.tgt_platform: multiple
keywords:
- WM_DSA_SHEET_CLOSE_NOTIFY Active Directory-Nachricht
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CLOSE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f840790de51ce712b33fc9a9611934e8be9a76a35a0fc01a4ce0abe4ba040d2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181672"
---
# <a name="wm_dsa_sheet_close_notify-message"></a>WM \_ DSA \_ SHEET CLOSE \_ NOTIFY \_ message

Die **WM \_ DSA SHEET CLOSE \_ \_ \_ NOTIFY-Meldung** wird an das Active Directory MMC-Snap-In gesendet, wenn ein sekundäres Eigenschaftenblatt zerstört wird.

> [!Note]  
> Dieser Nachrichtenwert ist in einer veröffentlichten Headerdatei nicht definiert. Um diesen Nachrichtenwert zu verwenden, müssen Sie ihn selbst im genauen formatierten Format definieren.

 


```C++
#define WM_DSA_SHEET_CLOSE_NOTIFY (WM_USER + 5)
```




```C++
LRESULT SendMessage( (HWND)   hwnd, 
                     (UINT)   WM_DSA_SHEET_CLOSE_NOTIFY,
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

Enthält einen anwendungsdefinierten 32-Bit-Wert. Dies wird aus dem **wParamSheetClose-Member** der [**PROPSHEETCFG-Struktur**](propsheetcfg.md) ermittelt.

</dd> <dt>

*lParam* 
</dt> <dd>

Wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Meldung wird nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**PROPSHEETCFG**](propsheetcfg.md)
</dt> </dl>

 

 





