---
description: Setzt die Prozesse des Pakets an, wenn sie gerade ausgeführt werden.
ms.assetid: 83f44285-46ed-4968-b0af-7964dfacf602
title: IPackageDebugSettings::Suspend-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPackageDebugSettings.Suspend
api_type:
- COM
api_location:
- Shobjidl.idl
ms.openlocfilehash: 0517ce3cca6a8e74f19b053897511062cefa252297d3a0e6633d4678c0deaa95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118822813"
---
# <a name="ipackagedebugsettingssuspend-method"></a>IPackageDebugSettings::Suspend-Methode

Setzt die Prozesse des Pakets an, wenn sie gerade ausgeführt werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT Suspend(
  [in] LPCWSTR packageFullName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*packageFullName* \[ In\]
</dt> <dd>

Typ: **LPCWSTR**

Der vollständige Paketname.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                            | Beschreibung                                      |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Der Vorgang wurde erfolgreich ausgeführt.<br/>              |
| <dl> <dt>**E \_ ILLEGAL \_ STATECHANGE**</dt> </dl> | Der Prozess wird derzeit nicht ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Jeder Prozess empfängt das [**Suspending-Ereignis.**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) Es kann für Entwickler nützlich sein, schritt für Schritt zu erfahren, wie ihre Apps auf dieses Ereignis reagieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                          |
| Idl<br/>                      | <dl> <dt>Shobjidl.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))
</dt> </dl>

 

 
