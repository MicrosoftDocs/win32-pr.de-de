---
description: Füllt ein Array von Zeigern auf IWiaItem2-Schnittstellen.
ms.assetid: 35fd5bdf-7e6c-431f-a9c6-62a86ee05f95
title: IEnumWiaItem2::Next-Methode (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Next
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: cf884375f504bb801bcebcaad3f75b23c5f82956ce3a1d45dd5a50bfa5f8e53c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451140"
---
# <a name="ienumwiaitem2next-method"></a>IEnumWiaItem2::Next-Methode

Füllt ein Array von Zeigern auf [**IWiaItem2-Schnittstellen.**](-wia-iwiaitem2.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT Next(
  [in]      ULONG     cElt,
  [out]     IWiaItem2 **ppIWiaItem2,
  [in, out] ULONG     *pcEltFetched
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cElt* \[ In\]
</dt> <dd>

Typ: **ULONG**

Gibt die Anzahl der Arrayelemente im Array an, die durch den *ppIWiaItem2-Parameter angegeben* werden.

</dd> <dt>

*ppIWiaItem2* \[ out\]
</dt> <dd>

Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Empfängt die Adresse eines Arrays von [**IWiaItem2-Schnittstellenzeigen.**](-wia-iwiaitem2.md) **IEnumWiaItem2::Next** füllt dieses Array mit Schnittstellenzeigen.

</dd> <dt>

*pcEltFetched* \[ in, out\]
</dt> <dd>

Typ: **ULONG \***

Bei der Ausgabe empfängt dieser Parameter die Anzahl von Schnittstellenzeigen, die tatsächlich in dem Array gespeichert sind, das durch den *ppIWiaItem2-Parameter angegeben* wird. Wenn die Enumeration abgeschlossen ist, enthält dieser Parameter 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Das Windows Image Acquisition (WIA) 2.0-Laufzeitsystem stellt WIA 2.0-Hardwaregeräte als hierarchische Struktur von [**IWiaItem2-Objekten**](-wia-iwiaitem2.md) dar. Anwendungen verwenden die **IEnumWiaItem2::Next-Methode,** um einen **IWiaItem2-Schnittstellenzeiger** für jedes Element im aktuellen Ordner der **IWiaItem2-Objektstruktur** eines Hardwaregeräts zu erhalten.

Um die Liste der Zeiger zu erhalten, übergibt die Anwendung ein Array von [**IWiaItem2-Schnittstellenzeigen,**](-wia-iwiaitem2.md) die sie zuteilen. Außerdem wird die Anzahl der Arrayelemente im Parameter *cElt übergeben.* Die **IEnumWiaItem2::Next-Methode** füllt das Array mit Zeigern auf **IWiaItem2-Schnittstellen** auf.

Bis der Enumerationsprozess abgeschlossen ist, gibt die **IEnumWiaItem2::Next-Methode** S \_ OK zurück. Jedes Mal, wenn dies der Fall ist, wird der Wert, auf den *pcEltFetched* zeigt, auf die Anzahl der Elemente, die in das Array eingefügt wurden, fest. Wenn **IEnumWiaItem2::Next** den Prozess zum Aufzählen von [**IWiaItem2-Objekten**](-wia-iwiaitem2.md) beendet, wird S FALSE zurückgegeben und der Speicherort, auf den \_ *pcEltFetched* zeigt, auf 0 (null) festgelegt.

Anwendungen müssen die [IUnknown::Release-Methode für](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) die Schnittstellenzeigen aufrufen, die sie über den *ppIWiaItem2-Parameter* erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
