---
description: Setzt die Prozesse des Pakets fort, wenn Sie zurzeit angehalten sind.
ms.assetid: c5376e00-b4b7-4a81-a84c-3a46758fe130
title: 'Ipackagedebugsettings:: Resume-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPackageDebugSettings.Resume
api_type:
- COM
api_location:
- Shobjidl.idl
ms.openlocfilehash: 2d36b11baffdc3f587924acd1732cbdfdb43d37f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344443"
---
# <a name="ipackagedebugsettingsresume-method"></a>Ipackagedebugsettings:: Resume-Methode

Setzt die Prozesse des Pakets fort, wenn Sie zurzeit angehalten sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT Resume(
  [in] LPCWSTR packageFullName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*packagefullname* \[ in\]
</dt> <dd>

Typ: **LPCWSTR**

Der vollständige Paketname.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Jeder Prozess empfängt das [**resuming**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) -Ereignis. Es kann nützlich sein, wenn Entwickler schrittweise durchlaufen, wie Ihre apps auf dieses Ereignis reagieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                          |
| IDL<br/>                      | <dl> <dt>Shobjidl. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ipackagedebugsettings**](/previous-versions//hh438393(v=vs.85))
</dt> </dl>

 

 
