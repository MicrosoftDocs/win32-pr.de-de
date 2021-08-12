---
description: Benutzersystemrichtlinien, die mit dem Windows Installer verwendet werden.
ms.assetid: 74e940a1-dc7c-4ea3-ab62-d118204dac3e
title: Benutzerrichtlinien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ce52f4a691729c71ed57ddba8dd80811681844e1ba6c02664ee50c11f8d0e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118623089"
---
# <a name="user-policies"></a>Benutzerrichtlinien

Die folgenden Benutzerrichtlinien können unter konfiguriert werden.

**HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**



| Wertname                                                            | Wertdatentypen          | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AlwaysInstallElevated](alwaysinstallelevated.md)<br/>         | **REG \_ DWORD**<br/> | Wenn dieser Wert auf "1" festgelegt ist und auch der entsprechende Computerwert festgelegt ist, wird das Installationsprogramm immer mit erhöhten Rechten installiert.<br/> Andernfalls verwendet das Installationsprogramm erhöhte Rechte, um verwaltete Anwendungen zu installieren, und verwendet die Berechtigungsstufe des aktuellen Benutzers für nicht verwaltete Anwendungen.<br/>                                                                                                                                                                                                      |
| [DisableMedia](disablemedia.md)<br/>                           | **REG \_ DWORD**<br/> | Wenn die [DisableMedia-Richtlinie](disablemedia.md) auf "1" festgelegt ist, werden Benutzer und Administratoren, die eine Wartungsinstallation eines Produkts ausführen, daran gehindert, das Dialogfeld Durchsuchen zum Durchsuchen von Medienquellen wie CD-ROM für die Quellen anderer installierbarer Produkte zu verwenden. Das Suchen nach anderen Produkten wird unabhängig davon verhindert, ob die Installation über erhöhte Rechte verfügt. Es ist weiterhin möglich, dass der Benutzer das Produkt über Medien neu installiert, wenn der Benutzer über eine ordnungsgemäß bezeichnete Medienquelle verfügt.<br/> |
| [DisableRollback](disablerollback.md)<br/>                     | **REG \_ DWORD**<br/> | Wenn dieser Wert auf "1" festgelegt ist, speichert das Installationsprogramm während der Installation keine Rollbackdateien, wodurch das Installationsrollback deaktiviert wird. Standardmäßig ist das Rollback aktiviert. Administratoren wird empfohlen, diese Richtlinie nur zu verwenden, wenn sie unbedingt erforderlich ist.<br/>                                                                                                                                                                                                                                                             |
| [SearchOrder](searchorder.md)<br/>                             | **REG \_ SZ**<br/>    | Reihenfolge, in der das Installationsprogramm die drei verschiedenen Arten von Quellen durchsucht:<br/> "n": Netzwerk<br/> "m": Medien (CD-ROM oder DVD)<br/> "u": URL (Uniform Resource Locator)<br/> Beispielsweise weist der Wert "nmu" das Installationsprogramm an, zuerst Netzwerkquellen, dann Medienquellen an zweiter Stelle und zuletzt URL-Quellen zu durchsuchen. Wenn Sie einen Buchstaben weglassen, wird der entsprechende Volumetyp aus der Suche entfernt. Die Standardreihenfolge ohne diesen Wert lautet network first und dann media gefolgt von URL.<br/>          |
| [TransformsAtSource-Richtlinie](transformsatsource-policy.md)<br/> | **REG \_ DWORD**<br/> | Wenn dieser Wert vorhanden ist und auf "1" festgelegt ist, Das Installationsprogramm sucht im Stammverzeichnis aller Netzwerkquellen in der [**Quellliste**](sourcelist.md) für das Produkt nach Transformationsdateien. Standardmäßig werden Transformationen im Ordner Anwendungsdaten des Profils eines Benutzers gespeichert.<br/>                                                                                                                                                                                                                                             |



 

 

 




