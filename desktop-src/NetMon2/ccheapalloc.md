---
description: Die ccheapbelegc-Funktion ordnet Speicher auf der Grundlage der Erfassung zu.
ms.assetid: 6403c35f-d78f-48dc-90cc-0b76260bbab7
title: Cbillienc-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapAlloc
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 14fce9f56103803e575d295799a5c5971ed1c459
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864799"
---
# <a name="ccheapalloc-function"></a>Cbillienc-Funktion

Die **ccheapbelegc** -Funktion ordnet Speicher auf der Grundlage der Erfassung zu.

## <a name="syntax"></a>Syntax


```C++
LPVOID WINAPI CCHeapAlloc(
   DWORD dwBytes,
   BOOL  bZeroInit
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwBytes* 
</dt> <dd>

Angeforderte Länge des zugeordneten Arbeitsspeichers.

</dd> <dt>

*bzeroinit* 
</dt> <dd>

Indikator dafür, ob zugewiesener Arbeitsspeicher initialisiert wurde. Wenn der Parameterwert **true** ist, wird der zugeordnete Arbeitsspeicher mit 0 (null) initialisiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf den zugeordneten Arbeitsspeicher. Wenn Sie den belegten Arbeitsspeicher nicht mehr benötigen, können Sie den Speicher freigeben, indem Sie die [**ccheapfree**](ccheapfree.md) -Funktion aufrufen.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Setccinstptr**](setccinstptr.md)
</dt> <dt>

[**Getccinstptr**](getccinstptr.md)
</dt> <dt>

[**Ccheapfree**](ccheapfree.md)
</dt> <dt>

[**Ccheaprezuweisung**](ccheaprealloc.md)
</dt> <dt>

[**Ccheapsize**](ccheapsize.md)
</dt> </dl>

 

 




