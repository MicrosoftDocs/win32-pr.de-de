---
description: WMI verfügt über Sicherheitskonst constants, die für die Namespacezugriffsüberprüfung durch \_ \_ SystemSecurity::GetCallerAccessRights verwendet werden.
ms.assetid: 2e905078-d510-4417-8acb-a6ff535d9d0b
ms.tgt_platform: multiple
title: Namespacezugriffsrechte-Konstanten (Wbemcli.h)
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
ms.openlocfilehash: 6c23bcde9d085a6668fd5c57ee0ff51a7db61784de44d79080e2b2d2d1ee051f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992750"
---
# <a name="namespace-access-rights-constants"></a>Namespacezugriffsrechte-Konstanten

WMI verfügt über Sicherheitskonst constants, die für die Namespacezugriffsüberprüfung durch [**\_ \_ SystemSecurity::GetCallerAccessRights verwendet werden.**](--systemsecurity-getcalleraccessrights.md) Sicherheitsinformationen zu Zugriffssteuerungslisten (ACLs, DACLs oder SACLs) finden Sie unter [Access Control-Listen (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) und [**Standardzugriffsrechte.**](/windows/desktop/SecAuthZ/standard-access-rights) Diese Konstanten werden in der **WBEM \_ SECURITY \_ FLAGS-Enumeration** definiert.

<dl> <dt>

<span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM \_ ENABLE**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Aktiviert das Konto und gewährt dem Benutzer Leseberechtigungen. Dies ist ein Standardzugriffsrecht für alle Benutzer und entspricht der Berechtigung Konto aktivieren für Registerkarte "Sicherheit" des [*WMI-Steuerelements.*](gloss-w.md) Weitere Informationen finden Sie unter [Festlegen der Namespacesicherheit mit dem WMI-Steuerelement](setting-namespace-security-with-the-wmi-control.md).


</dt> </dl> </dd> <dt>

<span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**\_WBEM-METHODE \_ EXECUTE**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Ermöglicht die Ausführung von Methoden. Anbieter können zusätzliche Zugriffsüberprüfungen durchführen. Dies ist ein Standardzugriffsrecht für alle Benutzer und entspricht der Berechtigung Methoden ausführen für Registerkarte "Sicherheit" des WMI-Steuerelements.


</dt> </dl> </dd> <dt>

<span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM \_ FULL \_ WRITE \_ REP**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Ermöglicht einem Benutzerkonto das Schreiben in Klassen im WMI-Repository sowie in Instanzen. Ein Benutzer kann nicht in Systemklassen schreiben. Nur Mitglieder der Gruppe Administratoren verfügen über diese Berechtigung. **WBEM \_ FULL \_ WRITE \_ REP** entspricht der Berechtigung Vollständiger Schreibzugriff auf Registerkarte "Sicherheit" des WMI-Steuerelements.


</dt> </dl> </dd> <dt>

<span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM \_ PARTIAL \_ WRITE \_ REP**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Ermöglicht das Schreiben von Daten nur in Instanzen, nicht in Klassen. Ein Benutzer kann keine Klassen in das [*WMI-Repository schreiben.*](gloss-w.md) Nur Mitglieder der Gruppe "Administratoren" haben dieses Recht. **WBEM \_ PARTIAL \_ WRITE \_ REP** entspricht der Berechtigung Partial Write für Registerkarte "Sicherheit" des WMI-Steuerelements.


</dt> </dl> </dd> <dt>

<span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**\_WBEM-SCHREIBANBIETER \_**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Ermöglicht das Schreiben von Klassen und Instanzen an Anbieter. Beachten Sie, dass Anbieter beim Identitätswechsel eines Benutzers zusätzliche Zugriffsüberprüfungen durchführen können. Dies ist ein Standardzugriffsrecht für alle Benutzer und entspricht der Schreibberechtigung des Anbieters für Registerkarte "Sicherheit" des WMI-Steuerelements.


</dt> </dl> </dd> <dt>

<span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**\_WBEM-REMOTEZUGRIFF \_**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Ermöglicht einem Benutzerkonto das Remote ausführen von Vorgängen, die durch die oben beschriebenen Berechtigungen zulässig sind. Nur Mitglieder der Gruppe "Administratoren" haben dieses Recht. **WBEM \_ REMOTE \_ ACCESS** entspricht der Berechtigung Remote enable für Registerkarte "Sicherheit" des WMI-Steuerelements.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                       |
| Header<br/>                   | <dl> <dt>Wbemcli.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[WMI-Sicherheitskonst constants](wmi-security-constants.md)
</dt> <dt>

[Sichern von WMI-Namespaces](securing-wmi-namespaces.md)
</dt> <dt>

[Zugriff auf WMI-Namespaces](access-to-wmi-namespaces.md)
</dt> <dt>

[WMI-Sicherheitsdeskriptorobjekte](wmi-security-descriptor-objects.md)
</dt> <dt>

[Ändern der Zugriffssicherheit für sicherungsfähige Objekte](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

