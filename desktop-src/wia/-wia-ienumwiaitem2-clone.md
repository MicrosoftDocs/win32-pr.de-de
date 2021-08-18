---
description: Erstellt eine zusätzliche Instanz der IEnumWiaItem2-Schnittstelle und sendet einen Zeiger darauf zurück.
ms.assetid: 0d36d555-d0d9-4a1c-ac54-de611850449c
title: IEnumWiaItem2::Clone-Methode (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Clone
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 21c94c634a6930f28f48cdc35a4d3cf199b8fa33e9fb5f08444797fd76f50c45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965849"
---
# <a name="ienumwiaitem2clone-method"></a>IEnumWiaItem2::Clone-Methode

Erstellt eine zusätzliche Instanz der [**IEnumWiaItem2-Schnittstelle**](-wia-ienumwiaitem2.md) und sendet einen Zeiger darauf zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT Clone(
  [out] IEnumWiaItem2 **ppIEnum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppIEnum* \[ out\]
</dt> <dd>

Typ: **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***

Empfängt die Adresse der [**IEnumWiaItem2-Schnittstelleninstanz,**](-wia-ienumwiaitem2.md) die **IEnumWiaItem2::Clone erstellt.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Anwendungen müssen die [IUnknown::Release-Methode für](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) die Schnittstellenze0er aufrufen, die sie über *den ppIEnum-Parameter* empfangen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
