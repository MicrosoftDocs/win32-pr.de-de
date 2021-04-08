---
title: INapComponentConfig2 isremoteconfigsupported-Methode (napcommon. h)
description: Wird von System Integritätsprüfungen (SHVs) implementiert, um anzugeben, ob die Remote Konfiguration unterstützt wird.
ms.assetid: c4b8e60b-ed60-49ec-b4d6-4e1575e4d1a5
keywords:
- Isremoteconfigsupported-Methode NAP
- Isremoteconfigsupported-Methode, NAP, INapComponentConfig2-Schnittstelle
- INapComponentConfig2 Interface NAP, isremoteconfigsupported-Methode
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
ms.openlocfilehash: a2d144926aafff6f5ad7e243efe2a81a2955f497
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949673"
---
# <a name="inapcomponentconfig2isremoteconfigsupported-method"></a>INapComponentConfig2:: isremoteconfigsupported-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **isremoteconfigsupported** -Methode wird von System Integritätsprüfungen (SHVs) implementiert, um anzugeben, ob die Remote Konfiguration unterstützt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsRemoteConfigSupported(
  [out] BOOL  *isSupported,
  [out] UINT8 *remoteConfigType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IsSupported* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen booleschen Wert, der auf **true** festgelegt ist, wenn die Komponente die Remote Konfiguration unterstützt, andernfalls **false** .

</dd> <dt>

*remoteconfigtype* \[ vorgenommen\]
</dt> <dd>

Gibt den Typ der Remote Konfiguration an, der mit dem Wert aus der [**remoteconfigurationtype**](/windows/win32/api/naptypes/ne-naptypes-remoteconfigurationtype) -Enumeration unterstützt wird:



| Wert                                                                                                 | Bedeutung                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>remoteconfigtypemachine</dt> </dl>    | [**Invokeuiformachine**](inapcomponentconfig2-invokeuiformachine.md) ist implementiert.<br/>                                                                                                                                                                                                |
| <dl> <dt>remoteconfigtypeconfigblob</dt> </dl> | [**Invokeuifromconfigblob**](inapcomponentconfig2-invokeuifromconfigblob.md) ist implementiert. [**Inapcomponentconfig:: GetConfig**](inapcomponentconfig-getconfig.md) und [**inapcomponentconfig:: setconfig**](inapcomponentconfig-setconfig.md) können mithilfe von DCOM Remote aufgerufen werden.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK oder einen der standardmäßigen Windows-Fehlercodes zurück.

## <a name="remarks"></a>Bemerkungen

Wenn weder [**invokeuiformachine**](inapcomponentconfig2-invokeuiformachine.md) noch [**invokeuifromconfigblob**](inapcomponentconfig2-invokeuifromconfigblob.md) implementiert ist, ist die Remote Konfiguration des SHV nicht möglich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Napcommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napcommon. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> </dl>

 

 





