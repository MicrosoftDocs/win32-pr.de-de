---
description: Der SCM verwaltet eine Datenbank installierter Dienste in der Registrierung.
ms.assetid: 70f24e15-2607-4c32-9192-a9413b74558b
title: Datenbank der installierten Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d24a92712d6713e2ca31dbc4b768e3b7c2983ffc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960443"
---
# <a name="database-of-installed-services"></a>Datenbank der installierten Dienste

Der SCM verwaltet eine Datenbank installierter Dienste in der Registrierung. Die-Datenbank wird von SCM und Programmen verwendet, die Dienste hinzufügen, ändern oder konfigurieren. Im folgenden finden Sie den Registrierungsschlüssel für diese Datenbank: **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services**.

Dieser Schlüssel enthält einen Unterschlüssel für jeden installierten Dienst und Treiber Dienst. Der Name des unter Schlüssels ist der Name des Diensts, der durch die Funktion "" von der Funktion "Funktion" [**bei der Installation**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) des Diensts durch ein Dienst Konfigurationsprogramm angegeben wurde.

Bei der Installation des Systems wird eine erste Kopie der Datenbank erstellt. Die Datenbank enthält Einträge für die Gerätetreiber, die beim Systemstart erforderlich sind. Die-Datenbank enthält die folgenden Informationen zu den einzelnen installierten Dienst-und Treiber Diensten:

-   Der Diensttyp. Dies gibt an, ob der Dienst in einem eigenen Prozess ausgeführt wird oder einen Prozess mit anderen Diensten freigibt. Für Treiber Dienste gibt dies an, ob der Dienst ein Kernel Treiber oder ein Dateisystem Treiber ist.
-   Der Starttyp. Hiermit wird angegeben, ob der Dienst-oder Treiber Dienst beim Systemstart automatisch gestartet wird (Dienst für automatisches Starten) oder ob der SCM ihn startet, wenn er von einem Dienst Steuerungsprogramm (Demand-Start-Dienst) angefordert wird. Der Starttyp kann auch darauf hinweisen, dass der Dienst-oder Treiber Dienst deaktiviert ist. in diesem Fall kann er nicht gestartet werden.
-   Die Fehler Steuerungsebene. Hiermit wird der Schweregrad des Fehlers angegeben, wenn der Dienst-oder Treiber Dienst beim Systemstart nicht gestartet werden kann, und bestimmt die Aktion, die vom Start Programm ausgeführt wird.
-   Der voll qualifizierte Pfad der ausführbaren Datei. Die Dateinamenerweiterung ist. EXE für Dienste und. SYS für Treiber Dienste.
-   Optionale Abhängigkeitsinformationen, die verwendet werden, um die richtige Reihenfolge zum Starten von Diensten oder Treiber Diensten zu bestimmen Für-Dienste können diese Informationen eine Liste der Dienste enthalten, die vom SCM gestartet werden müssen, bevor der angegebene Dienst gestartet werden kann, der Name einer Lade Sortier Gruppe, der der Dienst angehört, und ein Tagbezeichner, der die Start Reihenfolge des Diensts in der Gruppe der Lade Reihenfolge angibt. Für Treiber Dienste umfasst diese Informationen eine Liste der Treiber, die vor dem angegebenen Treiber gestartet werden müssen.
-   Für Dienste, einen optionalen Kontonamen und ein Kennwort. Das Dienstprogramm wird im Kontext dieses Kontos ausgeführt. Wenn kein Konto angegeben ist, wird der Dienst im Kontext des Kontos " [LocalSystem](localsystem-account.md)" ausgeführt.
-   Für Treiber Dienste ein optionaler Treiber Objektname (z. \\ b. Dateisystem- \\ rdr oder \\ Treiber- \\ XNS), der vom e/a-System zum Laden des Gerätetreibers verwendet wird. Wenn kein Name angegeben wird, erstellt das e/a-System einen Standardnamen basierend auf dem Namen des Treiber Dienstanbieter.

> [!Note]  
> Diese Datenbank wird auch als servicesactive Database oder SCM-Datenbank bezeichnet. Sie müssen die vom SCM bereitgestellten Funktionen verwenden, anstatt die Datenbank direkt zu ändern.

 

 

 



