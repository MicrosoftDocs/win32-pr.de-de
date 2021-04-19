---
title: "\"Itsremoteprogram\"-remoteprogrammode-Eigenschaft"
description: Der RemoteApp-Modus von Windows Server 2008 R2.
ms.assetid: 9ebdf966-db9c-4a14-8469-f8b153c6ea78
ms.tgt_platform: multiple
keywords:
- Remoteprogrammode-Eigenschaft Remotedesktopdienste
- Remoteprogrammode-Eigenschaft Remotedesktopdienste, itsremoteprogram-Schnittstelle
- Itsremoteprogram-Schnittstelle Remotedesktopdienste, remoteprogrammode-Eigenschaft
- Remoteprogrammode-Eigenschaft Remotedesktopdienste, ITSRemoteProgram2-Schnittstelle
- ITSRemoteProgram2 Interface Remotedesktopdienste, remoteprogrammode-Eigenschaft
- Remoteprogrammode-Eigenschaft Remotedesktopdienste, ITSRemoteProgram3-Schnittstelle
- ITSRemoteProgram3 Interface Remotedesktopdienste, remoteprogrammode-Eigenschaft
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
ms.openlocfilehash: e8582824e2f6349e37b125ffd974847b602ad6fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337525"
---
# <a name="itsremoteprogramremoteprogrammode-property"></a>Itsremoteprogram:: remoteprogrammode-Eigenschaft

Der RemoteApp-Modus von Windows Server 2008 R2.

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

Der RemoteApp-Modus. Wenn der Wert auf **Variant \_ true** festgelegt ist, wird der RemoteApp-Modus aktiviert, und die Remote Sitzung hostet RemoteApp-Programme. Wenn der Wert auf **Variant \_ false** (Standardeinstellung) festgelegt ist, ist der RemoteApp-Modus nicht aktiviert. Die Remote Sitzung hostet einen Remote Desktop.

## <a name="error-codes"></a>Fehlercodes

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ itsremoteprogram ist als FDD029F9-467A-4c49-8529-64B521DBD1B4 definiert.<br/>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITSRemoteProgram2**](itsremoteprogram2.md)
</dt> <dt>

[**ITSRemoteProgram3**](itsremoteprogram3.md)
</dt> <dt>

[**Itsremoteprogram**](itsremoteprogram.md)
</dt> </dl>

 

 





