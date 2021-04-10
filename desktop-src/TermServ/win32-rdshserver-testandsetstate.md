---
title: Testandsetstate-Methode der Win32_RDSHServer-Klasse
description: Vergleicht den aktuellen Zustand mit dem angegebenen comparand. Wenn die beiden Stimmen, wird der Zustand auf einen neuen Wert festgelegt. Unabhängig von der Übereinstimmung wird der aktuelle Zustand ebenfalls zurückgegeben.
ms.assetid: f1bb0076-251b-4c0d-92f9-1c460e1b26bb
ms.tgt_platform: multiple
keywords:
- Testandsetstate-Methode Remotedesktopdienste
- Testandsetstate-Methode Remotedesktopdienste, Win32_RDSHServer-Klasse
- Win32_RDSHServer-Klasse Remotedesktopdienste, testandsetstate-Methode
topic_type:
- apiref
api_name:
- Win32_RDSHServer.TestAndSetState
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ff4c9b616c2a288f5f39b240d71b2611e25d45f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103983"
---
# <a name="testandsetstate-method-of-the-win32_rdshserver-class"></a>Testandsetstate-Methode der Win32 \_ rdshserver-Klasse

Vergleicht den aktuellen Zustand mit dem angegebenen comparand. Wenn die beiden Stimmen, wird der Zustand auf einen neuen Wert festgelegt. Unabhängig von der Übereinstimmung wird der aktuelle Zustand ebenfalls zurückgegeben.

## <a name="syntax"></a>Syntax


```mof
uint32 TestAndSetState(
  [in]  uint32 Comparand,
  [in]  uint32 NewState,
  [out] uint32 InitState
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Comparand* \[ in\]
</dt> <dd>

Ein Wert, der mit dem aktuellen Zustand verglichen werden soll. Wenn die beiden Werte stimmen, wird der Zustand auf *newState* festgelegt.

</dd> <dt>

*NewState* \[ in\]
</dt> <dd>

Der neue Wert des Zustands.

</dd> <dt>

*Initstate* \[ vorgenommen\]
</dt> <dd>

Bei Erfolg oder Fehler gibt den aktuellen Status zurück.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                              |
| Namespace<br/>                | Root \\ CIMV2 \\ RDMs<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Rdmanagement. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ rdshserver**](win32-rdshserver.md)
</dt> </dl>

 

 





