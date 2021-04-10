---
title: RegistrationInfo-Objekt
description: Skript Objekt, das die administrativen Informationen bereitstellt, die zum Beschreiben der Aufgabe verwendet werden können.
ms.assetid: 3d5a5545-5adc-4361-9ce8-fffd35ff6df7
keywords:
- Registrierungsinformationen Taskplaner, Objekt
- RegistrationInfo-Objekt Taskplaner
- RegistrationInfo-Objekt Taskplaner, beschrieben
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
ms.openlocfilehash: 7b7eb50da6b69622f6101fdbae4ad098d88f0366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040338"
---
# <a name="registrationinfo-object"></a>RegistrationInfo-Objekt

Skript Objekt, das die administrativen Informationen bereitstellt, die zum Beschreiben der Aufgabe verwendet werden können. Diese Informationen umfassen Details wie z. b. eine Beschreibung der Aufgabe, den Autor der Aufgabe, das Datum, an dem der Task registriert ist, und die Sicherheits Beschreibung des Tasks.

## <a name="members"></a>Member

Das **RegistrationInfo** -Objekt verfügt über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **RegistrationInfo** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                                     | Zugriffstyp           | BESCHREIBUNG                                                                                                                                |
|:-----------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Autor**](registrationinfo-author.md)<br/>                         | Lesen/Schreiben<br/> | Ruft den Autor der Aufgabe ab oder legt ihn fest.<br/>                                                                                            |
| [**Datum**](registrationinfo-date.md)<br/>                             | Lesen/Schreiben<br/> | Ruft das Datum und die Uhrzeit der Registrierung der Aufgabe ab oder legt diese fest.<br/>                                                                     |
| [**Beschreibung**](registrationinfo-description.md)<br/>               | Lesen/Schreiben<br/> | Ruft die Beschreibung der Aufgabe ab oder legt Sie fest.<br/>                                                                                       |
| [**Dokumentation**](registrationinfo-documentation.md)<br/>           | Lesen/Schreiben<br/> | Ruft eine zusätzliche Dokumentation für den Task ab oder legt diese fest.<br/>                                                                         |
| [**SecurityDescriptor**](registrationinfo-securitydescriptor.md)<br/> |                       | Ruft die Sicherheits Beschreibung der Aufgabe ab oder legt Sie fest.<br/>                                                                               |
| [**`Source`**](registrationinfo-source.md)<br/>                         | Lesen/Schreiben<br/> | Ruft ab oder legt fest, wo die Aufgabe aus stammt. Beispielsweise kann eine Aufgabe aus einer Komponente, einem Dienst, einer Anwendung oder einem Benutzer stammen.<br/> |
| [**RT**](registrationinfo-uri.md)<br/>                               | Lesen/Schreiben<br/> | Ruft den URI der Aufgabe ab oder legt ihn fest.<br/>                                                                                               |
| [**Version**](registrationinfo-version.md)<br/>                       | Lesen/Schreiben<br/> | Ruft die Versionsnummer der Aufgabe ab oder legt Sie fest.<br/>                                                                                    |
| [**XmlText**](registrationinfo-xmltext.md)<br/>                       | Lesen/Schreiben<br/> | Ruft eine XML-formatierte Version der Registrierungsinformationen für den Task ab oder legt diese fest.<br/>                                             |



 

## <a name="remarks"></a>Bemerkungen

Registrierungsinformationen können verwendet werden, um eine Aufgabe über die Taskplaner-Benutzeroberfläche oder als Suchkriterium zu identifizieren, wenn die registrierten Tasks aufgezählt werden.

Beim Lesen oder Schreiben von XML für eine Aufgabe werden Registrierungsinformationen für die Aufgabe im [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) -Element des Taskplaner Schemas angegeben.

## <a name="examples"></a>Beispiele

Weitere Informationen und Beispielcode für dieses Skript Objekt finden Sie unter [time-auslöserbeispiel (Skripterstellung)](time-trigger-example--scripting-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





