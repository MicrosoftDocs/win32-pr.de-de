---
title: ICM_COMPRESS Meldung (VFW. h)
description: In der ICM- \_ Komprimierungs Meldung wird ein Video Komprimierungs Treiber benachrichtigt, um einen Datenrahmen in einen Anwendungs definierten Puffer zu komprimieren.
ms.assetid: d95b943f-458d-4a5e-bab1-e3648d323395
keywords:
- ICM_COMPRESS-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_COMPRESS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8021a4c18ab47c9b5b848dd1cb097358f2714bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340359"
---
# <a name="icm_compress-message"></a>ICM- \_ Komprimierungs Meldung

In der **ICM- \_ Komprimierungs** Meldung wird ein Video Komprimierungs Treiber benachrichtigt, um einen Datenrahmen in einen Anwendungs definierten Puffer zu komprimieren.


```C++
ICM_COMPRESS 
wParam = (DWORD) (LPVOID) &icc; 
lParam = sizeof(ICCOMPRESS); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="icc"></span><span id="ICC"></span>*ausgeliefert*
</dt> <dd>

Zeiger auf eine [**iccompress**](/windows/desktop/api/Vfw/ns-vfw-iccompress) -Struktur. Die folgenden Member dieser Struktur geben die Komprimierungs Parameter an: **lpbiinput**, **lpinput**, **lpbioutput**, **lpoutput**, **lpbiprev**, **lpprev**, **lpckid**, **lpdwflags**, **dwframesize** und **dwquality**. Der Treiber sollte auch den **bisizeimage** -Member der [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) -Struktur verwenden, die **lpbioutput** von **iccompress** zugeordnet ist, um die Größe des komprimierten Rahmens zurückzugeben.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Größe von [**iccompress**](/windows/desktop/api/Vfw/ns-vfw-iccompress)(in Bytes).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.

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

 

