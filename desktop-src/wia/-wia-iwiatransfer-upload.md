---
description: Initiiert einen Daten Upload eines einzelnen Elements vom Aufrufer.
ms.assetid: 301ac5d9-b864-4c3c-bd4b-143cc4032dcb
title: 'Iwiatransfer:: Upload-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Upload
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 6aae6ca8f86d07ec052fdd59d24b0da2b96599d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214652"
---
# <a name="iwiatransferupload-method"></a>Iwiatransfer:: Upload-Methode

Initiiert einen Daten Upload eines einzelnen Elements vom Aufrufer.

## <a name="syntax"></a>Syntax


```C++
HRESULT Upload(
  [in] LONG                 lFlags,
  [in] IStream              *pSource,
  [in] IWiaTransferCallback *pIWiaTransferCallback
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lFlags* \[ in\]
</dt> <dd>

Type: **Long**

Derzeit nicht verwendet. Sollte auf Null festgelegt werden.

</dd> <dt>

*psource* \[ in\]
</dt> <dd>

Typ: **[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _

Gibt einen Zeiger auf die [IStream](/windows/win32/api/objidl/nn-objidl-istream) -Daten an.

</dd> <dt>

_pIWiaTransferCallback * \[ in\]
</dt> <dd>

Typ: **[**iwiatransfercallback**](-wia-iwiatransfercallback.md) \** _

Gibt einen Zeiger auf die [_ *iwiatransfercallback* *](-wia-iwiatransfercallback.md) -Schnittstelle des Aufrufers an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
