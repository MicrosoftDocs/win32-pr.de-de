---
title: Verwenden von StoServe
description: StoServe ist eine DLL, die hauptsächlich als COM-Server vorgesehen ist.
ms.assetid: 32cb284a-de78-4953-9d8e-5bb87d6d5a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e3a220f03e17892b02a94c1e76bafc4a869c0922973c7277589627d233175a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034750"
---
# <a name="using-stoserve"></a>Verwenden von StoServe

**StoServe ist** eine DLL, die hauptsächlich als COM-Server vorgesehen ist. Obwohl es implizit geladen werden kann, indem eine Verknüpfung mit dem zugeordneten -Typ verwendet wird. LIB-Datei wird normalerweise nach einem expliziten LoadLibrary-Aufruf verwendet, normalerweise innerhalb der COM-Funktion [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject). **StoServe ist** ein Selbstregistrierungs-In-Process-Server.

Um **StoServe verwenden zu** können, muss ein Clientprogramm STOSERVE nicht enthalten. H oder Link zu STOSERVE. Lib. Ein COM-Client **von StoServe** erhält den Zugriff ausschließlich über die CLSID- und COM-Dienste seines Objekts. Für **StoServe ist** diese CLSID CLSID \_ DllPaper (definiert in der Datei PAPGUIDS. H im verzeichnis der \\ gleichgeordneten INC-Elemente). Das [StoClien-Codebeispiel](structured-storage-client-sample--stoclien-.md) zeigt, wie der Client diesen Zugriff erhält.

Das Makefile, das dieses Beispiel erstellt, registriert den Server automatisch in der Registrierung. Sie können die Selbstregistrierung manuell initiieren, indem Sie den folgenden Befehl an der Eingabeaufforderung im **StoServe-Verzeichnis** ausführen:

**nmake** **register**

Dabei wird davon ausgegangen, dass Sie eine Kompilierungsumgebung eingerichtet haben. Falls nicht, können Sie den Befehl REGISTER.EXE direkt an der Eingabeaufforderung aufrufen, während Sie sich im **StoServe-Verzeichnis** befinden.

**..\\ registrieren \\register.exe** **stoserve.dll**

Diese Registrierungsbefehle erfordern einen vorherigen Build des REGISTER-Beispiels in dieser Reihe sowie einen vorherigen Build STOSERVE.DLL.

In dieser Reihe verwenden die Makefiles REGISTER.EXE Hilfsprogramm aus dem REGISTER-Beispiel. Aktuelle Releases des Platform Software Development Kit (SDK) und Visual C++ enthalten das Hilfsprogramm REGSVR32.EXE, das auf ähnliche Weise verwendet werden kann, um Prozessserver zu registrieren und DLLs zu marshallen.

**StoServe verwendet** viele der Hilfsprogrammklassen und -dienste, die von APPUTIL bereitgestellt werden. Weitere Informationen zu APPUTIL finden Sie im Quellcode der APPUTIL-Bibliothek im nebengeordneten Verzeichnis APPUTIL, und APPUTIL.HTM im Hauptverzeichnis des Tutorials.

 

 