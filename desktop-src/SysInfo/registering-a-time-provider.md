---
description: Das System lädt einen Zeitanbieter basierend auf den in der Registrierung gespeicherten Konfigurationsinformationen.
ms.assetid: 67f79c31-9dd7-4e3f-bfe1-701b10611f91
title: Registrieren eines Zeitanbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eeb7bce1370e443eaf3eb42d78cdfd058cf2c38147da038de1e921d85e957f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763925"
---
# <a name="registering-a-time-provider"></a>Registrieren eines Zeitanbieters

Das System lädt einen Zeitanbieter basierend auf den in der Registrierung gespeicherten Konfigurationsinformationen. Jedes Mal, wenn der Anbieter den folgenden Registrierungsschlüssel erstellen sollte:

**HKEY \_ LOCAL \_ MACHINE \\ System** \\ **CurrentControlSet** \\ **Services** \\ **W32Time** \\ **TimeProviders** \\ *ProviderName*

In der folgenden Tabelle werden die Werte beschrieben, die im Schlüssel jedes Anbieters vorhanden sein müssen.



| Wert             | Beschreibung                                                                                                                                                                                                              |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **DllName**       | Der Name der DLL, die den Anbieter enthält. Dieser Wert weist den Typ **REG \_ SZ** auf.                                                                                                                                     |
| **Aktiviert**       | Gibt an, ob der Anbieter gestartet werden soll. Wenn dieser Wert 1 ist, wird der Anbieter gestartet. Andernfalls wird der Anbieter nicht gestartet. Dieser Wert weist den Typ **REG \_ DWORD** auf.                                           |
| **InputProvider** | Gibt an, ob der Anbieter ein Eingabeanbieter oder ein Ausgabeanbieter ist. Wenn dieser Wert 1 ist, ist der Anbieter ein Eingabeanbieter. Andernfalls ist der Anbieter ein Ausgabeanbieter. Dieser Wert weist den Typ **REG \_ DWORD** auf. |



 

Der Zeitanbieter-Manager listet die Schlüssel unter dem **TimeProviders-Schlüssel** auf und startet jeden aktivierten Anbieter. Anbieter werden beim Systemstart und immer dann gestartet, wenn Parameteränderungen vorgenommen werden.

Jeder Anbieter kann auch anwendungsspezifische Konfigurationsinformationen in der Registrierung speichern.

 

 



