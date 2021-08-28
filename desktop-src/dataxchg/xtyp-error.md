---
title: XTYP_ERROR Transaktion (Ddeml.h)
description: Eine DDE-Rückruffunktion (dynamische Daten Exchange, DdeCallback) empfängt die XTYP \_ ERROR-Transaktion, wenn ein kritischer Fehler auftritt.
ms.assetid: 710daa04-ed83-42e3-a55e-6ccf891a3d52
keywords:
- XTYP_ERROR transaktion Exchange
topic_type:
- apiref
api_name:
- XTYP_ERROR
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce59800723758201b4857b5a3ae0844675347b2d4fd403c77650b36d9275bfb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755980"
---
# <a name="xtyp_error-transaction"></a>XTYP \_ ERROR-Transaktion

Eine dynamische Daten Exchange-Rückruffunktion [*(DDE), DdeCallback,*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)empfängt die **XTYP \_ ERROR-Transaktion,** wenn ein kritischer Fehler auftritt.


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_ERROR              (0x0000 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK )
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*uType* 
</dt> <dd>

Der Transaktionstyp:

</dd> <dt>

*uFmt* 
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

*hconv* 
</dt> <dd>

Ein Handle für die Konversation, die dem Fehler zugeordnet ist. Dieser Parameter ist **NULL,** wenn der Fehler keiner Konversation zugeordnet ist.

</dd> <dt>

*hsz1* 
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

*hsz2* 
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

*hdata* 
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

*dwData1* 
</dt> <dd>

Der Fehlercode im Wort mit niedriger Reihenfolge. Derzeit wird nur der folgende Fehlercode unterstützt.



| Wert                                                                                                                                                                      | Bedeutung                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="DMLERR_LOW_MEMORY"></span><span id="dmlerr_low_memory"></span><dl> <dt>**DMLERR \_ LOW \_ MEMORY**</dt> </dl> | Der Arbeitsspeicher ist gering. Daten zum Raten, Verwerten oder Ausführen können verloren gegangen sein, oder das System schlägt fehl.<br/> |



 

</dd> <dt>

*dwData2* 
</dt> <dd>

Wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Eine Anwendung kann diesen Transaktionstyp nicht blockieren. der **CBR \_ BLOCK-Rückgabecode** wird ignoriert. Die dynamische Daten Exchange Management Library (DDEML) versucht, Arbeitsspeicher freizugeben, indem nicht kritische Ressourcen entfernt werden. Eine Anwendung, die Konversationen blockiert hat, sollte die Blockierung aufheben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Ddeml.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über dynamische Daten Exchange-Verwaltungsbibliothek](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

