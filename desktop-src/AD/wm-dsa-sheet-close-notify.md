---
title: WM_DSA_SHEET_CLOSE_NOTIFY Meldung
description: Wird an das Active Directory MMC-Snap-in gesendet, wenn ein sekundäres Eigenschaften Blatt zerstört wird.
ms.assetid: 74271550-e1f7-4576-a04f-52d5b7c619cb
ms.tgt_platform: multiple
keywords:
- WM_DSA_SHEET_CLOSE_NOTIFY Meldung Active Directory
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CLOSE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36f03cdb6224ae5f55bc995897d766ce61e67693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341614"
---
# <a name="wm_dsa_sheet_close_notify-message"></a>WM- \_ DSA- \_ Blatt " \_ \_ Nachricht schließen"

Wenn ein sekundäres Eigenschaften Blatt zerstört wird, wird die Meldung zum Schließen der Meldung zum **\_ \_ \_ Schließen \_ des WM** -MMC an das Active Directory MMC-Snap-in gesendet.

> [!Note]  
> Dieser Nachrichtenwert ist nicht in einer veröffentlichten Header Datei definiert. Wenn Sie diesen Nachrichtenwert verwenden möchten, müssen Sie ihn im exakten Format definieren.

 


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

*HWND* 
</dt> <dd>

Das Fenster Handle des Snap-in-Fensters, das diese Nachricht verarbeitet. Dieses Handle wird vom **hwndhidden** -Member der [**propsheetcfg**](propsheetcfg.md) -Struktur abgerufen.

</dd> <dt>

*wParam* 
</dt> <dd>

Enthält einen von der Anwendung definierten 32-Bit-Wert. Dies wird vom **wparamsheetclose** -Member der [**propsheetcfg**](propsheetcfg.md) -Struktur abgerufen.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Nachricht wird nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Propsheetcfg**](propsheetcfg.md)
</dt> </dl>

 

 





