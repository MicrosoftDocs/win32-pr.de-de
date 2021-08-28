---
title: ITSRemoteProgram RemoteProgramMode (Eigenschaft)
description: Der Windows Server 2008 R2 RemoteApp-Modus.
ms.assetid: 9ebdf966-db9c-4a14-8469-f8b153c6ea78
ms.tgt_platform: multiple
keywords:
- RemoteProgramMode-Remotedesktopdienste
- RemoteProgramMode-Eigenschaft Remotedesktopdienste , ITSRemoteProgram-Schnittstelle
- ITSRemoteProgram-Schnittstelle Remotedesktopdienste , RemoteProgramMode-Eigenschaft
- RemoteProgramMode-Eigenschaft Remotedesktopdienste , ITSRemoteProgram2-Schnittstelle
- ITSRemoteProgram2-Schnittstelle Remotedesktopdienste , RemoteProgramMode-Eigenschaft
- RemoteProgramMode-Eigenschaft Remotedesktopdienste , ITSRemoteProgram3-Schnittstelle
- ITSRemoteProgram3-Schnittstelle Remotedesktopdienste , RemoteProgramMode-Eigenschaft
topic_type:
- apiref
api_name:
- ITSRemoteProgram.RemoteProgramMode
- ITSRemoteProgram.get_RemoteProgramMode
- ITSRemoteProgram.put_RemoteProgramMode
- ITSRemoteProgram2.RemoteProgramMode
- ITSRemoteProgram2.get_RemoteProgramMode
- ITSRemoteProgram2.put_RemoteProgramMode
- ITSRemoteProgram3.RemoteProgramMode
- ITSRemoteProgram3.get_RemoteProgramMode
- ITSRemoteProgram3.put_RemoteProgramMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c36f450e6cbfec3922a56a42bc2f1f61466774eeff46c0987b6fad4ca9dc9731
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124820"
---
# <a name="itsremoteprogramremoteprogrammode-property"></a>ITSRemoteProgram::RemoteProgramMode (Eigenschaft)

Der Windows Server 2008 R2 RemoteApp-Modus.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_RemoteProgramMode(
  [in]  VARIANT_BOOL vboolRemoteProgramMode
);

HRESULT get_RemoteProgramMode(
  [out] VARIANT_BOOL *pvboolRemoteProgramMode
);
```



## <a name="property-value"></a>Eigenschaftswert

Der RemoteApp-Modus. Wenn variant **\_ true festgelegt ist,** ist der RemoteApp-Modus aktiviert, und die Remotesitzung hosten RemoteApp-Programme. Wenn die **Standardeinstellung VARIANT \_ FALSE** festgelegt ist, ist der RemoteApp-Modus nicht aktiviert. Die Remotesitzung hosten einen Remotedesktop.

## <a name="error-codes"></a>Fehlercodes

Gibt **S \_ OK zurück,** wenn erfolgreich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ ITSRemoteProgram ist als FDD029F9-467A-4c49-8529-64B521DBD1B4 definiert.<br/>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITSRemoteProgram2**](itsremoteprogram2.md)
</dt> <dt>

[**ITSRemoteProgram3**](itsremoteprogram3.md)
</dt> <dt>

[**ITSRemoteProgram**](itsremoteprogram.md)
</dt> </dl>

 

 





