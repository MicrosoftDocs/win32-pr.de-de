---
description: Ruft den MICROSOFT MEDIA FOUNDATION VIDEO RENDERING-Senke ab.
ms.assetid: 809e89e4-3ed5-4dba-82dc-4ec217b8ef38
title: MANAGERSXGIDeviceManagerSource::GetManager-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFDXGIDeviceManagerSource.GetManager
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: 9e42e42e88dfa2acec9061a54f3a8fcc96128ad5aee6ff004e49f6dd10062074
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957831"
---
# <a name="imfdxgidevicemanagersourcegetmanager-method"></a>MANAGERSXGIDeviceManagerSource::GetManager-Methode

Ruft den [**MICROSOFT MEDIA FOUNDATION**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) VIDEO RENDERING-Senke ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetManager(
  [out] IMFDXGIDeviceManager **ppManager
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppManager* \[ out\]
</dt> <dd>

Das [**OBJECTDXGIDeviceManager-Objekt.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 \|Desktop-Apps UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[R2-Desktop-Apps \| UWP-Apps\]<br/>                       |
| Idl<br/>                      | <dl> <dt>Mfidl.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MANAGERSXGIDeviceManagerSource**](imfdxgidevicemanagersource.md)
</dt> </dl>

 

 




