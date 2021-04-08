---
description: Anwendungen können einen Teil der Registrierung in einer Datei speichern und dann den Inhalt der Datei wieder in die Registrierung laden.
ms.assetid: a71a564d-934a-46e8-b555-989a6fa82337
title: Registrierungsdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44916618946f6541495186aa5843799c9b864fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959915"
---
# <a name="registry-files"></a>Registrierungsdateien

Anwendungen können einen Teil der Registrierung in einer Datei speichern und dann den Inhalt der Datei wieder in die Registrierung laden. Eine Registrierungsdatei ist nützlich, wenn eine große Datenmenge bearbeitet wird, wenn in der Registrierung viele Einträge erstellt werden oder wenn die Daten transitiv sind und geladen und dann erneut entladen werden müssen. Anwendungen, die Teile der Registrierung sichern und wiederherstellen, verwenden wahrscheinlich Registrierungsdateien.

Um einen Schlüssel und dessen Unterschlüssel und Werte in einer Registrierungsdatei zu speichern, kann eine Anwendung die [**regsavekey**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya) -oder [**regsavekeyex**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa) -Funktion aufrufen.

[**Regsavekey**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya) und [**regsavekeyex**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa) erstellen die Datei mit dem Archiv Attribut. Die Datei wird im aktuellen Verzeichnis des Prozesses für einen lokalen Schlüssel und im Verzeichnis% systemroot% \\ system32 für einen Remote Schlüssel erstellt.

Registrierungsdateien haben die folgenden zwei Formate: Standard und latest. Das Standardformat ist das einzige von Windows 2000 unterstützte Format. Sie wird auch von neueren Versionen von Windows aus Gründen der Abwärtskompatibilität unterstützt. [**Regsavekey**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya) erstellt Dateien im Standardformat.

Das neueste Format wird ab Windows XP unterstützt. Registrierungsdateien, die in diesem Format erstellt werden, können nicht unter Windows 2000 geladen werden. [**Regsavekeyex**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa) kann Registrierungsdateien in beiden Formaten speichern, indem entweder das reg- \_ Standard \_ Format oder das reg Latest-Format angegeben wird \_ \_ . Daher kann es verwendet werden, um Registrierungsdateien, die das Standardformat verwenden, in das aktuelle Format zu konvertieren.

Um die Registrierungsdatei zurück in die Registrierung zu schreiben, kann eine Anwendung die Funktionen [**RegLoadKey**](/windows/desktop/api/Winreg/nf-winreg-regloadkeya), [**RegReplaceKey**](/windows/desktop/api/Winreg/nf-winreg-regreplacekeya)oder [**RegRestoreKey**](/windows/desktop/api/Winreg/nf-winreg-regrestorekeya) wie folgt verwenden.

-   **RegLoadKey** lädt Registrierungsdaten aus einer angegebenen Datei in einen angegebenen Unterschlüssel unter **HKEY \_ Users** oder **HKEY \_ local \_ Machine** auf dem Computer der aufrufenden Anwendung oder auf einem Remote Computer. Die-Funktion erstellt den angegebenen Unterschlüssel, wenn er nicht bereits vorhanden ist. Nach dem Aufrufen dieser Funktion kann eine Anwendung die [**regunloadkey**](/windows/desktop/api/Winreg/nf-winreg-regunloadkeya) -Funktion verwenden, um die Registrierung in Ihrem vorherigen Zustand wiederherzustellen.
-   [**RegReplaceKey**](/windows/desktop/api/Winreg/nf-winreg-regreplacekeya) ersetzt einen Schlüssel und alle seine Unterschlüssel und Werte in der Registrierung durch die Daten, die in einer angegebenen Datei enthalten sind. Die neuen Daten werden wirksam, wenn das System das nächste Mal gestartet wird.
-   [**RegRestoreKey**](/windows/desktop/api/Winreg/nf-winreg-regrestorekeya) lädt Registrierungsdaten aus einer angegebenen Datei in einen angegebenen Schlüssel auf dem Computer der aufrufenden Anwendung oder auf einem Remote Computer. Diese Funktion ersetzt die Unterschlüssel und Werte unterhalb des angegebenen Schlüssels durch die untergeordneten Schlüssel und Werte, die dem Schlüssel der obersten Ebene in der Datei folgen.

Die [**regconnectregistry**](/windows/desktop/api/Winreg/nf-winreg-regconnectregistrya) -Funktion stellt eine Verbindung mit einem vordefinierten Registrierungs Handle auf einem anderen Computer her. Eine Anwendung verwendet diese Funktion hauptsächlich für den Zugriff auf Informationen aus einer Remote Registrierung auf anderen Computern in einer Netzwerkumgebung, die Sie auch über den Registrierungs-Editor verwenden können. Möglicherweise möchten Sie auf eine Remote Registrierung zugreifen, um eine Registrierung zu sichern oder den Netzwerk Zugriff darauf zu regulieren. Beachten Sie, dass Sie über die entsprechenden Berechtigungen für den Zugriff auf eine Remote Registrierung mit dieser Funktion verfügen müssen.

 

 



