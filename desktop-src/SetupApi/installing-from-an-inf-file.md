---
description: Nachdem Sie Installationsinformationen aus einer INF-Datei abgerufen haben, gibt es mehrere Funktionen zur Dateibehandlung, mit denen Sie die in einem INF-Abschnitt aufgeführten Dateien installieren können.
ms.assetid: 4e6042a0-36a9-4f74-b6cc-554e7f7aa2d9
title: Installieren aus einer INF-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e32780855e126eaaa38ae937a265951711662434e90ab0ffb425e2e4f4f6c42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867570"
---
# <a name="installing-from-an-inf-file"></a>Installieren aus einer INF-Datei

Nachdem Sie Installationsinformationen aus einer INF-Datei abgerufen haben, gibt es mehrere Funktionen zur Dateibehandlung, mit denen Sie die in einem INF-Abschnitt aufgeführten Dateien installieren können. Funktionen auf niedriger Ebene wie [**SetupInstallFile und**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea) [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa) installieren eine einzelne Datei.

Es gibt auch Funktionen zum Verarbeiten komprimierter Dateien. Die [**SetupGetFileCompressionInfo-Funktion gibt**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfilecompressioninfoa) Informationen zu komprimierten Dateien zurück. Diese Informationen können dann von [**SetupDecompressOrCopyFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupdecompressorcopyfilea) verwendet werden, um die Datei zu kopieren und bei Bedarf zu erweitern.

Funktionen auf hoher Ebene wie [**SetupInstallFromInfSection,**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona)und [**SetupInstallServicesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectiona) verarbeiten die Installationsvorgänge in einem Installations- oder **Dienstabschnitt.**  Davon ist **SetupInstallFromInfSection** am vielseitigsten, da es jede Art  von Installationsvorgang ausführen kann, der im Abschnitt Installieren einer INF-Datei aufgeführt ist. Dies schließt die Registrierungs- und INI-Vorgänge ein, die in den Zeilen **AddReg,** **DelReg,** **UpdateInis** oder **UpdateIniField** eines **Install-Abschnitts aufgeführt** sind.

Die [**Funktionen SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona) und [**SetupInstallServicesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectiona) stellen  Vorgänge aus einem **Installations-** bzw. Dienstabschnitt in eine vorhandene Dateiwarteschlange ein. Beachten Sie, dass Sie SetupInstallFromInfSection und SetupInstallServicesFromInfSection separat aufrufen müssen, um Vorgänge und Dienste in die Warteschlange zu stellen. Weitere Informationen finden Sie unter [Dateiwarteschlangen.](file-queues.md)

Im Gegensatz dazu erstellt und zerstört die [**SetupInstallFromInfSection-Funktion**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) ihre eigene interne Warteschlange. Eine gängige Verwendung von **SetupInstallFromInfSection** ist das Aufrufen, nachdem alle Dateien erfolgreich kopiert wurden, um die Registrierung und INI-Transaktionen durchzuführen.

In Windows 2000 können DLL-Dateien selbst registriert werden, indem [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) für eine INF-Datei  aufruft, die die **RegisterDlls-Direktive** im Abschnitt Installieren enthält. **SetupInstallFromInfSection** kann auch 32-Bit-DLLs aus einem 64-Bit-Prozess selbst registrieren.

Unter 64-Bit-Betriebssystemen kann [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) aufgerufen werden, um Vorgänge für den 32-Bit-Teil der Registrierung durchzuführen. Um dem 32-Bit-Teil der Registrierung einen Registrierungsschlüssel hinzuzufügen, schließen Sie das FLG \_ ADDREG \_ 32BITKEY-Flag in die **Zeile AddReg** der INF ein. Wenn Sie einen Registrierungsschlüssel nur im 32-Bit-Teil der Registrierung löschen möchten, schließen Sie den FLG \_ DELREG \_ 32BITKEY-Schlüssel in die **Zeile DelReg** ein. Wenn Sie einen Binärwert nur im 32-Bit-Teil der Registrierung festlegen oder löschen, schließen Sie FLG \_ BITREG \_ 32BITKEY in die **BitReg-Zeile** ein.

Zusätzlich zu den zuvor aufgeführten Funktionen enthält die Setup-API Funktionen, die Dateiinstallationsvorgänge in die Warteschlange stellen, entweder nach Datei oder nach INF-Abschnitt. Weitere Informationen finden Sie unter [Dateiwarteschlangen.](file-queues.md)

 

 



