---
description: 'WMI verfügt über Sicherheits Konstanten, die für die Überprüfung des Namespace Zugriffs durch \_ \_ SystemSecurity:: getcalleraccessrights verwendet werden.'
ms.assetid: 2e905078-d510-4417-8acb-a6ff535d9d0b
ms.tgt_platform: multiple
title: Namespace-Zugriffsrechte Konstanten (wbemcli. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WBEM_ENABLE
- WBEM_METHOD_EXECUTE
- WBEM_FULL_WRITE_REP
- WBEM_PARTIAL_WRITE_REP
- WBEM_WRITE_PROVIDER
- WBEM_REMOTE_ACCESS
api_type:
- HeaderDef
api_location:
- Wbemcli.h
ms.openlocfilehash: 469e036b7cd385fa2ac2bae23e0da081288b536b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041586"
---
# <a name="namespace-access-rights-constants"></a>Namespace-Zugriffsrechte Konstanten

WMI verfügt über Sicherheits Konstanten, die für die Überprüfung des Namespace Zugriffs durch [**\_ \_ SystemSecurity:: getcalleraccessrights**](--systemsecurity-getcalleraccessrights.md)verwendet werden. Sicherheitsinformationen zu Zugriffs Steuerungs Listen (ACLs, DACLs oder SACLs) finden Sie unter [Access Control Listen (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) und [**Standard Zugriffsrechte**](/windows/desktop/SecAuthZ/standard-access-rights). Diese Konstanten werden in der **WBEM- \_ \_ sicherheitsflags** -Enumeration definiert.

<dl> <dt>

<span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM- \_ Aktivierung**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Aktiviert das Konto und gewährt dem Benutzer Leseberechtigungen. Dies ist ein Standard Zugriffsrecht für alle Benutzer und entspricht der Berechtigung Konto aktivieren auf der Registerkarte Sicherheit des [*WMI-Steuer*](gloss-w.md)Elements. Weitere Informationen finden Sie unter [Festlegen der Namespace Sicherheit mit dem WMI-Steuer](setting-namespace-security-with-the-wmi-control.md)Element.


</dt> </dl> </dd> <dt>

<span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM- \_ Methode \_ Ausführen**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Ermöglicht die Ausführung von-Methoden. Anbieter können zusätzliche Zugriffs Überprüfungen durchführen. Dies ist ein Standard Zugriffsrecht für alle Benutzer und entspricht der Berechtigung Execute Methods auf der Registerkarte Sicherheit des WMI-Steuer Elements.


</dt> </dl> </dd> <dt>

<span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM \_ Vollständiger \_ Schreibzugriff \_**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Ermöglicht einem Benutzerkonto das Schreiben in Klassen im WMI-Repository und in-Instanzen. Ein Benutzer kann nicht in System Klassen schreiben. Nur Mitglieder der Gruppe "Administratoren" verfügen über diese Berechtigung. **WBEM \_ Voll \_ ständiger \_ Schreib** Zugriff entspricht der vollständigen Schreib Berechtigung auf der Registerkarte "Sicherheit" des WMI-Steuer Elements.


</dt> </dl> </dd> <dt>

<span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**\_partieller \_ Schreibvorgang von WBEM \_**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Ermöglicht das Schreiben von Daten nur in-Instanzen, nicht in Klassen. Ein Benutzer kann keine Klassen in das [*WMI-Repository*](gloss-w.md)schreiben. Nur Mitglieder der Gruppe "Administratoren" haben dieses Recht. **WBEM \_ Partieller \_ Schreib \_** Zugriff entspricht der Berechtigung zum partiellen schreiben auf der Registerkarte Sicherheit des WMI-Steuer Elements.


</dt> </dl> </dd> <dt>

<span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM- \_ Schreib \_ Anbieter**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Ermöglicht das Schreiben von Klassen und Instanzen in Anbieter. Beachten Sie, dass Anbieter bei der Identität eines Benutzers zusätzliche Zugriffs Überprüfungen durchführen können. Dies ist ein Standard Zugriffsrecht für alle Benutzer und entspricht der Schreib Berechtigung des Anbieters auf der Registerkarte Sicherheit des WMI-Steuer Elements.


</dt> </dl> </dd> <dt>

<span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM- \_ Remote \_ Zugriff**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Ermöglicht einem Benutzerkonto das Remote Ausführen von Vorgängen, die von den oben beschriebenen Berechtigungen zugelassen werden. Nur Mitglieder der Gruppe "Administratoren" haben dieses Recht. **WBEM \_ Der Remote \_ Zugriff** entspricht der Berechtigung Remote Aktivierung auf der Registerkarte Sicherheit des WMI-Steuer Elements.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                       |
| Header<br/>                   | <dl> <dt>Wbemcli. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WMI-Sicherheits Konstanten](wmi-security-constants.md)
</dt> <dt>

[Sichern von WMI-Namespaces](securing-wmi-namespaces.md)
</dt> <dt>

[Zugriff auf WMI-Namespaces](access-to-wmi-namespaces.md)
</dt> <dt>

[WMI-sicherheitsdeskriptorobjekte](wmi-security-descriptor-objects.md)
</dt> <dt>

[Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

