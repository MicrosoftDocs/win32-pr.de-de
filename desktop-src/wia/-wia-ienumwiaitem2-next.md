---
description: Füllt ein Array von Zeigern auf IWiaItem2-Schnittstellen auf.
ms.assetid: 35fd5bdf-7e6c-431f-a9c6-62a86ee05f95
title: 'IEnumWiaItem2:: Next-Methode (WIA. h)'
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
ms.openlocfilehash: 2e8800ead0c8f0abaddd0f055f31962d4d55d14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214835"
---
# <a name="ienumwiaitem2next-method"></a>IEnumWiaItem2:: Next-Methode

Füllt ein Array von Zeigern auf [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstellen auf.

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

*celt* \[ in\]
</dt> <dd>

Typ: **ulong**

Gibt die Anzahl der Array Elemente in dem Array an, das durch den *ppIWiaItem2* -Parameter angegeben wird.

</dd> <dt>

*ppIWiaItem2* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Empfängt die Adresse eines Arrays von [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstellen Zeigern. **IEnumWiaItem2:: Next** füllt dieses Array mit Schnittstellen Zeigern.

</dd> <dt>

*pceltfetch* \[ in, out\]
</dt> <dd>

Typ: **ulong \** _

Bei der Ausgabe empfängt dieser Parameter die Anzahl der Schnittstellen Zeiger, die tatsächlich in dem Array gespeichert werden, das durch den _ppIWiaItem2 *-Parameter angegeben wird. Wenn die Enumeration fertig ist, enthält dieser Parameter 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Das Windows Image Acquisition (WIA) 2,0-Laufzeitsystem stellt WIA 2,0-Hardware Geräte als hierarchische Struktur von [**IWiaItem2**](-wia-iwiaitem2.md) -Objekten dar. Anwendungen verwenden die **IEnumWiaItem2:: Next** -Methode zum Abrufen eines **IWiaItem2** -Schnittstellen Zeigers für jedes Element im aktuellen Ordner der **IWiaItem2** -Objektstruktur eines Hardware Geräts.

Um die Liste der Zeiger zu erhalten, übergibt die Anwendung ein Array von [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstellen Zeigern, die Sie zugeordnet. Außerdem wird die Anzahl der Array Elemente im *celt*-Parameter übergeben. Die **IEnumWiaItem2:: Next** -Methode füllt das Array mit Zeigern auf **IWiaItem2** -Schnittstellen auf.

Bis der enumerationsprozess abgeschlossen ist, gibt die **IEnumWiaItem2:: Next** -Methode S \_ OK zurück. Jedes Mal, wenn dies der Fall ist, wird der Wert, auf den *pceltfetch* zeigt, auf die Anzahl der in das Array eingefügten Elemente festgelegt. Wenn **IEnumWiaItem2:: Next** den Prozess der Enumeration von [**IWiaItem2**](-wia-iwiaitem2.md) -Objekten abschließt, wird S false zurückgegeben, \_ und der Speicher Speicherort, auf den *pceltfetch* verweist, wird auf 0 festgelegt.

Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für die Schnittstellen Zeiger aufrufen, die Sie über den *ppIWiaItem2* -Parameter empfangen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
