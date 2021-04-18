---
title: XTYP_ERROR Transaktion (Ddeml. h)
description: Eine dynamischer Datenaustausch (DDE)-Rückruffunktion (DDE Callback) empfängt die xD- \_ Fehler Transaktion, wenn ein kritischer Fehler auftritt.
ms.assetid: 710daa04-ed83-42e3-a55e-6ccf891a3d52
keywords:
- XTYP_ERROR Transaktionsdaten Austausch
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
ms.openlocfilehash: ebbad80cb23a37881e8954dee4a80a87f253e499
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337328"
---
# <a name="xtyp_error-transaction"></a>XYP- \_ Fehler Transaktion

Eine dynamischer Datenaustausch (DDE)-Rückruffunktion ( [*DDE Callback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)) empfängt die **xD- \_ Fehler** Transaktion, wenn ein kritischer Fehler auftritt.


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

*UF* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*has* 
</dt> <dd>

Ein Handle für die Konversation, die dem Fehler zugeordnet ist. Dieser Parameter ist **null** , wenn der Fehler nicht mit einer Konversation verknüpft ist.

</dd> <dt>

*hsz1* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*hsz2* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*hdata* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwData1* 
</dt> <dd>

Der Fehlercode im nieder wertigen Wort. Derzeit wird nur der folgende Fehlercode unterstützt.



| Wert                                                                                                                                                                      | Bedeutung                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="DMLERR_LOW_MEMORY"></span><span id="dmlerr_low_memory"></span><dl> <dt>**dmlerr \_ wenig Arbeits \_ Speicher**</dt> </dl> | Der Arbeitsspeicher ist niedrig. Daten vom Typ "Empfehlung", "Poke" oder "ausführen" können verloren gehen, oder das System schlägt fehl.<br/> |



 

</dd> <dt>

*dwData2* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Transaktionstyp kann von einer Anwendung nicht blockiert werden. der Rückgabecode des **CBR- \_ Blocks** wird ignoriert. Die Ddeml (dynamischer Datenaustausch Management Library) versucht, Arbeitsspeicher freizugeben, indem nicht kritische Ressourcen entfernt werden. Eine Anwendung, die blockierte Konversationen hat, sollte Sie entsperren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Ddeml. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über die dynamischer Datenaustausch-Verwaltungs Bibliothek](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

