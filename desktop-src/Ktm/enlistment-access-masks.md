---
description: KTM definiert die folgenden Eintragung-Zugriffs Masken, die beim Öffnen von Eintragung verwendet werden.
ms.assetid: 93773eb7-141a-49f3-9306-ffbda2f4ab9f
title: Eintragung von Zugriffs Masken (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63e4ebd67f93368215ebcdcd362595d0341adb52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369046"
---
# <a name="enlistment-access-masks"></a>Eintragung von Zugriffs Masken

KTM definiert die folgenden Eintragung-Zugriffs Masken, die beim Öffnen von Eintragung verwendet werden.

<dl> <dt>

<span id="ENLISTMENT_QUERY_INFORMATION"></span><span id="enlistment_query_information"></span>**Eintragung von \_ Abfrage \_ Informationen**
</dt> <dd> <dl> <dt>

0x00001 beginnt
</dt> <dt>



Der Aufrufer kann KTM nach Informationen zur Eintragung Abfragen.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_SET_INFORMATION"></span><span id="enlistment_set_information"></span>**Informationen zu Eintragung \_ \_**
</dt> <dd> <dl> <dt>

0x00002
</dt> <dt>



Der Aufrufer kann Informationen über die Eintragung festlegen.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_RECOVER"></span><span id="enlistment_recover"></span>**Eintragung der Eintragung \_**
</dt> <dd> <dl> <dt>

0x00004
</dt> <dt>



Der Aufrufer kann eine Eintragung wiederherstellen.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_SUBORDINATE_RIGHTS"></span><span id="enlistment_subordinate_rights"></span>**unter \_ geordnete Rechte der \_ Eintragung**
</dt> <dd> <dl> <dt>

0x00008
</dt> <dt>



Der Aufrufer kann Aktionen ausführen, die ein Ressourcen-Manager für die Transaktion ausführt. Im folgenden finden Sie eine Liste von Aktionen:

-   [**Commitcomplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
-   [**Preparecomplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
-   [**Prepreparecomplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)
-   [**Rollbackcomplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete)
-   [**Read onlyeintragung**](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)
-   [**Rollbackeintragung**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)
-   [**Singlephasereject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_SUPERIOR_RIGHTS"></span><span id="enlistment_superior_rights"></span>**Erweiterte Rechte Eintragung \_ \_**
</dt> <dd> <dl> <dt>

0x00010
</dt> <dt>



Der Aufrufer kann sich als übergeordneter Transaktions-Manager in die Transaktion eintragen.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_GENERIC_READ"></span><span id="enlistment_generic_read"></span>**allgemeiner Einschreibungs \_ \_ Lesevorgang**
</dt> <dd> <dl> <dt>

0x20001
</dt> <dt>



Der Aufrufer verfügt über die folgenden Berechtigungen: **Standard \_ Rechte \_ Lese** -und Eintragung von **\_ Abfrage \_ Informationen**.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_GENERIC_WRITE"></span><span id="enlistment_generic_write"></span>**\_allgemeiner \_ Schreibzugriff**
</dt> <dd> <dl> <dt>

0x2001e
</dt> <dt>



Der Aufrufer verfügt über die folgenden Berechtigungen: **Standard \_ Rechte \_ Schreiben**, **\_ \_ Informationen** zu Eintragung und **Eintragung \_ Wiederherstellen**.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_GENERIC_EXECUTE"></span><span id="enlistment_generic_execute"></span>**\_generische Eintragung \_ Ausführen**
</dt> <dd> <dl> <dt>

0x2001c
</dt> <dt>



Der Aufrufer verfügt über die folgenden Berechtigungen: **Standard \_ Rechte werden \_ ausgeführt**, **Eintragung werden \_ wieder hergestellt**, und Eintragung von unter **\_ geordneten \_ rechten**.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_ALL_ACCESS"></span><span id="enlistment_all_access"></span>**Eintragung für den \_ gesamten \_ Zugriff**
</dt> <dd> <dl> <dt>

0xF 001F
</dt> <dt>



Dieser Wert legt alle gültigen Bits für einen Eintragung-Zugriffs Wert fest.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                     |
| Header<br/>                   | <dl> <dt>WinNT. h</dt> </dl> |



 

 




