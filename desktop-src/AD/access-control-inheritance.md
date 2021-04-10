---
title: Access Control Vererbung
description: Zugriffs Steuerungs Einträge (ACEs) in einer Objekt Zugriffs Steuerungs Liste (Access Control List, ACL) können zu einer effektiven Zugriffs Steuerungs Liste (ACL) oder als Vererbungs-ACL gehören.
ms.assetid: 2530eef5-7804-4b27-8756-d97be1cea116
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec7514ab8cae8b07121d84e579ccb8492b67c45
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101402"
---
# <a name="access-control-inheritance"></a>Access Control Vererbung

Zugriffs Steuerungs Einträge (ACEs) in einer Objekt Zugriffs Steuerungs Liste (Access Control List, ACL) können zu einer von zwei Kategorien gehören:

-   Effektive ACL: ACEs in dieser Kategorie gelten für das-Objekt.
-   ACL erben: ACEs in dieser Kategorie werden von Objekten geerbt, die im Container erstellt werden.

Jeder ACE in der DACL kann zu einer oder mehreren Kategorien gehören. Die Kategorien, zu denen ein ACE gehört, werden durch die im ACE festgelegten vererbungssteuerungflags festgelegt.

In der [**AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) -Eigenschaft eines ACE können drei Vererbungs kontrollflags festgelegt werden.



| Flag                                          | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ADS- \_ aceflag \_ erben \_**                | Dieses Flag gibt an, dass der ACE Teil der erbt-ACL ist und dass untergeordnete Objekte die Vererbungs kontrollenflags dieses ACE erben.                                                                                                                                                                                                                                                                                                                         |
| **ADS- \_ aceflag \_ No \_ propagieren- \_ \_ ACE** | Dieses Flag gibt an, dass der ACE Teil der erbt-ACL ist, aber dass keine Vererbungs kontrollflags an direkte untergeordnete Objekte weitergegeben werden (direkte Nachfolger) und der ACE für die direkt untergeordneten Objekte wirksam ist.                                                                                                                                                                                                                                          |
| **ADS- \_ aceflag \_ \_ nur von \_ ACE erben**          | Dieses Flag gibt an, dass der ACE nicht Teil einer effektiven ACL ist. Wenn dieses Flag nicht festgelegt ist, ist der ACE Teil der effektiven ACL. Dieses Flag eignet sich für das Festlegen von Berechtigungen, die durch unter Objekte vererbbar sind, aber keine Auswirkungen auf den Zugriff auf den Container haben. Wenn z. b. ein ACE von Benutzer Objekten in einer Organisationseinheit geerbt werden soll, ist es wahrscheinlich, dass er nicht für den Zugriff auf die Organisationseinheit selbst erzwungen werden soll.<br/> |



 

Die Werbeeinblendungen "keine Weitergabe **\_ \_ \_ \_ erben \_** " und " **ADS \_ aceflag" \_ erben \_ nur die \_ ACE** -Flags sind nur dann sinnvoll, wenn die Werbeeinblendungen " **\_ \_ \_ ACE erben** " Dies liegt daran, dass das Flag " **ADS \_ aceflag \_ \_** Vererbung" das Vererbungs Verhalten zu einem vererbbaren ACE hinzufügt, aber nicht den Vererbungstyp definiert. Der **ADS- \_ aceflag \_ No \_ propagierungsace \_ \_** und **ADS \_ aceflag \_ erben \_ nur die \_ ACE** -Flags, die einen bestimmten Typ von Vererbungs Verhalten definieren.

Beachten Sie, dass das System auch die folgenden Flags basierend auf dem Typ und Zustand des ACE festlegt.



| Flag                                    | Beschreibung                                           |
|-----------------------------------------|-------------------------------------------------------|
| **von AD \_ EFLAG \_ geerbte \_ ACE**        | Dieses Flag gibt an, dass der ACE geerbt wurde.       |
| **gültige erstellungsflags für ADS- \_ aceflag \_ \_ \_** | Dieses Flag gibt an, dass die Vererbungsflags gültig sind. |



 

In der folgenden Tabelle sind die Auswirkungen der verschiedenen Flag-Kombinationen für die [**AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) -Eigenschaft eines ACE aufgeführt.



| Flag                                                                                                                    | Auswirkung auf das Objekt, das den ACE enthält                     | Auswirkung auf direkt untergeordnete Objekte                                                      | Auswirkung auf Objekte unterhalb von direkt untergeordneten Elementen               |
|-------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|-------------------------------------------------------------------------------------|-------------------------------------------------------|
| Keine Flags festgelegt.                                                                                                           | Effektive ACE: ACE gilt für das-Objekt.               | ACE wird nicht geerbt.                                                               | ACE wird nicht geerbt.                                 |
| **ADS- \_ aceflag \_ erben \_**                                                                                          | Effektiver ACE                                           | ACE wird geerbt. ACE ist ein effektiver ACE.<br/>                               | ACE wird geerbt. ACE ist ein effektiver ACE.<br/> |
| **Anzeigen \_ aceflag \_ erben \_ ACE** \| **ADS \_ aceflag \_ \_ nur \_ ACE erben**                                                  | Kein effektiver ACE: ACE gilt nicht für das Objekt. | ACE wird geerbt. ACE ist ein effektiver ACE.<br/>                               | ACE wird geerbt. ACE ist ein effektiver ACE.<br/> |
| **Anzeigen \_ aceflag \_ erben \_** ACE \| **ADS \_ aceflag \_ No \_ propagieren \_ \_ ACE**                                         | Effektiver ACE                                           | ACE ist geerbt, aber ohne Vererbungsflags. ACE ist ein effektiver ACE<br/>  | ACE wird nicht geerbt.                                 |
| **Anzeigen \_ aceflag \_ Erben der \_ ACE** -Werbeeinblendungen erbt \| **\_ \_ \_ nur \_ ACE** \| **ADS \_ aceflag \_ No \_ propagieren- \_ \_ ACE** | Kein effektiver ACE.                                   | ACE ist geerbt, aber ohne Vererbungsflags. ACE ist ein effektiver ACE.<br/> | ACE wird nicht geerbt.                                 |



 

 

