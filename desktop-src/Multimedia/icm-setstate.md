---
title: ICM_SETSTATE Nachricht (Vfw.h)
description: Die ICM \_ SETSTATE-Nachricht benachrichtigt einen Videokomprimierungstreiber, um den Zustand des Satzes festzulegen. Sie können diese Nachricht explizit oder mithilfe des ICSetState-Makros senden.
ms.assetid: d1a91847-2893-4c8b-9ca1-02db71ec2c81
keywords:
- ICM_SETSTATE nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_SETSTATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ea6cd7aa0314520a30e293a8f029920c22b8baa58e995eed7ff9e5a96dd1b7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525810"
---
# <a name="icm_setstate-message"></a>\_ICM SETSTATE-Nachricht

Die **ICM \_ SETSTATE-Nachricht** benachrichtigt einen Videokomprimierungstreiber, um den Zustand des Satzes festzulegen. Sie können diese Nachricht explizit oder mithilfe des [**ICSetState-Makros**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) senden.


```C++
ICM_SETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="pv"></span><span id="PV"></span>*Pv*
</dt> <dd>

Zeiger auf einen Speicherblock, der Konfigurationsdaten enthält. Sie können **NULL** für diesen Parameter angeben, um den Standardwert des -Parameters zurückzusetzen.

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*Cb*
</dt> <dd>

Größe des Speicherblocks in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl von Bytes zurück, die von der -Methode verwendet werden, wenn sie erfolgreich ist, oder 0 (null).

## <a name="remarks"></a>Hinweise

Die von dieser Nachricht verwendeten Informationen sind privat und spezifisch für einen bestimmten Kunden. Clientanwendungen sollten diese Nachricht nur zum Wiederherstellen von Informationen verwenden, die zuvor mit der [**ICM \_ GETSTATE-Nachricht**](icm-getstate.md) abgerufen wurden, und die [**ICM \_ CONFIGURE-Nachricht**](icm-configure.md) verwenden, um die Konfiguration eines Videokomprimierungstreibers anzupassen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Videokomprimierungs-Manager](video-compression-manager.md)
</dt> <dt>

[Videokomprimierungsmeldungen](video-compression-messages.md)
</dt> </dl>

 

 





