---
description: Das System lädt einen Zeit Anbieter basierend auf seinen Konfigurationsinformationen, die in der Registrierung gespeichert sind.
ms.assetid: 67f79c31-9dd7-4e3f-bfe1-701b10611f91
title: Registrieren eines Zeit Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a98e5e516db6b2c800c917c5e47da9bd75ba5c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865707"
---
# <a name="registering-a-time-provider"></a>Registrieren eines Zeit Anbieters

Das System lädt einen Zeit Anbieter basierend auf seinen Konfigurationsinformationen, die in der Registrierung gespeichert sind. Jedes Mal, wenn der Anbieter den folgenden Registrierungsschlüssel erstellen sollte:

**HKEY \_ Lokales \_ Computer \\ System** \\ **CurrentControlSet** \\ **Services** \\ **W32Time** \\ **Zeit Anbieter** \\ *providerName*

In der folgenden Tabelle werden die Werte beschrieben, die im Schlüssel jedes Anbieters vorhanden sein müssen.



| Wert             | BESCHREIBUNG                                                                                                                                                                                                              |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **DllName**       | Der Name der dll, die den Anbieter enthält. Dieser Wert weist den Typ **reg \_ SZ** auf.                                                                                                                                     |
| **Aktiviert**       | Gibt an, ob der Anbieter gestartet werden soll. Wenn dieser Wert 1 ist, wird der Anbieter gestartet. Andernfalls wird der Anbieter nicht gestartet. Dieser Wert weist den Typ " **reg \_ DWORD**" auf.                                           |
| **InputProvider** | Gibt an, ob der Anbieter ein Eingabe-oder Ausgabe Anbieter ist. Wenn dieser Wert 1 ist, ist der Anbieter ein Eingabe Anbieter. Andernfalls ist der Anbieter ein Ausgabe Anbieter. Dieser Wert weist den Typ " **reg \_ DWORD**" auf. |



 

Der Zeit Anbieter-Manager listet die Schlüssel unter dem Schlüssel **timeproviders** auf und startet jeden aktivierten Anbieter. Anbieter werden beim Systemstart gestartet und immer dann, wenn Parameter geändert werden.

Jeder Anbieter kann auch anwendungsspezifische Konfigurationsinformationen in der Registrierung speichern.

 

 



