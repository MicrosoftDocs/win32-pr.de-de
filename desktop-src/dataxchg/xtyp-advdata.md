---
title: XTYP_ADVDATA Transaktion (Ddeml. h)
description: Informiert den Client, dass sich der Wert des Datenelements geändert hat. Dynamischer Datenaustausch die DDE-Client Rückruffunktion (DDE Callback) empfängt diese Transaktion, nachdem eine Empfehlung-Schleife mit einem Server eingerichtet wurde.
ms.assetid: c6e61785-b98c-4ffa-9d23-339e1c66cb4d
keywords:
- XTYP_ADVDATA Transaktionsdaten Austausch
topic_type:
- apiref
api_name:
- XTYP_ADVDATA
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8359e34388d185200b5f30c4554e138cc1f6b94a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338120"
---
# <a name="xtyp_advdata-transaction"></a>\_Xttyadvdata-Transaktion

Informiert den Client, dass sich der Wert des Datenelements geändert hat. Dynamischer Datenaustausch die DDE-Client Rückruffunktion ( [*DDE Callback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)) empfängt diese Transaktion, nachdem eine Empfehlung-Schleife mit einem Server eingerichtet wurde.


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_ADVDATA            (0x0010 | XCLASS_FLAGS         )
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*uType* 
</dt> <dd>

Der Transaktionstyp:

</dd> <dt>

*UF* 
</dt> <dd>

Das Format Atom der vom Server gesendeten Daten.

</dd> <dt>

*has* 
</dt> <dd>

Ein Handle für die Konversation.

</dd> <dt>

*hsz1* 
</dt> <dd>

Ein Handle für den Themen Namen.

</dd> <dt>

*hsz2* 
</dt> <dd>

Ein Handle für den Elementnamen.

</dd> <dt>

*hdata* 
</dt> <dd>

Ein Handle für die Daten, die dem Themen Namen und dem Elementnamen paar zugeordnet sind. Dieser Parameter ist **null** , wenn der Client das **xtypf \_ NODATA** -Flag angegeben hat, als er die Empfehlung-Schleife angefordert hat.

</dd> <dt>

*dwData1* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwData2* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine DDE-Rückruffunktion sollte **DDE \_ fakk** zurückgeben, wenn Sie diese Transaktion verarbeitet, **DDE \_ fausgelastet** , wenn Sie für die Verarbeitung dieser Transaktion zu stark ausgelastet ist, oder **DDE \_ fnotverarbeitete** , wenn Sie diese Transaktion ablehnt.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung darf das Daten handle, das während dieser Transaktion abgerufen wurde, nicht freigeben. Eine Anwendung muss jedoch die Daten kopieren, die dem Daten Handle zugeordnet sind, wenn die Anwendung die Daten verarbeiten muss, nachdem die Rückruffunktion zurückgegeben hat. Eine Anwendung kann die [**DDE GetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) -Funktion verwenden, um die Daten zu kopieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Ddeml. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**DDE clienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[**DDE GetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

[**DDE postadvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

**Licher**
</dt> <dt>

[dynamischer Datenaustausch-Verwaltungs Bibliothek](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

