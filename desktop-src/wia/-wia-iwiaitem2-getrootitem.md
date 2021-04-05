---
description: Ruft das Stamm Element einer Struktur von Item-Objekten ab, die zum Darstellen eines Windows-Abbild Erwerbs (WIA) 2,0-Hardware Geräts verwendet werden.
ms.assetid: bc31ad4a-0851-4510-a038-83646ffd5c98
title: 'IWiaItem2:: GetRootItem-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetRootItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: c8d4f004cc9c7cabaf4898f5e8c838a0399dc106
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751777"
---
# <a name="iwiaitem2getrootitem-method"></a>IWiaItem2:: GetRootItem-Methode

Ruft das Stamm Element einer Struktur von Item-Objekten ab, die zum Darstellen eines Windows-Abbild Erwerbs (WIA) 2,0-Hardware Geräts verwendet werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRootItem(
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppIWiaItem2* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Empfängt die Adresse eines Zeigers auf die [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle des Stamm Elements.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn ein beliebiges [**IWiaItem2**](-wia-iwiaitem2.md) -Objekt in der Objektstruktur eines WIA 2,0-Hardware Geräts vorhanden ist, ruft die Anwendung durch Aufrufen dieser Funktion einen Zeiger auf das Stamm Element ab.

Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für die Schnittstellen Zeiger aufrufen, die Sie über den *ppIWiaItem2* -Parameter empfangen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
