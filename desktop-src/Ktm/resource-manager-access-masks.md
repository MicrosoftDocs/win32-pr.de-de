---
description: KTM definiert die folgenden Eintragung-Zugriffs Masken, die beim Öffnen eines Ressourcen-Managers verwendet werden.
ms.assetid: 6b901b73-516d-4f27-b258-3b93a8f9675f
title: Ressourcen-Manager Zugriffs Masken (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f0f579a96ed80de100a5cb41cb9c4e9b847a060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131517"
---
# <a name="resource-manager-access-masks"></a>Ressourcen-Manager Zugriffs Masken

KTM definiert die folgenden Eintragung-Zugriffs Masken, die beim Öffnen eines Ressourcen-Managers verwendet werden.

<dl> <dt>

<span id="RESOURCEMANAGER_QUERY_INFORMATION"></span><span id="resourcemanager_query_information"></span>**ResourceManager- \_ Abfrage \_ Informationen**
</dt> <dd> <dl> <dt>



Der Aufrufer kann die Informationen des Ressourcen-Managers (RM) Abfragen.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_SET_INFORMATION"></span><span id="resourcemanager_set_information"></span>**Informationen zum ResourceManager- \_ Satz \_**
</dt> <dd> <dl> <dt>



Der Aufrufer kann die RM-Informationen festlegen.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_RECOVER"></span><span id="resourcemanager_recover"></span>**ResourceManager- \_ Wiederherstellung**
</dt> <dd> <dl> <dt>



Der Aufrufer kann das angegebene RM wiederherstellen.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_ENLIST"></span><span id="resourcemanager_enlist"></span>**ResourceManager- \_ Enlist**
</dt> <dd> <dl> <dt>



Der Aufrufer kann eine RM in eine Transaktion eintragen.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GET_NOTIFICATION"></span><span id="resourcemanager_get_notification"></span>**ResourceManager- \_ get- \_ Benachrichtigung**
</dt> <dd> <dl> <dt>



Der Aufrufer kann eine Benachrichtigung für einen RM erhalten.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GENERIC_READ"></span><span id="resourcemanager_generic_read"></span>**generischer ResourceManager- \_ \_ Lesevorgang**
</dt> <dd> <dl> <dt>



Der Aufrufer verfügt über die folgenden Berechtigungen: Standard \_ Rechte \_ lesen, Abfrage Informationen von ResourceManager \_ \_ und ResourceManager- \_ Wiederherstellung.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GENERIC_WRITE"></span><span id="resourcemanager_generic_write"></span>**\_generischer Schreibvorgang von ResourceManager \_**
</dt> <dd> <dl> <dt>



Der Aufrufer verfügt über die folgenden Berechtigungen: Standard \_ Rechte \_ schreiben, Informationen zum ResourceManager \_ \_ -Satz, ResourceManager \_ Enlist und ResourceManager \_ get- \_ Benachrichtigung.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GENERIC_EXECUTE"></span><span id="resourcemanager_generic_execute"></span>**generische ResourceManager- \_ \_ Ausführung**
</dt> <dd> <dl> <dt>



Der Aufrufer verfügt über die folgenden Berechtigungen: Standard \_ Rechte \_ Execute, ResourceManager \_ Enlist und ResourceManager \_ get \_ Notification.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_ALL_ACCESS"></span><span id="resourcemanager_all_access"></span>**ResourceManager \_ - \_ Zugriff**
</dt> <dd> <dl> <dt>



Der Aufrufer verfügt über die folgenden Berechtigungen: Standard \_ Rechte sind \_ erforderlich.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                     |
| Header<br/>                   | <dl> <dt>WinNT. h</dt> </dl> |



 

 




