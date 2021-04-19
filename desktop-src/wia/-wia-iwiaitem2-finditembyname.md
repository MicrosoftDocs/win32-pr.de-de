---
description: Durchsucht die Baumstruktur eines Elements anhand des Namens als Suchschlüssel.
ms.assetid: e4ce0bfb-9793-4928-b454-66ae1455b7b5
title: 'IWiaItem2:: finditembyname-Methode (WIA. h)'
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
ms.openlocfilehash: 821be7e4abd8d1396befa886093aa197bcdea7f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348791"
---
# <a name="iwiaitem2finditembyname-method"></a>IWiaItem2:: finditembyname-Methode

Durchsucht die Baumstruktur eines Elements anhand des Namens als Suchschlüssel.

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

*lFlags* \[ in\]
</dt> <dd>

Type: **Long**

Derzeit nicht verwendet. Sollte auf Null festgelegt werden.

</dd> <dt>

*bstraufullitemname* \[ in\]
</dt> <dd>

Typ: **BSTR**

Gibt den Namen des zu suchenden Elements an.

</dd> <dt>

*ppIWiaItem2* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Empfängt die Adresse eines Zeigers auf die [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle des gefundenen Elements.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Mit dieser Methode wird die Struktur der untergeordneten Elemente des aktuellen Elements mithilfe des Namens als Suchschlüssel durchsucht. Wenn **IWiaItem2:: finditembyname** das von *bstraufullitemname* angegebene Element findet, speichert es die Adresse eines Zeigers auf die [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle des Elements im *ppIWiaItem2* -Parameter.

Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für die Schnittstellen Zeiger aufrufen, die Sie über den *ppIWiaItem2* -Parameter empfangen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
