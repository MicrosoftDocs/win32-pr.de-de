---
description: BEI werden die folgenden Eintragungszugriffsmasken definiert, die beim Öffnen von Eintragungen verwendet werden sollen.
ms.assetid: 93773eb7-141a-49f3-9306-ffbda2f4ab9f
title: Eintragszugriffsmasken (WinNT.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85f3d774c474c27896c16bba5c7552713f248519aa86ef56da0da5b704234b19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870110"
---
# <a name="enlistment-access-masks"></a>Eintragszugriffsmasken

BEI werden die folgenden Eintragungszugriffsmasken definiert, die beim Öffnen von Eintragungen verwendet werden sollen.

<dl> <dt>

<span id="ENLISTMENT_QUERY_INFORMATION"></span><span id="enlistment_query_information"></span>**\_ \_ EINTRAGSABFRAGEINFORMATIONEN**
</dt> <dd> <dl> <dt>

0x00001
</dt> <dt>



Der Aufrufer kann BEI abfragen, um Informationen zur Eintragung zu erhalten.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_SET_INFORMATION"></span><span id="enlistment_set_information"></span>**\_ \_ EINTRAGSSATZINFORMATIONEN**
</dt> <dd> <dl> <dt>

0x00002
</dt> <dt>



Der Aufrufer kann Informationen zur Eintragung festlegen.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_RECOVER"></span><span id="enlistment_recover"></span>**ENLISTMENT \_ RECOVER**
</dt> <dd> <dl> <dt>

0x00004
</dt> <dt>



Der Aufrufer kann eine Eintragung wiederherstellen.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_SUBORDINATE_RIGHTS"></span><span id="enlistment_subordinate_rights"></span>**EINTRAGEN \_ \_ UNTERGEORDNETER RECHTE**
</dt> <dd> <dl> <dt>

0x00008
</dt> <dt>



Der Aufrufer kann Aktionen abschließen, die ein Ressourcen-Manager im Auftrag der Transaktion vornimmt. Im Folgenden ist eine Liste der Aktionen aufgeführt:

-   [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
-   [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
-   [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)
-   [**RollbackComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete)
-   [**ReadOnlyEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)
-   [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)
-   [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_SUPERIOR_RIGHTS"></span><span id="enlistment_superior_rights"></span>**ÜBERGEORDNETE RECHTE FÜR DIE EINTRAGUNG \_ \_**
</dt> <dd> <dl> <dt>

0x00010
</dt> <dt>



Der Aufrufer kann sich in der Transaktion als übergeordneter Transaktions-Manager eintragen.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_GENERIC_READ"></span><span id="enlistment_generic_read"></span>**EINTRAGEN \_ GENERISCHER \_ LESE-**
</dt> <dd> <dl> <dt>

0x20001
</dt> <dt>



Der Aufrufer verfügt über die folgenden Berechtigungen: **STANDARD \_ RIGHTS \_ READ** und **ENLISTMENT \_ QUERY \_ INFORMATION**.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_GENERIC_WRITE"></span><span id="enlistment_generic_write"></span>**EINTRAGEN DES \_ GENERISCHEN \_ SCHREIBZUGRIFFS**
</dt> <dd> <dl> <dt>

0x2001E
</dt> <dt>



Der Aufrufer verfügt über die folgenden Berechtigungen: **STANDARD \_ RIGHTS \_ WRITE,** **ENLISTMENT \_ SET \_ INFORMATION** und **ENLISTMENT \_ RECOVER**.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_GENERIC_EXECUTE"></span><span id="enlistment_generic_execute"></span>**ENLISTMENT \_ GENERIC \_ EXECUTE**
</dt> <dd> <dl> <dt>

0x2001C
</dt> <dt>



Der Aufrufer verfügt über die folgenden Berechtigungen: **STANDARD \_ RIGHTS \_ EXECUTE**, **ENLISTMENT \_ RECOVER** und **ENLISTMENT \_ SUBORDINATE \_ RIGHTS**.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_ALL_ACCESS"></span><span id="enlistment_all_access"></span>**EINTRAGEN \_ DES GESAMTEN \_ ZUGRIFFS**
</dt> <dd> <dl> <dt>

0xF001F
</dt> <dt>



Dieser Wert legt alle gültigen Bits für einen Eintragszugriffswert fest.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                     |
| Header<br/>                   | <dl> <dt>WinNT.h</dt> </dl> |



 

 




