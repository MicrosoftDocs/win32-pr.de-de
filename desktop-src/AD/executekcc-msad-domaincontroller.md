---
title: ExecuteKCC-Methode der MSAD_DomainController-Klasse
description: Ruft die DsReplicaConsistencyCheck-Funktion auf, die die Wissenskonsistenzprüfung (Knowledge Consistency Checker, KCC) aufruft, um die Replikationstopologie zu überprüfen.
ms.assetid: 958c9a15-cde2-4c74-bd4c-c2d53551cfb0
ms.tgt_platform: multiple
keywords:
- ExecuteKCC-Methode Active Directory
- ExecuteKCC-Methode Active Directory , MSAD_DomainController Klasse
- MSAD_DomainController Active Directory- und ExecuteKCC-Methode
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
ms.openlocfilehash: 48295638f105b79ea24a55965ca3ec75ee0ad6b9982c74664f8bfecdd0681cfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189618"
---
# <a name="executekcc-method-of-the-msad_domaincontroller-class"></a>ExecuteKCC-Methode der MSAD \_ DomainController-Klasse

Ruft die [**DsReplicaConsistencyCheck-Funktion**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaconsistencycheck) auf, die die Wissenskonsistenzprüfung (Knowledge Consistency Checker, KCC) aufruft, um die Replikationstopologie zu überprüfen.

## <a name="syntax"></a>Syntax


```mof
void ExecuteKCC(
  [in] uint32 TaskID,
  [in] uint32 dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*TaskID* \[ In\]
</dt> <dd>

Die Aufgabe, die der KCC ausführen soll. **DS \_ KCC \_ TASKID \_ UPDATE \_ TOPOLOGY** ist der einzige Wert, der derzeit unterstützt wird.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Ein Satz von Flags, die das Verhalten der **ExecuteKCC-Methode** ändern. Dieser Parameter kann 0 (null) oder eine Kombination aus mindestens einem der folgenden Werte sein.

<dt>

<span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>

<span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>**DS \_ KCC \_ FLAG \_ ASYNC \_ OP**


</dt> <dd>

Die Aufgabe wird in die Warteschlange gestellt, und die Funktion kehrt dann zurück, ohne auf den Abschluss der Aufgabe zu warten.

</dd> <dt>

<span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>

<span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>**\_DS-KCC-FLAG \_ \_ GEERBT**


</dt> <dd>

Die Aufgabe wird der Warteschlange nicht hinzugefügt, wenn bald eine andere Aufgabe in der Warteschlange ausgeführt wird.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ MicrosoftActiveDirectory<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MSAD \_ DomainController**](msad-domaincontroller.md)
</dt> </dl>

 

 





