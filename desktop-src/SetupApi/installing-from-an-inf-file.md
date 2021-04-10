---
description: Nachdem Sie die Installationsinformationen aus einer INF-Datei abgerufen haben, können Sie die Dateien, die in einem INF-Abschnitt aufgelistet sind, mit mehreren Datei Behandlungs Funktionen installieren.
ms.assetid: 4e6042a0-36a9-4f74-b6cc-554e7f7aa2d9
title: Installieren aus einer INF-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bc3642edfb7abc2864c2c0784c79fbb21612fb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866936"
---
# <a name="installing-from-an-inf-file"></a>Installieren aus einer INF-Datei

Nachdem Sie die Installationsinformationen aus einer INF-Datei abgerufen haben, können Sie die Dateien, die in einem INF-Abschnitt aufgelistet sind, mit mehreren Datei Behandlungs Funktionen installieren. Funktionen auf niedriger Ebene, wie z. b. " [**setupinstallfile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea) " und " [**setupinstallfileex**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa) ", installieren eine einzelne Datei.

Es gibt auch Funktionen zum Verarbeiten komprimierter Dateien. Die [**setupgetfilecompressioninfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfilecompressioninfoa) -Funktion gibt Informationen über komprimierte Dateien zurück. Diese Informationen können dann von [**setupdecompressorcopyfile**](/windows/desktop/api/Setupapi/nf-setupapi-setupdecompressorcopyfilea) verwendet werden, um die Datei zu kopieren und ggf. zu erweitern.

Allgemeine Funktionen wie " [**setupinstallfrominfsection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)", " [**setupinstallfilesfrominfsection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona)" und " [**setupinstallservicesfrominfsection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectiona) " verarbeiten die Installations Vorgänge in einem Abschnitt " **install** " oder " **Service** ". Dabei ist **setupinstallfrominlosection** die vielseitigste, da Sie jede Art von Installationsvorgang ausführen kann, die im Abschnitt **Installieren** einer INF-Datei aufgeführt ist. Dies umfasst die Registrierungs-und ini-Vorgänge, die in den Zeilen " **adressg**", " **Delta**", " **UpdateInis**" oder " **updateinifield** " eines **Installations** Abschnitts aufgeführt sind.

Die Funktionen " [**setupinstallfilesfrominfsection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona) " und " [**setupinstallservicesfrominfsection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectiona) " stellen Warteschlangen Vorgänge aus einem **Installations** -oder **Dienst** Abschnitt in eine vorhandene Datei Warteschlange. Beachten Sie, dass Sie setupinstallfrominfsection und setupinstallservicesfrominfsection separat aufrufen müssen, um Vorgänge und Dienste in die Warteschlange zu stellen. Weitere Informationen finden Sie unter [Datei Warteschlangen](file-queues.md).

Im Gegensatz dazu erstellt und zerstört die [**setupinstallfrominf section**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) -Funktion die eigene interne Warteschlange. Eine häufige Verwendung von **setupinstallfrominfsection** besteht darin, Sie aufzurufen, nachdem alle Dateien erfolgreich kopiert wurden, um die Registrierungs-und ini-Transaktionen auszuführen.

Unter Windows 2000 können DLL-Dateien selbst registriert werden, indem [**setupinstallfrominfsection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) für eine INF-Datei aufgerufen wird, die die **RegisterDLLs** -Direktive im **Installations** Abschnitt enthält. **Setupinstallfrominlosection** kann auch 32-Bit-DLLs von einem 64-Bit-Prozess selbst registrieren.

Auf 64-Bit-Betriebssystemen kann [**setupinstallfrominfsection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) aufgerufen werden, um Vorgänge für den 32-Bit-Teil der Registrierung auszuführen. Wenn Sie dem 32-Bit-Teil der Registrierung einen Registrierungsschlüssel hinzufügen möchten, schließen Sie das FLG \_ \_ adressflag 32bitkey in die **adressg** -Zeile der INF ein. Wenn Sie einen Registrierungsschlüssel nur im 32-Bit-Teil der Registrierung löschen möchten, schließen Sie den FLG- \_ Schlüssel "Delta- \_ 32bitkey" in die **Delta** -Zeile ein. Um einen binären Wert nur im 32-Bit-Bereich der Registrierung festzulegen oder zu löschen, fügen Sie den FLG \_ bitreg \_ 32bitkey in die **bitreg** -Zeile ein.

Zusätzlich zu den zuvor aufgeführten Funktionen enthält die Setup-API Funktionen, die Datei Installations Vorgänge in die Warteschlange stellen, entweder nach Datei oder nach inf. Weitere Informationen finden Sie unter [Datei Warteschlangen](file-queues.md).

 

 



