---
title: Executekcc-Methode der MSAD_DomainController-Klasse
description: Ruft die DsReplicaConsistencyCheck-Funktion auf, die die Konsistenzprüfung (KCC) zum Überprüfen der Replikations Topologie aufruft.
ms.assetid: 958c9a15-cde2-4c74-bd4c-c2d53551cfb0
ms.tgt_platform: multiple
keywords:
- Executekcc-Methode Active Directory
- Executekcc-Methode Active Directory, MSAD_DomainController-Klasse
- MSAD_DomainController-Klasse Active Directory, executekcc-Methode
topic_type:
- apiref
api_name:
- MSAD_DomainController.ExecuteKCC
api_location:
- replprov.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcce017f86042181d2e80ae3614e3fc1cbccc676
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342841"
---
# <a name="executekcc-method-of-the-msad_domaincontroller-class"></a>Executekcc-Methode der MSAD \_ Domain Controller-Klasse

Ruft die [**DsReplicaConsistencyCheck**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaconsistencycheck) -Funktion auf, die die Konsistenzprüfung (KCC) zum Überprüfen der Replikations Topologie aufruft.

## <a name="syntax"></a>Syntax


```mof
void ExecuteKCC(
  [in] uint32 TaskID,
  [in] uint32 dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*TaskID* \[ in\]
</dt> <dd>

Der Task, der von der KCC ausgeführt werden soll. **DS \_ Die KCC \_ TaskID- \_ Update \_ Topologie** ist der einzige Wert, der derzeit unterstützt wird.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Ein Satz von Flags, die das Verhalten der **executekcc** -Methode ändern. Dieser Parameter kann NULL sein oder eine Kombination aus einem oder mehreren der folgenden Werte aufweisen.

<dt>

<span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>

<span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>**DS- \_ KCC- \_ Flag \_ Async \_ op**


</dt> <dd>

Der Task wird in die Warteschlange eingereiht, und die Funktion wird zurückgegeben, ohne auf den Abschluss der Aufgabe zu warten

</dd> <dt>

<span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>

<span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>**DS- \_ KCC- \_ Flag \_ gedämpft**


</dt> <dd>

Der Task wird der Warteschlange nicht hinzugefügt, wenn ein anderer Task in der Warteschlange bald ausgeführt wird.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Microsoftactivedirectory-Stammverzeichnis<br/>                                               |
| MOF<br/>                      | <dl> <dt>ReplProv. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSAD \_ Domain Controller**](msad-domaincontroller.md)
</dt> </dl>

 

 





