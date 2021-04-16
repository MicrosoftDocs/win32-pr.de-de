---
title: Self-Registration
description: Die Selbstregistrierung ist die Standardmethode, mit der ein Servermodul seine eigenen Registrierungs Vorgänge (Registrierung und Aufhebung der Registrierung) im Modul selbst verpacken kann.
ms.assetid: fb5dcb2b-b0e3-4f37-a8e7-b84b9a265227
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c95d422213b8e33ac89b89408ed95724f0769b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474356"
---
# <a name="self-registration"></a>Self-Registration

Da Komponenten Software weiterhin als Markt wächst, sind mehr und mehr Instanzen vorhanden, in denen ein Benutzer eine neue Softwarekomponente als einzelnes DLL-oder exe-Modul erhält, z. b. Wenn eine neue Komponente von einem Onlinedienst heruntergeladen oder von einem Friend auf einer Diskette empfangen wird. In diesen Fällen ist es nicht praktikabel, dass der Benutzer ein langes Installationsverfahren oder Setup Programm durchlaufen muss. Neben den Lizenzierungs Problemen, die über [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)behandelt werden, erstellt eine Installationsprozedur in der Regel die notwendigen Registrierungseinträge, damit eine Komponente ordnungsgemäß im com-und OLE-Kontext ausgeführt werden kann.

Die Selbstregistrierung ist die Standardmethode, mit der ein Servermodul seine eigenen Registrierungs Vorgänge (Registrierung und Aufhebung der Registrierung) im Modul selbst verpacken kann. Bei Verwendung mit der durch [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)behandelten Lizenzierung kann ein Server zu einem vollständig eigenständigen Modul werden, ohne dass externe Installationsprogramme oder reg-Dateien erforderlich sind.

Alle selbst Registrierungs Module, dll oder exe, sollten zunächst eine "OleSelfRegister"-Zeichenfolge im [stringfileinfo](/windows/desktop/menurc/stringfileinfo-block) -Abschnitt der Versions Informations Ressource enthalten, wie hier gezeigt.

``` syntax
VS_VERSION_INFO VERSIONINFO 
 
 ... 
 
 BEGIN 
   BLOCK "StringFileInfo" 
    BEGIN 
#ifdef UNICODE 
     BLOCK "040904B0" // Lang=US English, CharSet=Unicode 
#else 
     BLOCK "040904E4" // Lang=US English, CharSet=Windows Multilingual 
#endif 
      BEGIN 
       ... 
       VALUE "OLESelfRegister", "\0" 
      END 
 
   ... 
 
   END 
 
 ... 
 
 END 
 
```

Das vorhanden sein dieser Daten ermöglicht allen interessierten Parteien, z. b. einer Anwendung, die diese neue Komponente integrieren möchte, zu bestimmen, ob der Server die Selbstregistrierung unterstützt, ohne zuerst die dll oder exe laden zu müssen.

Wenn der Server in einem dll-Modul verpackt ist, muss die dll die Funktionen [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) und [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)exportieren. Jede Anwendung, die den Server anweisen soll, sich selbst zu registrieren (d. h. alle zugehörigen CLSIDs-und Typbibliotheks-IDs), kann über die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion einen Zeiger auf **DllRegisterServer** abrufen. Innerhalb von **DllRegisterServer** erstellt die dll alle notwendigen Registrierungseinträge, wobei der richtige Pfad zur DLL für alle [InProcServer32](inprocserver32.md) -oder [InprocHandler32](inprochandler32.md) -Einträge gespeichert wird.

Wenn eine Anwendung die Komponente aus dem System entfernen möchte, sollte die Registrierung dieser Komponente durch Aufrufen von [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)aufgehoben werden. In diesem-Befehl entfernt der Server genau die Einträge, die er zuvor in [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)erstellt hat. Der Server sollte nicht blind alle Einträge für seine Klassen entfernen, weil andere Software möglicherweise zusätzliche Einträge, z. b. einen [behandatenschlüssel](treatas.md) , gespeichert hat.

Wenn der Server in ein exe-Modul gepackt ist, wird der exe-Server von der Anwendung, die den Server registrieren möchte, mit dem Befehlszeilenargument **/RegServer** oder **-RegServer** (ohne Beachtung der Groß-/Kleinschreibung) gestartet. Wenn die Registrierung des Servers von der Anwendung aufgehoben werden soll, wird die exe-Datei mit dem Befehlszeilenargument **/unregserver** oder **-unregserver** gestartet. Die selbst Registrierungs-exe erkennt diese Befehlszeilenargumente und ruft die gleichen Vorgänge wie eine DLL in [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)und [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)auf und registriert ihren Modulpfad unter [LocalServer32](localserver32.md) anstelle von **InProcServer32** oder **InprocHandler32**.

Der Server muss den vollständigen Pfad zum Installations Speicherort des dll-oder exe-Moduls für die entsprechenden **InProcServer32**-, **InprocHandler32**-und **LocalServer32** -Schlüssel in der Registrierung registrieren. Der Modulpfad kann problemlos über die [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) -Funktion abgerufen werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Installieren von als Dienst Anwendung](installing-as-a-service-application.md)
</dt> <dt>

[Registrieren einer Klasse bei der Installation](registering-a-class-at-installation.md)
</dt> <dt>

[Registrieren eines ausführenden exe-Servers](registering-a-running-exe-server.md)
</dt> <dt>

[Registrieren von Objekten in der rot](registering-objects-in-the-rot.md)
</dt> </dl>

 

 