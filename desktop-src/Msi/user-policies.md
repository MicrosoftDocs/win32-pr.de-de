---
description: Benutzersystem Richtlinien, die mit dem Windows Installer verwendet werden.
ms.assetid: 74e940a1-dc7c-4ea3-ab62-d118204dac3e
title: Benutzerrichtlinien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26cec4066e4d8267b2750d538e691d91382550fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862035"
---
# <a name="user-policies"></a>Benutzerrichtlinien

Die folgenden Benutzerrichtlinien können unter

**HKEY \_ Aktuelle \_** Richtlinien für Benutzer \\ **Software** \\  \\ **Microsoft** \\ **Windows** \\ **Installer**



| Wertname                                                            | Wert Datentypen          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Alwaysinstallangehoben](alwaysinstallelevated.md)<br/>         | **REG \_ DWORD**<br/> | Wenn dieser Wert auf "1" festgelegt ist und der entsprechende Computer Wert ebenfalls festgelegt ist, wird das Installationsprogramm immer mit erhöhten Rechten installiert.<br/> Andernfalls verwendet das Installationsprogramm erweiterte Berechtigungen, um verwaltete Anwendungen zu installieren, und verwendet die Berechtigungsstufe des aktuellen Benutzers für nicht verwaltete Anwendungen.<br/>                                                                                                                                                                                                      |
| [Disablemedia](disablemedia.md)<br/>                           | **REG \_ DWORD**<br/> | Wenn die [disablemedia](disablemedia.md) -Richtlinie auf "1" festgelegt ist, können Benutzer und Administratoren, die eine Wartungs Installation eines Produkts ausführen, das Dialog Feld "Durchsuchen" nicht zum Durchsuchen von Medienquellen (z. b. CD-ROM) für die Quellen anderer installier barer Produkte verwenden. Das Durchsuchen anderer Produkte wird verhindert, unabhängig davon, ob die Installation erweiterte Berechtigungen hat. Der Benutzer kann das Produkt weiterhin von einem Medium aus neu installieren, wenn der Benutzer über eine ordnungsgemäß bezeichnete Medienquelle verfügt.<br/> |
| [DISABLEROLLBACK](disablerollback.md)<br/>                     | **REG \_ DWORD**<br/> | Wenn dieser Wert auf "1" festgelegt ist, speichert das Installationsprogramm während der Installation keine Rollback-Dateien, und das Installations Rollback wird deaktiviert. Standardmäßig ist das Rollback aktiviert. Administratoren wird empfohlen, diese Richtlinie nicht zu verwenden, es sei denn, Sie ist unbedingt erforderlich.<br/>                                                                                                                                                                                                                                                             |
| [SearchOrder](searchorder.md)<br/>                             | **REG- \_ SZ**<br/>    | Die Reihenfolge, in der das Installationsprogramm die drei unterschiedlichen Arten von Quellen durchsucht:<br/> "n" – Netzwerk<br/> "m" – Medium (CD-ROM oder DVD)<br/> "u" – URL (Uniform Resource Locator)<br/> Beispielsweise weist der Wert "NMU" das Installationsprogramm an, zuerst Netzwerk Quellen, Medienquellen und URL-Quellen zu durchsuchen. Wenn Sie einen Buchstaben verlassen, wird der entsprechende Volumentyp aus der Suche entfernt. Die Standard Reihenfolge, in der dieser Wert nicht vorhanden ist, ist Network First, then Media gefolgt von URL.<br/>          |
| [Transformsatsource-Richtlinie](transformsatsource-policy.md)<br/> | **REG \_ DWORD**<br/> | , Wenn dieser Wert vorhanden und auf "1" festgelegt ist. Das Installationsprogramm sucht im Stammverzeichnis von Netzwerk Quellen in der [**Quell Liste**](sourcelist.md) für das Produkt nach Transformations Dateien. Standardmäßig werden Transformationen im Ordner Anwendungsdaten des Profils eines Benutzers gespeichert.<br/>                                                                                                                                                                                                                                             |



 

 

 




