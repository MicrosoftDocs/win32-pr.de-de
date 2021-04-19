---
description: KTM definiert die folgenden Transaktions Zugriffs Masken, die beim Öffnen einer Transaktion verwendet werden sollen.
ms.assetid: 93ef3098-b3cc-4b24-ae82-1c10d937f14f
title: Transaktions Zugriffs Masken (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b815bcb04a97dbd059c85c6c615a7d607bf77ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348559"
---
# <a name="transaction-access-masks"></a>Transaktions Zugriffs Masken

KTM definiert die folgenden Transaktions Zugriffs Masken, die beim Öffnen einer Transaktion verwendet werden sollen.

<dl> <dt>

<span id="TRANSACTION_QUERY_INFORMATION"></span><span id="transaction_query_information"></span>**Transaktions \_ Abfrage \_ Informationen**
</dt> <dd> <dl> <dt>

0x000001
</dt> <dt>



Der Aufrufer kann Transaktionsinformationen Abfragen.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_SET_INFORMATION"></span><span id="transaction_set_information"></span>**Transaktions \_ Satz \_ Informationen**
</dt> <dd> <dl> <dt>

0x000002
</dt> <dt>



Der Aufrufer kann Transaktionsinformationen festlegen.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_ENLIST"></span><span id="transaction_enlist"></span>**Transaktions \_ enliste**
</dt> <dd> <dl> <dt>

0x000004
</dt> <dt>



Der Aufrufer kann diese Transaktion eintragen.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_COMMIT"></span><span id="transaction_commit"></span>**\_Transaktionscommit**
</dt> <dd> <dl> <dt>

0x000008
</dt> <dt>



Der Aufrufer kann diese Transaktion übertragen.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_ROLLBACK"></span><span id="transaction_rollback"></span>**Transaktions \_ Rollback**
</dt> <dd> <dl> <dt>

0x000010
</dt> <dt>



Der Aufrufer kann diese Transaktion zurücksetzen.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_PROPAGATE"></span><span id="transaction_propagate"></span>**Transaktionsverteilung \_**
</dt> <dd> <dl> <dt>

0x000020
</dt> <dt>



Der Aufrufer kann diese Transaktion an einen übergeordneten Ressourcen-Manager weitergeben, z. b. an den Distributed Transaction Coordinator (DTC).


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_GENERIC_READ"></span><span id="transaction_generic_read"></span>**\_allgemeiner Transaktions \_ Lesevorgang**
</dt> <dd> <dl> <dt>

0x120001
</dt> <dt>



Der Aufrufer verfügt über die folgenden Berechtigungen: **Standard \_ Rechte \_ Lesen**, **Transaktions \_ Abfrage \_ Informationen** und **Synchronisieren**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_GENERIC_WRITE"></span><span id="transaction_generic_write"></span>**\_allgemeiner Transaktions \_ Schreibvorgang**
</dt> <dd> <dl> <dt>

0x12003e
</dt> <dt>



Der Aufrufer verfügt über die folgenden Berechtigungen: **Standard \_ Rechte \_ Schreiben**, **Transaktions \_ Satz \_ Informationen**, **Transaktionscommit \_**, **Transaktions \_ Einschreibung**, **Transaktions \_ Rollback**, **Transaktions \_** Weitergabe und **Synchronisieren**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_GENERIC_EXECUTE"></span><span id="transaction_generic_execute"></span>**\_generische Transaktions \_ Ausführung**
</dt> <dd> <dl> <dt>

0x120018
</dt> <dt>



Der Aufrufer verfügt über die folgenden Berechtigungen: **Standard \_ Rechte werden \_ ausgeführt**, **Transaktionscommit \_**, **Transaktions \_ Rollback** und **Synchronisieren**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_ALL_ACCESS"></span><span id="transaction_all_access"></span>**\_Zugriff auf alle Transaktionen \_**
</dt> <dd> <dl> <dt>

0x12003f
</dt> <dt>



Der Aufrufer verfügt über die folgenden Berechtigungen: **Standard \_ Rechte \_ erforderlich**, **\_ allgemeiner Transaktions \_ Lese** Vorgang, **\_ allgemeiner Transaktions \_ Schreibvorgang** und **transaktionsgenerische \_ \_ Ausführung**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_RESOURCE_MANAGER_RIGHTS"></span><span id="transaction_resource_manager_rights"></span>**Rechte für den Transaktions \_ Ressourcen- \_ Manager \_**
</dt> <dd> <dl> <dt>

0x120037
</dt> <dt>



Der Aufrufer verfügt über die folgenden Berechtigungen: **\_ allgemeiner Transaktions \_ Lesevorgang**, **Standard \_ Rechte \_ Schreib** Vorgänge, **Transaktions \_ Satz \_ Informationen**, **Transaktions \_ Rollback**, **Transaktions \_ Einschreibung**, **Transaktions \_** Weitergabe und **Synchronisieren**.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Es wird empfohlen, dass Ressourcen-Manager beim Eintragen in eine Transaktion beim Öffnen einer Transaktion **Transaktions \_ Ressourcen-Manager- \_ \_ Rechte** angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                     |
| Header<br/>                   | <dl> <dt>WinNT. h</dt> </dl> |



 

 




