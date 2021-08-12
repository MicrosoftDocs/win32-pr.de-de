---
description: Stellt den Fortschritt und andere Benachrichtigungen während einer Übertragung bereit.
ms.assetid: 0faba0f8-b318-4c47-85e0-5ce128fe1c82
title: IWiaTransferCallback::TransferCallback-Methode (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback.TransferCallback
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 02c24f4cb1795e233fbbbb3dc30ad1bbb3624e104d59ac72f8e310bbbd323820
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118440318"
---
# <a name="iwiatransfercallbacktransfercallback-method"></a>IWiaTransferCallback::TransferCallback-Methode

Stellt den Fortschritt und andere Benachrichtigungen während einer Übertragung bereit.

## <a name="syntax"></a>Syntax


```C++
HRESULT TransferCallback(
  [in] LONG              lFlags,
  [in] WiaTransferParams *pWiaTransferParams
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lFlags* \[ In\]
</dt> <dd>

Typ: **LONG**

Derzeit nicht verwendet. Sollte auf Null festgelegt werden.

</dd> <dt>

*pWiaTransferParams* \[ In\]
</dt> <dd>

Typ: **[ **WiaTransferParams**](-wia-wiatransferparams.md)\***

Gibt einen Zeiger auf eine [**WiaTransferParams-Struktur**](-wia-wiatransferparams.md) an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Wenn diese Methode von einem Bildverarbeitungsfilter implementiert wird, ruft der minidriver Windows Image Acquisition (WIA) 2.0 diese während der Imageerfassung auf, um Statusmeldungen an die Anwendung zurückzusenden.

Die **IWiaTransferCallback::TransferCallback** eines Filters muss an die **IWiaTransferCallback::TransferCallback-Methode** des Anwendungsrückrufs delegiert werden. In der Regel filtert der Filterstream die an ihn übergebenen Daten und schreibt die gefilterten Daten direkt in den von der Anwendung bereitgestellten Stream. Wenn der Bildverarbeitungsfilter Daten zwischen Aufrufen der [IStream::Write-Methode](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) speichert, muss er auch die Werte *lPercentComplete* und *ulBytesWrittenToCurrentStream* in der [**WiaTransferParams-Struktur**](-wia-wiatransferparams.md) ändern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 
