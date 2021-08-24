---
description: KTM definiert die folgenden Eintragungszugriffsmasken, die beim Öffnen eines Ressourcen-Managers verwendet werden sollen.
ms.assetid: 6b901b73-516d-4f27-b258-3b93a8f9675f
title: Resource Manager Access Masks (WinNT.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12ede54d5d49533e70aa9cda2d9c4a363d61f1fdbd894108a5b83f2c5e9efc98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146483"
---
# <a name="resource-manager-access-masks"></a>Resource Manager Zugriffsmasken

KTM definiert die folgenden Eintragungszugriffsmasken, die beim Öffnen eines Ressourcen-Managers verwendet werden sollen.

<dl> <dt>

<span id="RESOURCEMANAGER_QUERY_INFORMATION"></span><span id="resourcemanager_query_information"></span>**\_RESOURCEMANAGER-ABFRAGEINFORMATIONEN \_**
</dt> <dd> <dl> <dt>



Der Aufrufer kann die Resource Manager-Informationen (RM) abfragen.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_SET_INFORMATION"></span><span id="resourcemanager_set_information"></span>**RESOURCEMANAGER \_ SET \_ INFORMATION**
</dt> <dd> <dl> <dt>



Der Aufrufer kann die RM-Informationen festlegen.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_RECOVER"></span><span id="resourcemanager_recover"></span>**RESOURCEMANAGER \_ RECOVER**
</dt> <dd> <dl> <dt>



Der Aufrufer kann den angegebenen RM wiederherstellen.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_ENLIST"></span><span id="resourcemanager_enlist"></span>**RESOURCEMANAGER \_ ENLIST**
</dt> <dd> <dl> <dt>



Der Aufrufer kann einen RM in eine Transaktion einlisten.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GET_NOTIFICATION"></span><span id="resourcemanager_get_notification"></span>**RESOURCEMANAGER \_ GET \_ NOTIFICATION**
</dt> <dd> <dl> <dt>



Der Aufrufer kann eine Benachrichtigung für einen RM empfangen.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GENERIC_READ"></span><span id="resourcemanager_generic_read"></span>**GENERISCHER \_ \_ RESOURCEMANAGER-LESE-**
</dt> <dd> <dl> <dt>



Der Aufrufer verfügt über die folgenden Berechtigungen: STANDARD \_ RIGHTS \_ READ, RESOURCEMANAGER \_ QUERY INFORMATION und \_ RESOURCEMANAGER \_ RECOVER.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GENERIC_WRITE"></span><span id="resourcemanager_generic_write"></span>**GENERISCHER \_ \_ RESOURCEMANAGER-SCHREIBZUGRIFF**
</dt> <dd> <dl> <dt>



Der Aufrufer verfügt über die folgenden Berechtigungen: STANDARD \_ RIGHTS \_ WRITE, RESOURCEMANAGER \_ SET \_ INFORMATION, RESOURCEMANAGER \_ ENLIST und RESOURCEMANAGER \_ GET \_ NOTIFICATION.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GENERIC_EXECUTE"></span><span id="resourcemanager_generic_execute"></span>**RESOURCEMANAGER \_ GENERIC \_ EXECUTE**
</dt> <dd> <dl> <dt>



Der Aufrufer verfügt über die folgenden Berechtigungen: STANDARD \_ RIGHTS \_ EXECUTE, RESOURCEMANAGER \_ ENLIST und RESOURCEMANAGER \_ GET \_ NOTIFICATION.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_ALL_ACCESS"></span><span id="resourcemanager_all_access"></span>**RESOURCEMANAGER \_ ALL \_ ACCESS**
</dt> <dd> <dl> <dt>



Der Aufrufer verfügt über die folgenden Berechtigungen: STANDARD \_ RIGHTS \_ REQUIRED.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                     |
| Header<br/>                   | <dl> <dt>WinNT.h</dt> </dl> |



 

 




