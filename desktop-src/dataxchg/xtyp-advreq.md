---
title: XTYP_ADVREQ Transaktion (Ddeml. h)
description: Mit der xtipp- \_ advreq-Transaktion wird dem Server mitgeteilt, dass eine Benachrichtigungs Transaktion für den angegebenen Themen Namen und das angegebene Elementnamen paar aussteht und dass die Daten, die dem Themen Namen und dem Elementnamen paar entsprechen, geändert wurden.
ms.assetid: 9bd43e61-cbd6-4d53-bab3-90e85819b16b
keywords:
- XTYP_ADVREQ Transaktionsdaten Austausch
topic_type:
- apiref
api_name:
- XTYP_ADVREQ
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2884e838268342ab10c556c6ae3cfc8349ed5d2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391974"
---
# <a name="xtyp_advreq-transaction"></a>XYP- \_ advreq-Transaktion

Mit der **xtipp- \_ advreq** -Transaktion wird dem Server mitgeteilt, dass eine Benachrichtigungs Transaktion für den angegebenen Themen Namen und das angegebene Elementnamen paar aussteht und dass die Daten, die dem Themen Namen und dem Elementnamen paar entsprechen, geändert wurden. Das System sendet diese Transaktion an die dynamischer Datenaustausch (DDE)-Rückruffunktion [*ddecallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), nachdem der Server die [**ddepostadvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) -Funktion aufgerufen hat.


```C++
#define     XCLASS_DATA              0x2000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_ADVREQ             (0x0020 | XCLASS_DATA | XTYPF_NOBLOCK )
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*uType* 
</dt> <dd>

Der Transaktionstyp:

</dd> <dt>

*UF* 
</dt> <dd>

Das Format, in dem die Daten an den Client übermittelt werden sollen.

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

Ein Handle für den Elementnamen, der geändert wurde.

</dd> <dt>

*hdata* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwData1* 
</dt> <dd>

Die Anzahl der **xD \_ advreq** -Transaktionen im nieder wertigen Wort, die im Kontext des aktuellen Aufrufens der [**ddepostadvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) -Funktion für dasselbe Thema, Element und denselben Format Namen verarbeitet werden. Der Zählerwert ist 0 (null), wenn die aktuelle **xD- \_ advreq** -Transaktion der letzte ist. Ein Server kann diese Anzahl verwenden, um zu bestimmen, ob ein **hdata \_** -Daten Handle für die Empfehlung erstellt werden soll.

Das nieder wertige Wort wird auf **cadv \_ lateack** festgelegt, wenn die Ddeml die **xD- \_ advreq** -Transaktion aufgrund einer Nachricht, die eine späte Bestätigung durchläuft, von \_ einem Client, der vom Server entfernt wird, ausgegeben hat.

Das höchst wertige Wort wird nicht verwendet.

</dd> <dt>

*dwData2* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Server sollte zuerst die [**ddecreatedatahandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) -Funktion aufrufen, um ein Daten Handle zu erstellen, das die geänderten Daten identifiziert und dann das Handle zurückgibt. Der Server sollte **null** zurückgeben, wenn die Transaktion nicht abgeschlossen werden kann.

## <a name="remarks"></a>Bemerkungen

Ein Server kann diesen Transaktionstyp nicht blockieren. der Rückgabecode des **CBR- \_ Blocks** wird ignoriert.

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

[**Ddecreatedatahandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)
</dt> <dt>

[**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DDE postadvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

**Licher**
</dt> <dt>

[dynamischer Datenaustausch-Verwaltungs Bibliothek](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

