---
title: RegistrationInfo-Objekt
description: Skripterstellungsobjekt, das die administrativen Informationen enthält, die zum Beschreiben der Aufgabe verwendet werden können.
ms.assetid: 3d5a5545-5adc-4361-9ce8-fffd35ff6df7
keywords:
- Registrierungsinformationen Taskplaner , Objekt
- RegistrationInfo-Taskplaner
- RegistrationInfo-Taskplaner , beschrieben
topic_type:
- apiref
api_name:
- RegistrationInfo
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f85bb423ae27a3d0b0b15f7b04d287a749f4fe23f3a4b58f7c2462b487b8a705
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072650"
---
# <a name="registrationinfo-object"></a>RegistrationInfo-Objekt

Skripterstellungsobjekt, das die administrativen Informationen enthält, die zum Beschreiben der Aufgabe verwendet werden können. Diese Informationen umfassen Details wie eine Beschreibung der Aufgabe, den Autor der Aufgabe, das Datum, an dem die Aufgabe registriert wurde, und die Sicherheitsbeschreibung der Aufgabe.

## <a name="members"></a>Member

Das **RegistrationInfo-Objekt** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **RegistrationInfo-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                                     | Zugriffstyp           | BESCHREIBUNG                                                                                                                                |
|:-----------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Autor**](registrationinfo-author.md)<br/>                         | Lesen/Schreiben<br/> | Ruft den Autor der Aufgabe ab oder legt diese fest.<br/>                                                                                            |
| [**Date**](registrationinfo-date.md)<br/>                             | Lesen/Schreiben<br/> | Ruft das Datum und die Uhrzeit der Registrierung der Aufgabe ab oder legt diese fest.<br/>                                                                     |
| [**Beschreibung**](registrationinfo-description.md)<br/>               | Lesen/Schreiben<br/> | Ruft die Beschreibung der Aufgabe ab oder legt sie fest.<br/>                                                                                       |
| [**Dokumentation**](registrationinfo-documentation.md)<br/>           | Lesen/Schreiben<br/> | Ruft eine zusätzliche Dokumentation für den Task ab oder legt diese fest.<br/>                                                                         |
| [**SecurityDescriptor**](registrationinfo-securitydescriptor.md)<br/> |                       | Ruft den Sicherheitsdeskriptor der Aufgabe ab oder legt diese fest.<br/>                                                                               |
| [**Quelle**](registrationinfo-source.md)<br/>                         | Lesen/Schreiben<br/> | Ruft ab oder legt fest, woher die Aufgabe stammt. Beispielsweise kann eine Aufgabe von einer Komponente, einem Dienst, einer Anwendung oder einem Benutzer stammen.<br/> |
| [**URI**](registrationinfo-uri.md)<br/>                               | Lesen/Schreiben<br/> | Ruft den URI der Aufgabe ab oder legt den URI fest.<br/>                                                                                               |
| [**Version**](registrationinfo-version.md)<br/>                       | Lesen/Schreiben<br/> | Ruft die Versionsnummer der Aufgabe ab oder legt sie fest.<br/>                                                                                    |
| [**Xmltext**](registrationinfo-xmltext.md)<br/>                       | Lesen/Schreiben<br/> | Ruft eine XML-formatierte Version der Registrierungsinformationen für den Task ab oder legt diese fest.<br/>                                             |



 

## <a name="remarks"></a>Hinweise

Registrierungsinformationen können verwendet werden, um eine Aufgabe über die benutzeroberfläche Taskplaner oder als Suchkriterien beim Aufzählen der registrierten Aufgaben zu identifizieren.

Beim Lesen oder Schreiben von XML für einen Task werden registrierungsinformationen für den Task im [**RegistrationInfo-Element**](taskschedulerschema-registrationinfo-tasktype-element.md) des Taskplaner angegeben.

## <a name="examples"></a>Beispiele

Weitere Informationen und Beispielcode für dieses Skriptobjekt finden Sie unter [Time Trigger Example (Scripting) .](time-trigger-example--scripting-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





