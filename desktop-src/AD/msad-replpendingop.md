---
title: MSAD_ReplPendingOp-Klasse
description: Stellt die DS- \_ repl- \_ op-Struktur dar, die eine Replikations Aufgabe beschreibt, die gerade ausgeführt wird oder deren Ausführung aussteht
ms.assetid: d1c101fa-ae33-48da-9b00-93fde553a4f9
ms.tgt_platform: multiple
keywords:
- MSAD_ReplPendingOp-Klasse Active Directory
- MSAD_ReplPendingOp Klasse Active Directory, beschrieben
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
ms.openlocfilehash: 0f1c3faddac915f602104d7e5dc4e9b6bc7d6944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391923"
---
# <a name="msad_replpendingop-class"></a>MSAD \_ replpdingop-Klasse

Stellt die [**DS- \_ repl- \_ op**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw) -Struktur dar, die eine Replikations Aufgabe beschreibt, die gerade ausgeführt wird oder deren Ausführung aussteht Diese Struktur wird von der [**dsreplicagetinfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) -Funktion zurückgegeben.

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

Die **MSAD \_ replpdingop** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSAD \_ replpdingop** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Dsaaddress**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft die Transport spezifische Netzwerkadresse des Remote Servers ab, der diesem Vorgang zugeordnet ist. **Null** , wenn kein Remote Server vorhanden ist, der diesem Vorgang zugeordnet ist.

</dd> <dt>

**Dsadn**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den X. 500-Pfad des DSA ab, der dem Remote Server zugeordnet ist, der diesem Vorgang entspricht. **Null** , wenn kein Remote Server diesem Vorgang entspricht.

</dd> <dt>

**Dsaobjguid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert des [**objectGUID**](/windows/desktop/ADSchema/a-objectguid) -Attributs des DSA ab, das durch die **dsadn** -Eigenschaft identifiziert wird.

</dd> <dt>

**Namingcontextdn**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den X. 500-Pfad des Namens Kontexts (NC) ab, der diesem Vorgang zugeordnet ist.

</dd> <dt>

**Namingcontextobjguid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft das [**objectGUID**](/windows/desktop/ADSchema/a-objectguid) -Attribut des NC ab, das durch die **namingcontextdn** -Eigenschaft identifiziert wird.

</dd> <dt>

**Opstarttime**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft die Zeit ab, zu der der Vorgang gestartet wurde. **Null** , wenn sich dieser Vorgang noch in der Warteschlange befindet.

</dd> <dt>

**Optionen**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Satz von Flags ab, der zusätzliche Daten über den Vorgang bereitstellt. Der Inhalt dieses Elements wird durch den Wert der **optype** -Eigenschaft bestimmt.

<dt>

<span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>

<span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>**DS \_ repl- \_ op- \_ \_ typsynchronisierung**


</dt> <dd>

Enthält 0 (null) oder eine Kombination aus einem oder mehreren der **DS \_ \_ \* repsync* _-Werte, wie für den _Options *-Parameter in [**dsreplicasync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca)definiert.

</dd> <dt>

<span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>

<span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>**DS \_ repl \_ op- \_ Typ \_ Hinzufügen**


</dt> <dd>

Enthält 0 (null) oder eine Kombination aus einem oder mehreren der **DS \_ \_ \**-Werte, die für den Parameter "_Options *" in " [**dsreplicaadd**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda)" definiert sind.

</dd> <dt>

<span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>

<span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>**DS \_ repl- \_ op- \_ Typ \_ Löschen**


</dt> <dd>

Enthält 0 (null) oder eine Kombination aus einem oder mehreren der **DS- \_ \_ \* repdel* _-Werte, wie für den _Options *-Parameter in [**dsreplicadel**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela)definiert.

</dd> <dt>

<span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>

<span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>**DS \_ repl- \_ op- \_ \_ Typänderung**


</dt> <dd>

Enthält 0 (null) oder eine Kombination aus einem oder mehreren der **DS- \_ repmod \_ \** _-Werte, wie für den _Options *-Parameter in [**dsreplicamodify**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya)definiert.

</dd> <dt>

<span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>

<span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>**DS \_ repl \_ - \_ \_ typupdate- \_ Refs**


</dt> <dd>

Enthält 0 (null) oder eine Kombination aus einem oder mehreren der **DS- \_ \_ \* repsupd* _-Werte, wie für den Parameter "_Options *" in [**dsreplicaupdaterefs**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa)definiert.

</dd> </dl>

</dd> <dt>

**OpType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert des [**DS- \_ repl- \_ op- \_ Typs**](/windows/desktop/api/Ntdsapi/ne-ntdsapi-ds_repl_op_type) ab, der den Typ des Vorgangs angibt, den diese Klasse darstellt.

</dd> <dt>

**Positioninq**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft die Position dieses Vorgangs in der Warteschlange ab.

</dd> <dt>

**Priority**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft die Priorität dieses Vorgangs ab. Aufgaben mit höherer Priorität werden zuerst ausgeführt. Die Priorität wird vom Server basierend auf dem Typ des Vorgangs, der von dieser Klasse dargestellt wird, und den Parametern des Vorgangs berechnet.

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ruft die ID des Vorgangs ab, der pro Computer und pro Start eindeutig ist.

</dd> <dt>

**Zeit in Warteschlange eingereiht**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
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
| Namespace<br/>                | \\Microsoftactivedirectory-Stammverzeichnis<br/>                                               |
| MOF<br/>                      | <dl> <dt>ReplProv. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



 

