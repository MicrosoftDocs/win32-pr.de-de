---
description: KTM definiert die folgenden Eintragung-Zugriffs Masken, die beim Öffnen eines Transaktions-Managers (TM) verwendet werden.
ms.assetid: 8f9b9d3d-e7ea-4df2-82b1-2d4c3e0766c0
title: Zugriffs Masken für den Transaktions-Manager (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efae6c0bac1fc2bfa117e74e38aff8d439eb2f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864567"
---
# <a name="transaction-manager-access-masks"></a>Zugriffs Masken für den Transaktions-Manager

KTM definiert die folgenden Eintragung-Zugriffs Masken, die beim Öffnen eines Transaktions-Managers (TM) verwendet werden.

<dl> <dt>

<span id="TRANSACTIONMANAGER_QUERY_INFORMATION"></span><span id="transactionmanager_query_information"></span>**transaktionmanager- \_ Abfrage \_ Informationen**
</dt> <dd> <dl> <dt>

0x00001 beginnt
</dt> <dt>



Der Aufrufer kann Informationen zu diesem TM Abfragen.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_SET_INFORMATION"></span><span id="transactionmanager_set_information"></span>**Informationen zum transaktionmanager- \_ Satz \_**
</dt> <dd> <dl> <dt>

0x00002
</dt> <dt>



Der Aufrufer kann Informationen zu diesem TM festlegen.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_RECOVER"></span><span id="transactionmanager_recover"></span>**Wiederherstellung durch transaktionmanager \_**
</dt> <dd> <dl> <dt>

0x00004
</dt> <dt>



Der Aufrufer kann dieses TM wiederherstellen.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_RENAME"></span><span id="transactionmanager_rename"></span>**Umbenennen von transaktionmanager \_**
</dt> <dd> <dl> <dt>

0x00008
</dt> <dt>



Der Aufrufer kann eine TM-Instanz umbenennen.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_CREATE_RM"></span><span id="transactionmanager_create_rm"></span>**transaktionmanager \_ Create \_ RM**
</dt> <dd> <dl> <dt>

0x00010
</dt> <dt>



Der Aufrufer kann einen Ressourcen-Manager erstellen, der mit diesem TM verknüpft ist.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_BIND_TRANSACTION"></span><span id="transactionmanager_bind_transaction"></span>**Transaktions-Manager- \_ Bindungs \_ Transaktion**
</dt> <dd> <dl> <dt>

0x00020
</dt> <dt>



Dieser Wert ist reserviert.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_READ"></span><span id="transactionmanager_generic_read"></span>**allgemeiner transaktionmanager- \_ \_ Lesevorgang**
</dt> <dd> <dl> <dt>

0x20001
</dt> <dt>



Der Aufrufer verfügt über die folgenden Berechtigungen: **Standard \_ Rechte \_ Lesen** und **transaktionmanager- \_ Abfrage \_ Informationen**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_WRITE"></span><span id="transactionmanager_generic_write"></span>**allgemeiner transaktionmanager- \_ \_ Schreibvorgang**
</dt> <dd> <dl> <dt>

0x2001e
</dt> <dt>



Der Aufrufer verfügt über die folgenden Berechtigungen: **Standard \_ Rechte \_ Schreiben**, **Transaktions-Manager-Set- \_ \_ Informationen**, **transaktionmanager- \_ Wiederherstellung**, **Transaktions-umbenennen \_** und **Transaktionsmanager \_ Create \_ RM**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_EXECUTE"></span><span id="transactionmanager_generic_execute"></span>**generische transaktionmanager- \_ \_ Ausführung**
</dt> <dd> <dl> <dt>

0x20000
</dt> <dt>



Der Aufrufer verfügt über die folgenden Berechtigungen: **Standard \_ Rechte werden \_ ausgeführt**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_ALL_ACCESS"></span><span id="transactionmanager_all_access"></span>**transaktionmanager \_ alle \_ Zugriffe**
</dt> <dd> <dl> <dt>

0xF 003F
</dt> <dt>



Dieser Wert legt alle gültigen Bits für einen TM-Zugriffs Wert fest.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                     |
| Header<br/>                   | <dl> <dt>WinNT. h</dt> </dl> |



 

 




