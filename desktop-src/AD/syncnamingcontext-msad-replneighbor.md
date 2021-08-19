---
title: SyncNamingContext-Methode der MSAD_ReplNeighbor-Klasse
description: Ruft die DsReplicaSync-Funktion auf, die einen Zielbenennungskontext mit einer ihrer Quellen synchronisiert.
ms.assetid: 005053c4-8d9c-42f6-bae6-3ecdedd5ac2b
ms.tgt_platform: multiple
keywords:
- SyncNamingContext-Methode Active Directory
- SyncNamingContext-Methode Active Directory , MSAD_ReplNeighbor-Klasse
- MSAD_ReplNeighbor Active Directory-Klasse, SyncNamingContext-Methode
topic_type:
- apiref
api_name:
- MSAD_ReplNeighbor.SyncNamingContext
api_location:
- replprov.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b96dd7363b5c2a48a6c25826d8c2752c181bc9125955b6c73d5532eb2665514
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024668"
---
# <a name="syncnamingcontext-method-of-the-msad_replneighbor-class"></a>SyncNamingContext-Methode der MSAD \_ ReplNeighbor-Klasse

Ruft die [**DsReplicaSync-Funktion**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca) auf, die einen Zielbenennungskontext mit einer ihrer Quellen synchronisiert.

## <a name="syntax"></a>Syntax


```mof
void SyncNamingContext(
  [in] uint32 Options
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Optionen* \[ In\]
</dt> <dd>

Zusätzliche Daten, die bestimmen, wie die Methode die Anforderung verarbeitet. Dieser Parameter kann eine Kombination der folgenden Werte sein.

<dt>

<span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>

<span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>**DS \_ REPSYNC \_ ADD \_ REFERENCE**


</dt> <dd>

Bewirkt, dass der Quellverzeichnissystem-Agent (DSA) überprüft, ob der lokale DSA in der Liste der Quellreplikationen vorhanden ist. Wenn die lokale DSA nicht vorhanden ist, wird sie hinzugefügt. Dadurch wird sichergestellt, dass die Quelle Änderungsbenachrichtigungen sendet.

</dd> <dt>

<span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>

<span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>**DS \_ REPSYNC \_ ALL \_ SOURCES**


</dt> <dd>

Dieser Wert wird nicht unterstützt.

**Windows Server 2008 R2, Windows Server 2008 und Windows Server 2003:** Synchronisiert aus allen Quellen.

</dd> <dt>

<span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>

<span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>**\_ \_ ASYNCHRONER DS-REPSYNC-VORGANG \_**


</dt> <dd>

Führt diesen Vorgang asynchron aus.

**Windows Server 2008 R2, Windows Server 2008 und Windows Server 2003:** Erforderlich, wenn **DS \_ REPSYNC \_ ALL \_ SOURCES** verwendet wird.

</dd> <dt>

<span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>

<span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>**DS \_ REPSYNC \_ FORCE**


</dt> <dd>

Wird auch dann synchronisiert, wenn der Link derzeit deaktiviert ist.

</dd> <dt>

<span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>

<span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>**DS \_ REPSYNC \_ FULL**


</dt> <dd>

Synchronisiert ab der ersten Updatesequenznummer (USN).

</dd> <dt>

<span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>

<span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>**DS \_ REPSYNC \_ INTERSITE \_ MESSAGING**


</dt> <dd>

Synchronisiert mithilfe eines ISM.

</dd> <dt>

<span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>

<span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>**DS \_ REPSYNC \_ NO \_ DISCARD**


</dt> <dd>

Diese Synchronisierungsanforderung wird auch dann nicht verworfen, wenn eine ähnliche Synchronisierung aussteht.

</dd> <dt>

<span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>

<span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>**DS \_ REPSYNC \_ PERIODIC**


</dt> <dd>

Gibt an, dass es sich bei diesem Vorgang um eine vom Administrator geplante regelmäßige Synchronisierungsanforderung handelt.

</dd> <dt>

<span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>

<span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>**DS \_ REPSYNC \_ DRINGEND**


</dt> <dd>

Gibt an, dass dieser Vorgang eine Benachrichtigung über ein Update ist, das als dringend markiert ist.

</dd> <dt>

<span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>

<span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>**DS \_ REPSYNC \_ WRITEABLE**


</dt> <dd>

Gibt an, dass dieses Replikat beschreibbar ist. Wenn dieses Flag nicht festgelegt ist, ist das Replikat schreibgeschützt.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\MicrosoftActiveDirectory-Stammverzeichnis<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MSAD \_ ReplNeighbor**](msad-replneighbor.md)
</dt> </dl>

 

 





