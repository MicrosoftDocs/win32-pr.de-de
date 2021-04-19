---
title: ICM_SETSTATE Meldung (VFW. h)
description: In der ICM- \_ SetState-Meldung wird ein Video Komprimierungs Treiber benachrichtigt, um den Status des-Kompressors festzulegen. Sie können diese Nachricht explizit oder mithilfe des icsetstate-Makros senden.
ms.assetid: d1a91847-2893-4c8b-9ca1-02db71ec2c81
keywords:
- ICM_SETSTATE-Nachricht (Multimedia)
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
ms.openlocfilehash: 230e0aaf3752016efd276d7d55624ee2abb4f8e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339606"
---
# <a name="icm_setstate-message"></a>ICM- \_ SetState-Meldung

In der **ICM- \_ SetState** -Meldung wird ein Video Komprimierungs Treiber benachrichtigt, um den Status des-Kompressors festzulegen. Sie können diese Nachricht explizit oder mithilfe des [**icsetstate**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) -Makros senden.


```C++
ICM_SETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="pv"></span><span id="PV"></span>*teuren*
</dt> <dd>

Zeiger auf einen Speicherblock, der Konfigurationsdaten enthält. Sie können **null** für diesen Parameter angeben, um den-Kompressor auf den Standardzustand zurückzusetzen.

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*betrieben*
</dt> <dd>

Größe des Speicherblocks in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der Bytes zurück, die vom-Kompressor bei erfolgreicher Ausführung verwendet werden, andernfalls NULL.

## <a name="remarks"></a>Bemerkungen

Die von dieser Nachricht verwendeten Informationen sind privat und spezifisch für einen bestimmten Kompressor. Client Anwendungen sollten diese Nachricht nur zum Wiederherstellen von Informationen verwenden, die zuvor mit der [**ICM \_ GetState**](icm-getstate.md) -Nachricht abgerufen wurden, und die [**ICM \_**](icm-configure.md) -Konfigurations Nachricht verwenden, um die Konfiguration eines Video Komprimierungs Treibers anzupassen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Videokomprimierungs-Manager](video-compression-manager.md)
</dt> <dt>

[Video Komprimierungs Meldungen](video-compression-messages.md)
</dt> </dl>

 

 





