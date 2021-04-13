---
title: Syncnamingcontext-Methode der MSAD_ReplNeighbor-Klasse
description: Ruft die dsreplicasync-Funktion auf, die einen Ziel namens Kontext mit einer seiner Quellen synchronisiert.
ms.assetid: 005053c4-8d9c-42f6-bae6-3ecdedd5ac2b
ms.tgt_platform: multiple
keywords:
- Syncnamingcontext-Methode Active Directory
- Syncnamingcontext-Methode Active Directory, MSAD_ReplNeighbor-Klasse
- MSAD_ReplNeighbor-Klasse Active Directory, syncnamingcontext-Methode
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
ms.openlocfilehash: 691bd3e943f491ba93d867097ac0167c97be6108
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478285"
---
# <a name="syncnamingcontext-method-of-the-msad_replneighbor-class"></a>Syncnamingcontext-Methode der MSAD \_ ReplNeighbor-Klasse

Ruft die [**dsreplicasync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca) -Funktion auf, die einen Ziel namens Kontext mit einer seiner Quellen synchronisiert.

## <a name="syntax"></a>Syntax


```mof
void SyncNamingContext(
  [in] uint32 Options
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Optionen* \[ in\]
</dt> <dd>

Zusätzliche Daten, die bestimmen, wie die-Methode die Anforderung verarbeitet. Dieser Parameter kann eine Kombination der folgenden Werte sein.

<dt>

<span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>

<span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>**DS \_ repsync \_ Verweis hinzufügen \_**


</dt> <dd>

Bewirkt, dass der Quellverzeichnis System-Agent (DSA) überprüft, ob das lokale DSA in der Liste Quell Replikate vorhanden ist. Wenn das lokale DSA nicht vorhanden ist, wird es hinzugefügt. Dadurch wird sichergestellt, dass die Quelle Änderungs Benachrichtigungen sendet.

</dd> <dt>

<span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>

<span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>**DS \_ repsync \_ alle \_ Quellen**


</dt> <dd>

Dieser Wert wird nicht unterstützt.

**Windows Server 2008 R2, Windows Server 2008 und Windows Server 2003:** Synchronisiert von allen Quellen.

</dd> <dt>

<span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>

<span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>**\_asynchroner DS repsync- \_ \_ Vorgang**


</dt> <dd>

Führt diesen Vorgang asynchron aus.

**Windows Server 2008 R2, Windows Server 2008 und Windows Server 2003:** Erforderlich, wenn " **DS \_ repsync \_ All \_**"-Quellen verwendet werden.

</dd> <dt>

<span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>

<span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>**DS \_ repsync- \_ Force**


</dt> <dd>

Wird synchronisiert, auch wenn der Link zurzeit deaktiviert ist.

</dd> <dt>

<span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>

<span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>**DS \_ repsync \_ voll**


</dt> <dd>

Wird beginnend mit der ersten Update Sequenznummer (Update Sequence Number, US) synchronisiert.

</dd> <dt>

<span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>

<span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>**DS \_ repsync- \_ standortübergreifende \_ Messaging**


</dt> <dd>

Wird mithilfe eines ISM synchronisiert.

</dd> <dt>

<span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>

<span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>**DS \_ repsync \_ nicht \_ verwerfen**


</dt> <dd>

Diese Synchronisierungs Anforderung wird von nicht verworfen, auch wenn eine ähnliche Synchronisierung aussteht.

</dd> <dt>

<span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>

<span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>**DS \_ repsync \_ periodisch**


</dt> <dd>

Gibt an, dass dieser Vorgang eine regelmäßige Synchronisierungs Anforderung ist, die vom Administrator geplant wird.

</dd> <dt>

<span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>

<span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>**DS \_ repsync ( \_ dringlich)**


</dt> <dd>

Gibt an, dass dieser Vorgang eine Benachrichtigung über ein Update ist, das als dringlich markiert ist.

</dd> <dt>

<span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>

<span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>**DS \_ repsync- \_ beschreibbares Element**


</dt> <dd>

Gibt an, dass dieses Replikat geschrieben werden kann. Wenn dieses Flag nicht festgelegt ist, ist das Replikat schreibgeschützt.

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

[**MSAD \_ ReplNeighbor**](msad-replneighbor.md)
</dt> </dl>

 

 





