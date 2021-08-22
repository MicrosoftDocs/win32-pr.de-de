---
title: INapComponentConfig2 IsRemoteConfigSupported-Methode (NapCommon.h)
description: Wird von System health validators (SHVs) implementiert, um anzugeben, ob die Remotekonfiguration unterstützt wird.
ms.assetid: c4b8e60b-ed60-49ec-b4d6-4e1575e4d1a5
keywords:
- IsRemoteConfigSupported-Methode NAP
- IsRemoteConfigSupported-Methode NAP, INapComponentConfig2-Schnittstelle
- INapComponentConfig2-Schnittstelle NAP, IsRemoteConfigSupported-Methode
topic_type:
- apiref
api_name:
- INapComponentConfig2.IsRemoteConfigSupported
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a42ae316063fc14054c8ffeb6e3987794bc33021441621ee231c9e839fc00248
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621767"
---
# <a name="inapcomponentconfig2isremoteconfigsupported-method"></a>INapComponentConfig2::IsRemoteConfigSupported-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **IsRemoteConfigSupported-Methode** wird von System health validators (SHVs) implementiert, um anzugeben, ob die Remotekonfiguration unterstützt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsRemoteConfigSupported(
  [out] BOOL  *isSupported,
  [out] UINT8 *remoteConfigType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*isSupported* \[ out\]
</dt> <dd>

Ein Zeiger auf eine BOOL, die auf **TRUE** festgelegt ist, wenn die Komponente die Remotekonfiguration unterstützt, und **FALSE,** wenn dies nicht der Fall ist.

</dd> <dt>

*remoteConfigType* \[ out\]
</dt> <dd>

Gibt den Typ der Remotekonfiguration an, die mit dem Wert der [**RemoteConfigurationType-Enumeration unterstützt**](/windows/win32/api/naptypes/ne-naptypes-remoteconfigurationtype) wird:



| Wert                                                                                                 | Bedeutung                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>remoteConfigTypeMachine</dt> </dl>    | [**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) ist implementiert.<br/>                                                                                                                                                                                                |
| <dl> <dt>remoteConfigTypeConfigBlob</dt> </dl> | [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) ist implementiert. [**INapComponentConfig::GetConfig**](inapcomponentconfig-getconfig.md) und [**INapComponentConfig::SetConfig**](inapcomponentconfig-setconfig.md) können remote über DCOM aufgerufen werden.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S OK zurück, wenn erfolgreich, oder einer der Windows \_ Standardfehlercodes.

## <a name="remarks"></a>Hinweise

Wenn weder [**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) noch [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) implementiert sind, ist die Remotekonfiguration der SHV nicht möglich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> </dl>

 

 





