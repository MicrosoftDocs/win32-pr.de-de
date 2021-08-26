---
title: ICM_GET (Vfw.h)
description: Die ICM \_ GET-Nachricht ruft einen anwendungsdefinierten DWORD-Wert aus einem Videokomprimierungstreiber ab.
ms.assetid: 288c0053-16a1-4547-b748-da218a0b588c
keywords:
- ICM_GET von Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_GET
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8885faf7b0605378ace3004165004384a582c9d49a0a8ce047122c108b6cb8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038730"
---
# <a name="icm_get-message"></a>\_ICM GET-Nachricht

Die **ICM \_ GET-Nachricht** ruft einen anwendungsdefinierten **DWORD-Wert** aus einem Videokomprimierungstreiber ab.


```C++
ICM_GET 
wParam = (DWORD) (LPVOID) pv; 
lParam = (DWORD) cb; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="pv"></span><span id="PV"></span>*Pv*
</dt> <dd>

Zeiger auf einen Speicherblock, der mit dem aktuellen Zustand gefüllt werden soll. Sie können auch **NULL angeben,** um die Menge an Arbeitsspeicher zu bestimmen, die für die Zustandsinformationen erforderlich ist.

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*Cb*
</dt> <dd>

Größe des Speicherblocks in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Menge an Arbeitsspeicher in Bytes zurück, die zum Speichern der Statusinformationen erforderlich ist.

## <a name="remarks"></a>Hinweise

Die Zum Darstellen von Zustandsinformationen verwendete Struktur ist treiberspezifisch und wird vom Treiber definiert.

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

 

 





