---
description: Anwendungen können einen Teil der Registrierung in einer Datei speichern und dann den Inhalt der Datei wieder in die Registrierung laden.
ms.assetid: a71a564d-934a-46e8-b555-989a6fa82337
title: Registrierungsdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a5caa34a075e4bffe48a542d02eec896ab28dd93fbdc2745dbc5a08effb9d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763813"
---
# <a name="registry-files"></a>Registrierungsdateien

Anwendungen können einen Teil der Registrierung in einer Datei speichern und dann den Inhalt der Datei wieder in die Registrierung laden. Eine Registrierungsdatei ist nützlich, wenn eine große Datenmenge bearbeitet wird, wenn viele Einträge in der Registrierung vorgenommen werden oder wenn die Daten vorübergehend sind und geladen und dann erneut entladen werden müssen. Anwendungen, die Teile der Registrierung sichern und wiederherstellen, verwenden wahrscheinlich Registrierungsdateien.

Um einen Schlüssel und seine Unterschlüssel und Werte in einer Registrierungsdatei zu speichern, kann eine Anwendung die [**RegSaveKey-**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya) oder [**RegSaveKeyEx-Funktion**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa) aufrufen.

[**RegSaveKey und**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya) [**RegSaveKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa) erstellen die Datei mit dem Archivattribut. Die Datei wird im aktuellen Verzeichnis des Prozesses für einen lokalen Schlüssel und im Verzeichnis %systemroot% \\ system32 für einen Remoteschlüssel erstellt.

Registrierungsdateien haben die folgenden beiden Formate: standard und latest. Das Standardformat ist das einzige Format, das von Windows 2000 unterstützt wird. Sie wird aus Gründen der Abwärtskompatibilität auch von Windows Versionen von unterstützt. [**RegSaveKey**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya) erstellt Dateien im Standardformat.

Das neueste Format wird ab xp Windows unterstützt. Registrierungsdateien, die in diesem Format erstellt werden, können nicht auf Windows 2000 geladen werden. [**RegSaveKeyEx kann**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa) Registrierungsdateien in beiden Formaten speichern, indem entweder REG \_ STANDARD FORMAT oder REG LATEST FORMAT angegeben \_ \_ \_ wird. Daher kann es verwendet werden, um Registrierungsdateien, die das Standardformat verwenden, in das neueste Format zu konvertieren.

Um die Registrierungsdatei zurück in die Registrierung zu schreiben, kann eine Anwendung die [**RegLoadKey-,**](/windows/desktop/api/Winreg/nf-winreg-regloadkeya) [**RegReplaceKey-**](/windows/desktop/api/Winreg/nf-winreg-regreplacekeya)oder [**RegRestoreKey-Funktionen**](/windows/desktop/api/Winreg/nf-winreg-regrestorekeya) wie folgt verwenden.

-   **RegLoadKey** lädt Registrierungsdaten aus einer angegebenen Datei in einen angegebenen Unterschlüssel unter **HKEY \_ USERS** oder **HKEY \_ LOCAL \_ MACHINE** auf dem Computer der aufrufenden Anwendung oder auf einem Remotecomputer. Die Funktion erstellt den angegebenen Unterschlüssel, wenn er noch nicht vorhanden ist. Nach dem Aufrufen dieser Funktion kann eine Anwendung die [**RegUnLoadKey-Funktion**](/windows/desktop/api/Winreg/nf-winreg-regunloadkeya) verwenden, um den vorherigen Zustand der Registrierung wiederherzustellen.
-   [**RegReplaceKey**](/windows/desktop/api/Winreg/nf-winreg-regreplacekeya) ersetzt einen Schlüssel und alle seine Unterschlüssel und Werte in der Registrierung durch die In einer angegebenen Datei enthaltenen Daten. Die neuen Daten werden wirksam, wenn das System das nächste Mal gestartet wird.
-   [**RegRestoreKey lädt**](/windows/desktop/api/Winreg/nf-winreg-regrestorekeya) Registrierungsdaten aus einer angegebenen Datei in einen angegebenen Schlüssel auf dem Computer der aufrufenden Anwendung oder auf einem Remotecomputer. Diese Funktion ersetzt die Unterschlüssel und Werte unterhalb des angegebenen Schlüssels durch die Unterschlüssel und Werte, die dem Schlüssel der obersten Ebene in der Datei folgen.

Die [**RegConnectRegistry-Funktion**](/windows/desktop/api/Winreg/nf-winreg-regconnectregistrya) stellt eine Verbindung mit einem vordefinierten Registrierungshand handle auf einem anderen Computer her. Eine Anwendung verwendet diese Funktion in erster Linie für den Zugriff auf Informationen aus einer Remoteregistrierung auf anderen Computern in einer Netzwerkumgebung. Dies ist auch über den Registrierungs-Editor der Fall. Möglicherweise möchten Sie auf eine Remoteregistrierung zugreifen, um eine Registrierung zu sichern oder den Netzwerkzugriff darauf zu steuern. Beachten Sie, dass Sie über die entsprechenden Berechtigungen für den Zugriff auf eine Remoteregistrierung mit dieser Funktion verfügen müssen.

 

 



