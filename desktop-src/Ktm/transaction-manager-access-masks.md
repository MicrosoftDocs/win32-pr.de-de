---
description: BEI werden die folgenden Eintragungszugriffsmasken definiert, die beim Öffnen eines Transaktions-Managers (TM) verwendet werden sollen.
ms.assetid: 8f9b9d3d-e7ea-4df2-82b1-2d4c3e0766c0
title: Transaktions-Manager-Zugriffsmasken (WinNT.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cfa093f38898ec49a789699fc5c7230612ef744fec78f200021361327d9f714
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913900"
---
# <a name="transaction-manager-access-masks"></a>Transaktions-Manager-Zugriffsmasken

BEI werden die folgenden Eintragungszugriffsmasken definiert, die beim Öffnen eines Transaktions-Managers (TM) verwendet werden sollen.

<dl> <dt>

<span id="TRANSACTIONMANAGER_QUERY_INFORMATION"></span><span id="transactionmanager_query_information"></span>**\_TRANSACTIONMANAGER-ABFRAGEINFORMATIONEN \_**
</dt> <dd> <dl> <dt>

0x00001
</dt> <dt>



Der Aufrufer kann Informationen zu diesem TM abfragen.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_SET_INFORMATION"></span><span id="transactionmanager_set_information"></span>**TRANSACTIONMANAGER \_ SET \_ INFORMATION**
</dt> <dd> <dl> <dt>

0x00002
</dt> <dt>



Der Aufrufer kann Informationen zu diesem TM festlegen.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_RECOVER"></span><span id="transactionmanager_recover"></span>**TRANSACTIONMANAGER \_ RECOVER**
</dt> <dd> <dl> <dt>

0x00004
</dt> <dt>



Der Aufrufer kann dieses TM wiederherstellen.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_RENAME"></span><span id="transactionmanager_rename"></span>**TRANSACTIONMANAGER \_ RENAME**
</dt> <dd> <dl> <dt>

0x00008
</dt> <dt>



Der Aufrufer kann eine TM-Instanz umbenennen.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_CREATE_RM"></span><span id="transactionmanager_create_rm"></span>**TRANSACTIONMANAGER \_ CREATE \_ RM**
</dt> <dd> <dl> <dt>

0x00010
</dt> <dt>



Der Aufrufer kann einen Ressourcen-Manager erstellen, der diesem TM zugeordnet ist.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_BIND_TRANSACTION"></span><span id="transactionmanager_bind_transaction"></span>**TRANSACTIONMANAGER \_ BIND \_ TRANSACTION**
</dt> <dd> <dl> <dt>

0x00020
</dt> <dt>



Dieser Wert ist reserviert.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_READ"></span><span id="transactionmanager_generic_read"></span>**TRANSACTIONMANAGER \_ GENERIC \_ READ**
</dt> <dd> <dl> <dt>

0x20001
</dt> <dt>



Der Aufrufer verfügt über die folgenden Berechtigungen: **STANDARD \_ RIGHTS \_ READ** und **TRANSACTIONMANAGER QUERY \_ \_ INFORMATION**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_WRITE"></span><span id="transactionmanager_generic_write"></span>**TRANSACTIONMANAGER \_ GENERIC \_ WRITE**
</dt> <dd> <dl> <dt>

0x2001E
</dt> <dt>



Der Aufrufer verfügt über die folgenden Berechtigungen: **STANDARD \_ RIGHTS \_ WRITE**, **TRANSACTIONMANAGER SET \_ \_ INFORMATION**, **TRANSACTIONMANAGER \_ RECOVER**, **TRANSACTIONMANAGER \_ RENAME** und **TRANSACTIONMANAGER CREATE \_ \_ RM**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_EXECUTE"></span><span id="transactionmanager_generic_execute"></span>**TRANSACTIONMANAGER \_ GENERIC \_ EXECUTE**
</dt> <dd> <dl> <dt>

0x20000
</dt> <dt>



Der Aufrufer verfügt über die folgenden Berechtigungen: **STANDARD \_ RIGHTS \_ EXECUTE**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_ALL_ACCESS"></span><span id="transactionmanager_all_access"></span>**TRANSACTIONMANAGER \_ ALL \_ ACCESS**
</dt> <dd> <dl> <dt>

0xF003F
</dt> <dt>



Dieser Wert legt alle gültigen Bits für einen TM-Zugriffswert fest.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                     |
| Header<br/>                   | <dl> <dt>WinNT.h</dt> </dl> |



 

 




