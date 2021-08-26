---
title: Principal-Objekt
description: Skripterstellungsobjekt, das die Sicherheitsanmeldeinformationen für einen Prinzipal enthält.
ms.assetid: 9589f3c2-2709-4e71-8986-2347be049f6b
keywords:
- Prinzipalobjekt-Taskplaner
- Prinzipalobjekt Taskplaner , beschrieben
topic_type:
- apiref
api_name:
- Principal
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6cf4187875f3b02dfbdc8ef5bd9fd8bd43ed99c37134b2c899215decacfb605
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126080"
---
# <a name="principal-object"></a>Principal-Objekt

Skripterstellungsobjekt, das die Sicherheitsanmeldeinformationen für einen Prinzipal enthält. Diese Sicherheitsanmeldeinformationen definieren den Sicherheitskontext für die Aufgaben, die dem Prinzipal zugeordnet sind.

## <a name="members"></a>Member

Das **Principal-Objekt** verfügt über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Principal-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                | Zugriffstyp           | Beschreibung                                                                                                                                                  |
|:--------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DisplayName**](principal-displayname.md)<br/> | Lesen/Schreiben<br/> | Ruft den Namen des Prinzipals ab, der auf der Benutzeroberfläche des -Taskplaner wird, oder legt diesen fest.<br/>                                                                |
| [**Groupid**](principal-groupid.md)<br/>         | Lesen/Schreiben<br/> | Ruft den Bezeichner der Benutzergruppe ab, die zum Ausführen der dem Prinzipal zugeordneten Aufgaben erforderlich ist, oder legt diesen fest.<br/>                           |
| [**Id**](principal-id.md)<br/>                   | Lesen/Schreiben<br/> | Ruft den Bezeichner des Prinzipals ab oder legt ihn fest.<br/>                                                                                                     |
| [**LogonType**](principal-logontype.md)<br/>     | Lesen/Schreiben<br/> | Ruft die Sicherheitsanmeldungsmethode ab, die zum Ausführen der dem Prinzipal zugeordneten Aufgaben erforderlich ist, oder legt diese fest.<br/>                                  |
| [**Runlevel**](principal-runlevel.md)<br/>       | Lesen/Schreiben<br/> | Ruft den Bezeichner ab, mit dem die Berechtigungsebene angegeben wird, die zum Ausführen der dem Prinzipal zugeordneten Aufgaben erforderlich ist, oder legt diesen fest.<br/> |
| [**Userid**](principal-userid.md)<br/>           | Lesen/Schreiben<br/> | Ruft den Benutzerbezeichner ab, der zum Ausführen der dem Prinzipal zugeordneten Aufgaben erforderlich ist, oder legt diesen fest.<br/>                                        |



 

## <a name="remarks"></a>Hinweise

Denken Sie beim Angeben eines Kontos daran, den doppelten zurücken Schrägstrich im Code ordnungsgemäß zu verwenden, um die Domäne und den Benutzernamen anzugeben. Verwenden Sie beispielsweise DOMAIN \\ \\ UserName, um einen Wert für die [**UserId-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) anzugeben.

Beim Lesen oder Schreiben von XML für eine Aufgabe werden die Sicherheitsanmeldeinformationen für einen Prinzipal im [**Principal-Element**](taskschedulerschema-principal-principaltype-element.md) des Taskplaner angegeben.

Wenn eine Aufgabe mithilfe des at.exe-Befehlszeilentools registriert wird und dieses Objekt zum Abrufen von Informationen über den Task verwendet wird, gibt die [**LogonType-Eigenschaft**](principal-logontype.md) 0 zurück, die [**RunLevel-Eigenschaft**](principal-runlevel.md) gibt 0 zurück, und die [**UserId-Eigenschaft**](principal-userid.md) gibt Nothing zurück.

## <a name="examples"></a>Beispiele

Weitere Informationen und Beispielcode für dieses Skriptobjekt finden Sie unter [Time Trigger Example (Scripting) .](time-trigger-example--scripting-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





