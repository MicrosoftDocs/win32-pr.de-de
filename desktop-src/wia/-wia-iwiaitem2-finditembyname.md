---
description: Durchsucht die Unterelementstruktur eines Elements unter Verwendung des Namens als Suchschlüssel.
ms.assetid: e4ce0bfb-9793-4928-b454-66ae1455b7b5
title: IWiaItem2::FindItemByName-Methode (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.FindItemByName
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 5ef0ffdf710d36d2d6c515352bf441e9c66ae169400528db5d5943e2114fefd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118440408"
---
# <a name="iwiaitem2finditembyname-method"></a>IWiaItem2::FindItemByName-Methode

Durchsucht die Unterelementstruktur eines Elements unter Verwendung des Namens als Suchschlüssel.

## <a name="syntax"></a>Syntax


```C++
HRESULT FindItemByName(
  [in]  LONG      lFlags,
  [in]  BSTR      bstrFullItemName,
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lFlags* \[ In\]
</dt> <dd>

Typ: **LONG**

Derzeit nicht verwendet. Sollte auf Null festgelegt werden.

</dd> <dt>

*bstrFullItemName* \[ In\]
</dt> <dd>

Typ: **BSTR**

Gibt den Namen des zu suchden Elements an.

</dd> <dt>

*ppIWiaItem2* \[ out\]
</dt> <dd>

Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Empfängt die Adresse eines Zeigers auf die [**IWiaItem2-Schnittstelle**](-wia-iwiaitem2.md) des gefundenen Elements.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Methode durchsucht die Struktur der unteren Elemente des aktuellen Elements unter Verwendung des Namens als Suchschlüssel. Wenn **IWiaItem2::FindItemByName** das durch *bstrFullItemName* angegebene Element findet, wird die Adresse eines Zeigers auf die [**IWiaItem2-Schnittstelle**](-wia-iwiaitem2.md) des Elements im *ppIWiaItem2-Parameter* gespeichert.

Anwendungen müssen die [IUnknown::Release-Methode für](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) die Schnittstellenzeigen aufrufen, die sie über den *ppIWiaItem2-Parameter* erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
