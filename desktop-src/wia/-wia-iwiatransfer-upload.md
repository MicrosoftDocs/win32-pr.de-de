---
description: Initiiert einen Datenupload eines einzelnen Elements vom Aufrufer.
ms.assetid: 301ac5d9-b864-4c3c-bd4b-143cc4032dcb
title: IWiaTransfer::Hochladen-Methode (Wia.h)
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
ms.openlocfilehash: 66bd542d27f29aa8fd531b6f3d8089d296efe2d963bcf967a0c1ab07e6f0db8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208238"
---
# <a name="iwiatransferupload-method"></a>IWiaTransfer::Hochladen-Methode

Initiiert einen Datenupload eines einzelnen Elements vom Aufrufer.

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

*lFlags* \[ In\]
</dt> <dd>

Typ: **LONG**

Derzeit nicht verwendet. Sollte auf Null festgelegt werden.

</dd> <dt>

*pSource* \[ In\]
</dt> <dd>

Typ: **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\***

Gibt einen Zeiger auf die [IStream-Daten](/windows/win32/api/objidl/nn-objidl-istream) an.

</dd> <dt>

*pIWiaTransferCallback* \[ In\]
</dt> <dd>

Typ: **[ **IWiaTransferCallback**](-wia-iwiatransfercallback.md)\***

Gibt einen Zeiger auf die [**IWiaTransferCallback-Schnittstelle**](-wia-iwiatransfercallback.md) des Aufrufers an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 
