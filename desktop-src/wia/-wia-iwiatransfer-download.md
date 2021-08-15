---
description: Initiiert einen Datendownload an den Aufrufer.
ms.assetid: e639fabb-2c13-4009-affa-1c2b06c0d4c8
title: IWiaTransfer::D ownload-Methode (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Download
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 039b7dd4579419bac744a07bbc6ddd55c4b0b2e2e713340bf256fdb95d8fc071
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450210"
---
# <a name="iwiatransferdownload-method"></a>IWiaTransfer::D ownload-Methode

Initiiert einen Datendownload an den Aufrufer.

## <a name="syntax"></a>Syntax


```C++
HRESULT Download(
  [in] LONG                 lFlags,
  [in] IWiaTransferCallback *pIWiaTransferCallback
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lFlags* \[ In\]
</dt> <dd>

Typ: **LONG**

Derzeit nicht verwendet. Sollte auf Null festgelegt werden.

</dd> <dt>

*pIWiaTransferCallback* \[ In\]
</dt> <dd>

Typ: **[ **IWiaTransferCallback**](-wia-iwiatransfercallback.md)\***

Gibt einen Zeiger auf die [**IWiaTransferCallback-Schnittstelle**](-wia-iwiatransfercallback.md) des Aufrufers an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Wenn ein Ordner heruntergeladen wird, werden auch alle untergeordneten Elemente dieses Ordners übertragen. Jedes Element wird in einem separaten Stream übertragen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 




