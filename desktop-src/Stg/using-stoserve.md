---
title: Verwenden von stoservice
description: Stoservice ist eine DLL, die in erster Linie als com-Server vorgesehen ist.
ms.assetid: 32cb284a-de78-4953-9d8e-5bb87d6d5a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d46dfd4070e9951223e0a498184b8db814c7a43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106342144"
---
# <a name="using-stoserve"></a>Verwenden von stoservice

**Stoservice** ist eine DLL, die in erster Linie als com-Server vorgesehen ist. Obwohl Sie durch Verknüpfen mit dem zugeordneten implizit geladen werden kann. LIB-Datei wird normalerweise nach einem expliziten LoadLibrary-Befehl verwendet, normalerweise aus der com-Funktion [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject). Bei **stoservice** handelt es sich um einen selbst registrierenden Prozess internen Server.

Zur Verwendung von **stoservice** muss ein Client Programm stoservice nicht einschließen. H oder Link zum stoservice. LIB. Ein com-Client von **stoservice** erhält ausschließlich den Zugriff über die CLSID und die com-Dienste seines Objekts. Für **stoservice** ist diese CLSID CLSID \_ dllpaper (in der Datei "papguids" definiert. H im \\ Verzeichnis "Inc.". Das [stoclien](structured-storage-client-sample--stoclien-.md) -Codebeispiel zeigt, wie der Client diesen Zugriff erhält.

Das Makefile, das dieses Beispiel erstellt, registriert den Server automatisch in der Registrierung. Sie können die Selbstregistrierung manuell initiieren, indem Sie den folgenden Befehl an der Eingabeaufforderung im **stoservice** -Verzeichnis ausgeben:

**NMAKE** - **Register**

Dabei wird davon ausgegangen, dass Sie eine Kompilierungs Umgebung eingerichtet haben. Andernfalls können Sie den REGISTER.EXE-Befehl auch direkt an der Eingabeaufforderung aufrufen, während Sie sich im **stoservice** -Verzeichnis befinden.

**..\\ \\register.exeregistrieren** **stoserve.dll**

Diese Registrierungs Befehle erfordern einen vorherigen Build des Register Beispiels in dieser Reihe sowie einen früheren Build STOSERVE.DLL.

In dieser Reihe verwenden Makefiles das REGISTER.EXE-Hilfsprogramm aus dem Register Sample. Aktuelle Versionen des Platform Software Development Kit (SDK) und Visual C++ enthalten ein Dienstprogramm, REGSVR32.EXE, das auf ähnliche Weise zum Registrieren von in-Process-Servern und Marshalling von DLLs verwendet werden kann.

**Stoservice** verwendet viele der Hilfsprogrammklassen und Dienste, die von apputil bereitgestellt werden. Weitere Informationen zu apputil erhalten Sie, wenn Sie den Quellcode der apputil-Bibliothek im gleich geordneten apputil-Verzeichnis untersuchen und im Hauptverzeichnis des Tutorials APPUTIL.HTM.

 

 