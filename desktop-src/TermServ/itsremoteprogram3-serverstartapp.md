---
title: ITSRemoteProgram3 serverstartapp-Methode
description: Gibt eine APP an, die in der Remote Sitzung gestartet werden soll.
ms.assetid: 55a05d05-66d5-48a1-b3a6-f087aeb62925
ms.tgt_platform: multiple
keywords:
- Serverstartapp-Methode Remotedesktopdienste
- Serverstartapp-Methode Remotedesktopdienste, ITSRemoteProgram3-Schnittstelle
- ITSRemoteProgram3 Interface Remotedesktopdienste, serverstartapp-Methode
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
ms.openlocfilehash: ef1822fa98094870ebebe607528cdc69a8a201f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343881"
---
# <a name="itsremoteprogram3serverstartapp-method"></a>ITSRemoteProgram3:: serverstartapp-Methode

Gibt eine APP an, die in der Remote Sitzung gestartet werden soll.

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

*bstrappusermodelid* \[ in\]
</dt> <dd></dd> <dt>

*bstrauarguments* \[ in\]
</dt> <dd></dd> <dt>

*vbexpandeinvvarinargumentsonserver* \[ in\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITSRemoteProgram3**](itsremoteprogram3.md)
</dt> </dl>

 

 





