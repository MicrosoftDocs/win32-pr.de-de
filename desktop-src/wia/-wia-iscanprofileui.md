---
description: Mithilfe der iscanprofileui-Schnittstelle können Anwendungen ein Dialogfeld anzeigen, sodass Benutzer Scan Profile erstellen, ändern und löschen können.
ms.assetid: d0c7edcc-00d8-49b2-a0f7-fe4bbba90bfb
title: Iscanprofileui-Schnittstelle (scanprofileui. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileUI
api_type:
- COM
api_location:
- Scanprofileui.h
ms.openlocfilehash: c8791461db76c72de81216aef188886f63fde4f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354532"
---
# <a name="iscanprofileui-interface"></a>Iscanprofileui-Schnittstelle

Mithilfe der **iscanprofileui** -Schnittstelle können Anwendungen ein Dialogfeld anzeigen, sodass Benutzer Scan Profile erstellen, ändern und löschen können.

## <a name="members"></a>Member

Die **iscanprofileui** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Iscanprofileui** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iscanprofileui** -Schnittstelle verfügt über diese Methoden.



| Methode                                                             | BESCHREIBUNG                                                                                      |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**Scanprofiledialog**](-wia-iscanprofileui-scanprofiledialog.md) | Zeigt ein Dialogfeld an, in dem Benutzer Scan Profile erstellen, ändern und löschen können.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Das Dialogfeld ist modal. der Benutzer kann erst zum übergeordneten Fenster wechseln, wenn das Dialogfeld geschlossen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Scanprofileui. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Profil Schema überprüfen](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
