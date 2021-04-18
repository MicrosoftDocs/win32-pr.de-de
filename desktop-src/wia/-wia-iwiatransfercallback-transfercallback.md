---
description: Gibt den Fortschritt und andere Benachrichtigungen während einer Übertragung an.
ms.assetid: 0faba0f8-b318-4c47-85e0-5ce128fe1c82
title: 'Iwiatransfercallback:: transfercallback-Methode (WIA. h)'
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
ms.openlocfilehash: f1e2f939a7a3d768fc744c0603563b0a088e08f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354496"
---
# <a name="iwiatransfercallbacktransfercallback-method"></a>Iwiatransfercallback:: transfercallback-Methode

Gibt den Fortschritt und andere Benachrichtigungen während einer Übertragung an.

## <a name="syntax"></a>Syntax


```C++
HRESULT TransferCallback(
  [in] LONG              lFlags,
  [in] WiaTransferParams *pWiaTransferParams
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lFlags* \[ in\]
</dt> <dd>

Type: **Long**

Derzeit nicht verwendet. Sollte auf Null festgelegt werden.

</dd> <dt>

*pwiatransferpara* \[ in\]
</dt> <dd>

Typ: **[**wiatransferparameams**](-wia-wiatransferparams.md) \** _

Gibt einen Zeiger auf eine [_ *wiatransferparameams* *](-wia-wiatransferparams.md) -Struktur an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn diese Methode von einem Bild Verarbeitungs Filter implementiert wird, ruft der Windows-Abbild Erwerb (WIA) 2,0 Mini Treiber Sie während der Abbild Erfassung auf, um Statusmeldungen an die Anwendung zurückzusenden.

**Iwiatransfercallback:: transfercallback** eines Filters muss an die **iwiatransfercallback:: transfercallback** -Methode des Anwendungs Rückrufs delegiert werden. Normalerweise filtert der Filterdaten Strom die an ihn über gebenden Daten und schreibt die gefilterten Daten direkt in den von der Anwendung bereitgestellten Stream. Wenn der Bild Verarbeitungs Filterdaten zwischen Aufrufen der [IStream:: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) -Methode speichert, muss er auch die Werte *lprozentucomplete* und *ulbytesschreibbcurrentstream* in der [**wiatransferparameams**](-wia-wiatransferparams.md) -Struktur ändern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
