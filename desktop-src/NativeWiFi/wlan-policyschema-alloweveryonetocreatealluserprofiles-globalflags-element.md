---
description: Gibt an, ob ein Benutzer ein Profil für alle Benutzer erstellen kann.
ms.assetid: b9bdfe85-b9d5-4dcc-a7f8-05cce9702ec3
title: "' zugweveryonetkreatealluserprofiles '-Element (globalflags)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- allowEveryoneToCreateAllUserProfiles
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 63bc4c76ccecd8c7f774dc0e73621ef3f9b19877
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525766"
---
# <a name="alloweveryonetocreatealluserprofiles-globalflags-element"></a>' zugweveryonetkreatealluserprofiles '-Element (globalflags)

Das Element " **connecweveryonedekreatealluserprofiles** " (globalflags) gibt an, ob ein Benutzer ein Profil für alle Benutzer erstellen kann. Ein Profil für alle Benutzer kann von jedem Benutzer auf dem Computer verwendet werden, um eine Verbindung mit dem Drahtlos Netzwerk herzustellen, das mit dem Profil verknüpft ist.

Wenn "zugebestellungs-Manager- **profile** " auf "true" festgelegt ist, kann ein beliebiges Benutzerprofil erstellt werden. Wenn " **connecweveryonedekreatealluserprofiles** " auf "false" festgelegt ist, können nicht alle Benutzer ein Profil für alle Benutzer erstellen, und es gibt eine DACL, die dem \_ Sicherheits Objekt "WLAN Secure \_ Add New all User Profiles" zugeordnet ist, \_ \_ \_ \_ das die Benutzer oder Benutzergruppen mit der Berechtigung zum Erstellen von Profilen für alle Benutzer angibt. Die Standard-DACL gibt an, dass nur Benutzer, die als Mitglied der Gruppe "Administratoren" angemeldet sind, ein Profil für alle Benutzer erstellen können. Die Standard Sicherheitseinstellungen können durch Aufrufen von [**wlansetsecuritysettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings)geändert werden. Um die aktuellen Sicherheitseinstellungen abzurufen, nennen Sie [**wlangetsecuritysettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).

Dieses Element ist obligatorisch. Wenn ein Profil vom AutoConfig-Dienst erstellt wird, hat dieses Element den Standardwert true.

``` syntax
<xs:element name="allowEveryoneToCreateAllUserProfiles"
    type="boolean"
 />
```

Das Element " **connecweveryonetkreatealluserprofiles** " wird durch das [**globalflags**](wlan-policyschema-globalflags-wlanpolicy-element.md) -Element definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**globalflags**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**globalflags (wlanpolicy)**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




