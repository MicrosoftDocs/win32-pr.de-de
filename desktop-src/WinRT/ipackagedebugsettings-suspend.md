---
description: Hält die Prozesse des Pakets an, wenn Sie derzeit ausgeführt werden.
ms.assetid: 83f44285-46ed-4968-b0af-7964dfacf602
title: 'Ipackagedebugsettings:: Suspend-Methode'
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
ms.openlocfilehash: 385ddc856661090caec4345df6651605b67fe883
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751496"
---
# <a name="ipackagedebugsettingssuspend-method"></a>Ipackagedebugsettings:: Suspend-Methode

Hält die Prozesse des Pakets an, wenn Sie derzeit ausgeführt werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT Suspend(
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

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                            | Beschreibung                                      |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Der Vorgang wurde erfolgreich ausgeführt.<br/>              |
| <dl> <dt>**E ungültige \_ \_ StateChange**</dt> </dl> | Der Prozess wird zurzeit nicht ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Jeder Prozess empfängt das [**Suspensions**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) Ereignis. Es kann nützlich sein, wenn Entwickler schrittweise durchlaufen, wie Ihre apps auf dieses Ereignis reagieren.

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

 

 
