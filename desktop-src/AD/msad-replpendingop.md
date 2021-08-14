---
title: MSAD_ReplPendingOp-Klasse
description: Stellt die DS \_ \_ REPL-OP-Struktur dar, die einen Replikationstask beschreibt, der gerade ausgeführt wird oder aussteht.
ms.assetid: d1c101fa-ae33-48da-9b00-93fde553a4f9
ms.tgt_platform: multiple
keywords:
- MSAD_ReplPendingOp Active Directory-Klasse
- MSAD_ReplPendingOp Active Directory-Klasse beschrieben
topic_type:
- apiref
api_name:
- MSAD_ReplPendingOp
- MSAD_ReplPendingOp.SerialNumber
- MSAD_ReplPendingOp.PositionInQ
- MSAD_ReplPendingOp.OpStartTime
- MSAD_ReplPendingOp.TimeEnqueued
- MSAD_ReplPendingOp.Priority
- MSAD_ReplPendingOp.OpType
- MSAD_ReplPendingOp.Options
- MSAD_ReplPendingOp.NamingContextDN
- MSAD_ReplPendingOp.NamingContextObjGuid
- MSAD_ReplPendingOp.DsaDN
- MSAD_ReplPendingOp.DsaAddress
- MSAD_ReplPendingOp.DsaObjGuid
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 164c5ebe672a52bb399727940e5e51b98904f7db322cc362425dabda25f547a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186075"
---
# <a name="msad_replpendingop-class"></a>MSAD \_ ReplPendingOp-Klasse

Stellt die [**DS \_ \_ REPL-OP-Struktur**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw) dar, die einen Replikationstask beschreibt, der gerade ausgeführt wird oder aussteht. Diese Struktur wird von der [**DsReplicaGetInfo-Funktion**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) zurückgegeben.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplPendingOp
{
  uint32   SerialNumber;
  uint32   PositionInQ;
  datetime OpStartTime;
  datetime TimeEnqueued;
  uint32   Priority;
  uint32   OpType;
  uint32   Options;
  String   NamingContextDN;
  String   NamingContextObjGuid;
  String   DsaDN;
  String   DsaAddress;
  String   DsaObjGuid;
};
```

## <a name="members"></a>Member

Die **MSAD \_ ReplPendingOp-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSAD \_ ReplPendingOp-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**DsaAddress**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft die transportspezifische Netzwerkadresse des Remoteservers ab, der diesem Vorgang zugeordnet ist. **NULL,** wenn diesem Vorgang kein Remoteserver zugeordnet ist.

</dd> <dt>

**DsaDN**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den X.500-Pfad des DSA ab, der dem Remoteserver zugeordnet ist, der diesem Vorgang entspricht. **NULL,** wenn diesem Vorgang kein Remoteserver entspricht.

</dd> <dt>

**DsaObjGuid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert des [**objectGuid-Attributs**](/windows/desktop/ADSchema/a-objectguid) des DSA ab, das durch die **DsaDN-Eigenschaft** identifiziert wird.

</dd> <dt>

**NamingContextDN**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den X.500-Pfad des Namenskontexts (NC) ab, der diesem Vorgang zugeordnet ist.

</dd> <dt>

**NamingContextObjGuid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft das [**objectGuid-Attribut**](/windows/desktop/ADSchema/a-objectguid) des NC ab, das durch die **NamingContextDN-Eigenschaft** identifiziert wird.

</dd> <dt>

**OpStartTime**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft die Uhrzeit ab, zu der der Vorgang gestartet wurde. **NULL,** wenn sich dieser Vorgang noch in der Warteschlange befindet.

</dd> <dt>

**Optionen**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Satz von Flags ab, die zusätzliche Daten über den Vorgang bereitstellt. Der Inhalt dieses Members wird durch den Wert der **OpType-Eigenschaft** bestimmt.

<dt>

<span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>

<span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>**DS \_ REPL \_ OP \_ TYPE \_ SYNC**


</dt> <dd>

Enthält 0 (null) oder eine Kombination aus einem oder mehreren **DS \_ REPSYNC \_ \** _-Werten, wie für den parameter _Options* in [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca)definiert.

</dd> <dt>

<span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>

<span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>**DS \_ REPL \_ OP \_ TYPE \_ ADD**


</dt> <dd>

Enthält 0 (null) oder eine Kombination aus einem oder mehreren **DS \_ REPADD \_ \** _-Werten, wie für den _Options*-Parameter in [**DsReplicaAdd**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda)definiert.

</dd> <dt>

<span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>

<span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>**DS \_ REPL \_ OP \_ TYPE \_ DELETE**


</dt> <dd>

Enthält 0 (null) oder eine Kombination aus einem oder mehreren **DS \_ \_ \* REPDEL* _-Werten, wie für den parameter _Options* in [**DsReplicaDel**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela)definiert.

</dd> <dt>

<span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>

<span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>**DS \_ REPL \_ OP \_ TYPE \_ MODIFY**


</dt> <dd>

Enthält 0 (null) oder eine Kombination aus einem oder mehreren **DS \_ \_ \* REPMOD* _-Werten, wie für den parameter _Options* in [**DsReplicaModify**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya)definiert.

</dd> <dt>

<span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>

<span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>**DS \_ REPL \_ OP \_ TYPE \_ UPDATE \_ REFS**


</dt> <dd>

Enthält null oder eine Kombination aus einem oder mehreren **DS \_ \_ \* REPSUPD* _-Werten, wie für den _Options*-Parameter in [**DsReplicaUpdateRefs**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa)definiert.

</dd> </dl>

</dd> <dt>

**OpType**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den [**DS \_ REPL \_ OP \_ TYPE-Wert**](/windows/desktop/api/Ntdsapi/ne-ntdsapi-ds_repl_op_type) ab, der den Typ des Vorgangs angibt, den diese Klasse darstellt.

</dd> <dt>

**PositionInQ**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft die Position dieses Vorgangs in der Warteschlange ab.

</dd> <dt>

**Priority**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft die Priorität dieses Vorgangs ab. Aufgaben mit höherer Priorität werden zuerst ausgeführt. Die Priorität wird vom Server basierend auf dem Vorgangstyp, den diese Klasse darstellt, und den Parametern des Vorgangs berechnet.

</dd> <dt>

**Serialnumber**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ruft die ID des Vorgangs ab, der pro Computer und pro Start eindeutig ist.

</dd> <dt>

**TimeEnqueued**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Zeitpunkt ab, zu dem dieser Vorgang der Warteschlange hinzugefügt wurde.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\MicrosoftActiveDirectory-Stammverzeichnis<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



 

