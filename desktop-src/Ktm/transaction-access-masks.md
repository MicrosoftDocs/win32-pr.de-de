---
description: BEI werden die folgenden Transaktionszugriffsmasken definiert, die beim Öffnen einer Transaktion verwendet werden sollen.
ms.assetid: 93ef3098-b3cc-4b24-ae82-1c10d937f14f
title: Transaktionszugriffsmasken (WinNT.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faafcce45944e37418191254fc5a2b81d00d9248b27ea5e8753fe8e34a734754
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520640"
---
# <a name="transaction-access-masks"></a>Transaktionszugriffsmasken

BEI werden die folgenden Transaktionszugriffsmasken definiert, die beim Öffnen einer Transaktion verwendet werden sollen.

<dl> <dt>

<span id="TRANSACTION_QUERY_INFORMATION"></span><span id="transaction_query_information"></span>**\_ \_ TRANSAKTIONSABFRAGEINFORMATIONEN**
</dt> <dd> <dl> <dt>

0x000001
</dt> <dt>



Der Aufrufer kann Transaktionsinformationen abfragen.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_SET_INFORMATION"></span><span id="transaction_set_information"></span>**\_ \_ TRANSAKTIONSSATZINFORMATIONEN**
</dt> <dd> <dl> <dt>

0x000002
</dt> <dt>



Der Aufrufer kann Transaktionsinformationen festlegen.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_ENLIST"></span><span id="transaction_enlist"></span>**TRANSACTION \_ ENLIST**
</dt> <dd> <dl> <dt>

0x000004
</dt> <dt>



Der Aufrufer kann sich in diese Transaktion eintragen.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_COMMIT"></span><span id="transaction_commit"></span>**\_TRANSAKTIONSCOMMIT**
</dt> <dd> <dl> <dt>

0x000008
</dt> <dt>



Der Aufrufer kann für diese Transaktion einen Commit durchführen.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_ROLLBACK"></span><span id="transaction_rollback"></span>**\_TRANSAKTIONSROLLBACK**
</dt> <dd> <dl> <dt>

0x000010
</dt> <dt>



Der Aufrufer kann ein Rollback für diese Transaktion durchführen.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_PROPAGATE"></span><span id="transaction_propagate"></span>**TRANSACTION \_ PROPAGATE**
</dt> <dd> <dl> <dt>

0x000020
</dt> <dt>



Der Aufrufer kann diese Transaktion an einen übergeordneten Ressourcen-Manager, z. B. den Distributed Transaction Coordinator (DTC), weiterspähen.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_GENERIC_READ"></span><span id="transaction_generic_read"></span>**GENERISCHER \_ \_ TRANSAKTIONSLESEVORGANG**
</dt> <dd> <dl> <dt>

0x120001
</dt> <dt>



Der Aufrufer verfügt über die folgenden Berechtigungen: **STANDARD \_ RIGHTS \_ READ,** **TRANSACTION QUERY \_ \_ INFORMATION** und **SYNCHRONIZE**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_GENERIC_WRITE"></span><span id="transaction_generic_write"></span>**GENERISCHER \_ \_ TRANSAKTIONSSCHREIBVORGANG**
</dt> <dd> <dl> <dt>

0x12003E
</dt> <dt>



Der Aufrufer verfügt über die folgenden Berechtigungen: **STANDARD \_ RIGHTS \_ WRITE,** **TRANSACTION SET \_ \_ INFORMATION,** **TRANSACTION \_ COMMIT,** **TRANSACTION \_ ENLIST,** **TRANSACTION \_ ROLLBACK,** **TRANSACTION \_ PROPAGATE** und **SYNCHRONIZE**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_GENERIC_EXECUTE"></span><span id="transaction_generic_execute"></span>**TRANSACTION \_ GENERIC \_ EXECUTE**
</dt> <dd> <dl> <dt>

0x120018
</dt> <dt>



Der Aufrufer verfügt über die folgenden Berechtigungen: **STANDARD \_ RIGHTS \_ EXECUTE,** **TRANSACTION \_ COMMIT,** **TRANSACTION \_ ROLLBACK** und **SYNCHRONIZE**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_ALL_ACCESS"></span><span id="transaction_all_access"></span>**TRANSACTION \_ ALL \_ ACCESS**
</dt> <dd> <dl> <dt>

0x12003F
</dt> <dt>



Der Aufrufer verfügt über die folgenden Berechtigungen: **STANDARD \_ RIGHTS \_ REQUIRED**, **TRANSACTION GENERIC \_ \_ READ**, **TRANSACTION GENERIC \_ \_ WRITE** und **TRANSACTION GENERIC \_ \_ EXECUTE**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_RESOURCE_MANAGER_RIGHTS"></span><span id="transaction_resource_manager_rights"></span>**RECHTE \_ DES TRANSAKTIONSRESSOURCEN-MANAGERS \_ \_**
</dt> <dd> <dl> <dt>

0x120037
</dt> <dt>



Der Aufrufer verfügt über die folgenden Berechtigungen: **TRANSACTION \_ GENERIC \_ READ,** **STANDARD RIGHTS \_ \_ WRITE,** **TRANSACTION SET \_ \_ INFORMATION,** **TRANSACTION \_ ROLLBACK,** **TRANSACTION \_ ENLIST,** **TRANSACTION \_ PROPAGATE** und **SYNCHRONIZE**.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Es wird empfohlen, dass Ressourcen-Manager bei der Eintragung in eine Transaktion **TRANSACTION \_ RESOURCE MANAGER \_ \_ RIGHTS** angeben, wenn sie eine Transaktion öffnen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                     |
| Header<br/>                   | <dl> <dt>WinNT.h</dt> </dl> |



 

 




