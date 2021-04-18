---
description: Ruft den imsdxgidebug Manager aus der Microsoft Media Foundation Video Rendering-Senke ab.
ms.assetid: 809e89e4-3ed5-4dba-82dc-4ec217b8ef38
title: 'IMF dxgidevicemanagersource:: GetManager-Methode'
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
ms.openlocfilehash: 098810e9e06f339b1035748d71f46c7af26e96a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343842"
---
# <a name="imfdxgidevicemanagersourcegetmanager-method"></a>IMF dxgidevicemanagersource:: GetManager-Methode

Ruft den [**imsdxgidebug Manager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) aus der Microsoft Media Foundation Video Rendering-Senke ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetManager(
  [out] IMFDXGIDeviceManager **ppManager
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppManager* \[ vorgenommen\]
</dt> <dd>

Das [**IMF dxgidebug Manager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) -Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1 \[ Desktop-Apps \| UWP-apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                       |
| IDL<br/>                      | <dl> <dt>MFI. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMF-xgide vicemanagersource**](imfdxgidevicemanagersource.md)
</dt> </dl>

 

 




