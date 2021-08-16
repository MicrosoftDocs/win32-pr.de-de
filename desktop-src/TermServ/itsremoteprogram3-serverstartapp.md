---
title: ITSRemoteProgram3 ServerStartApp-Methode
description: Gibt eine App an, die in der Remotesitzung gestartet werden soll.
ms.assetid: 55a05d05-66d5-48a1-b3a6-f087aeb62925
ms.tgt_platform: multiple
keywords:
- ServerStartApp-Methode Remotedesktopdienste
- ServerStartApp-Methode Remotedesktopdienste , ITSRemoteProgram3-Schnittstelle
- ITSRemoteProgram3-Schnittstelle Remotedesktopdienste , ServerStartApp-Methode
topic_type:
- apiref
api_name:
- ITSRemoteProgram3.ServerStartApp
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e162f220c59f8dfaca1d1f5666fb691ca02b8f53b5fcfe0476bf188d55b25d6e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072230"
---
# <a name="itsremoteprogram3serverstartapp-method"></a>ITSRemoteProgram3::ServerStartApp-Methode

Gibt eine App an, die in der Remotesitzung gestartet werden soll.

## <a name="syntax"></a>Syntax


```C++
HRESULT ServerStartApp(
  [in] BSTR         bstrAppUserModelId,
  [in] BSTR         bstrArguments,
  [in] VARIANT_BOOL vbExpandEnvVarInArgumentsOnServer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrAppUserModelId* \[ In\]
</dt> <dd></dd> <dt>

*bstrArguments* \[ In\]
</dt> <dd></dd> <dt>

*vbExpandEnvVarInArgumentsOnServer* \[ In\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITSRemoteProgram3**](itsremoteprogram3.md)
</dt> </dl>

 

 





