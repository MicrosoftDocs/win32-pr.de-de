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
# <a name="self-registration"></a><span data-ttu-id="23ff5-103">Self-Registration</span><span class="sxs-lookup"><span data-stu-id="23ff5-103">Self-Registration</span></span>

<span data-ttu-id="23ff5-104">Da Komponenten Software weiterhin als Markt wächst, sind mehr und mehr Instanzen vorhanden, in denen ein Benutzer eine neue Softwarekomponente als einzelnes DLL-oder exe-Modul erhält, z. b. Wenn eine neue Komponente von einem Onlinedienst heruntergeladen oder von einem Friend auf einer Diskette empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="23ff5-104">As component software continues to grow as a market, there will be more and more instances where a user obtains a new software component as a single DLL or EXE module, such as when downloading a new component from an on-line service or receiving one from a friend on a floppy disk.</span></span> <span data-ttu-id="23ff5-105">In diesen Fällen ist es nicht praktikabel, dass der Benutzer ein langes Installationsverfahren oder Setup Programm durchlaufen muss.</span><span class="sxs-lookup"><span data-stu-id="23ff5-105">In these cases, it is not practical to require the user to go through a lengthy installation procedure or setup program.</span></span> <span data-ttu-id="23ff5-106">Neben den Lizenzierungs Problemen, die über [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)behandelt werden, erstellt eine Installationsprozedur in der Regel die notwendigen Registrierungseinträge, damit eine Komponente ordnungsgemäß im com-und OLE-Kontext ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="23ff5-106">Besides the licensing issues, which are handled through [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), an installation procedure typically creates the necessary registry entries for a component to run properly in the COM and OLE context.</span></span>

<span data-ttu-id="23ff5-107">Die Selbstregistrierung ist die Standardmethode, mit der ein Servermodul seine eigenen Registrierungs Vorgänge (Registrierung und Aufhebung der Registrierung) im Modul selbst verpacken kann.</span><span class="sxs-lookup"><span data-stu-id="23ff5-107">Self-registration is the standard means through which a server module can package its own registry operations, both registration and unregistration, into the module itself.</span></span> <span data-ttu-id="23ff5-108">Bei Verwendung mit der durch [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)behandelten Lizenzierung kann ein Server zu einem vollständig eigenständigen Modul werden, ohne dass externe Installationsprogramme oder reg-Dateien erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="23ff5-108">When used with licensing handled through [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), a server can become an entirely self-contained module with no need for external installation programs or .reg files.</span></span>

<span data-ttu-id="23ff5-109">Alle selbst Registrierungs Module, dll oder exe, sollten zunächst eine "OleSelfRegister"-Zeichenfolge im [stringfileinfo](/windows/desktop/menurc/stringfileinfo-block) -Abschnitt der Versions Informations Ressource enthalten, wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="23ff5-109">Any self-registering module, DLL or EXE, should first include an "OleSelfRegister" string in the [StringFileInfo](/windows/desktop/menurc/stringfileinfo-block) section of its version information resource, as shown here.</span></span>

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

<span data-ttu-id="23ff5-110">Das vorhanden sein dieser Daten ermöglicht allen interessierten Parteien, z. b. einer Anwendung, die diese neue Komponente integrieren möchte, zu bestimmen, ob der Server die Selbstregistrierung unterstützt, ohne zuerst die dll oder exe laden zu müssen.</span><span class="sxs-lookup"><span data-stu-id="23ff5-110">The existence of this data allows any interested party, such as an application that wishes to integrate this new component, to determine whether the server supports self-registration without having to load the DLL or EXE first.</span></span>

<span data-ttu-id="23ff5-111">Wenn der Server in einem dll-Modul verpackt ist, muss die dll die Funktionen [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) und [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)exportieren.</span><span class="sxs-lookup"><span data-stu-id="23ff5-111">If the server is packaged in a DLL module, the DLL must export the functions [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span></span> <span data-ttu-id="23ff5-112">Jede Anwendung, die den Server anweisen soll, sich selbst zu registrieren (d. h. alle zugehörigen CLSIDs-und Typbibliotheks-IDs), kann über die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion einen Zeiger auf **DllRegisterServer** abrufen.</span><span class="sxs-lookup"><span data-stu-id="23ff5-112">Any application that wishes to instruct the server to register itself (that is, all its CLSIDs and type library IDs) can obtain a pointer to **DllRegisterServer** through the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) function.</span></span> <span data-ttu-id="23ff5-113">Innerhalb von **DllRegisterServer** erstellt die dll alle notwendigen Registrierungseinträge, wobei der richtige Pfad zur DLL für alle [InProcServer32](inprocserver32.md) -oder [InprocHandler32](inprochandler32.md) -Einträge gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="23ff5-113">Within **DllRegisterServer**, the DLL creates all its necessary registry entries, storing the correct path to the DLL for all [InprocServer32](inprocserver32.md) or [InprocHandler32](inprochandler32.md) entries.</span></span>

<span data-ttu-id="23ff5-114">Wenn eine Anwendung die Komponente aus dem System entfernen möchte, sollte die Registrierung dieser Komponente durch Aufrufen von [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)aufgehoben werden.</span><span class="sxs-lookup"><span data-stu-id="23ff5-114">When an application wishes to remove the component from the system, it should unregister that component by calling [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span></span> <span data-ttu-id="23ff5-115">In diesem-Befehl entfernt der Server genau die Einträge, die er zuvor in [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="23ff5-115">Within this call, the server removes exactly those entries it previously created in [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver).</span></span> <span data-ttu-id="23ff5-116">Der Server sollte nicht blind alle Einträge für seine Klassen entfernen, weil andere Software möglicherweise zusätzliche Einträge, z. b. einen [behandatenschlüssel](treatas.md) , gespeichert hat.</span><span class="sxs-lookup"><span data-stu-id="23ff5-116">The server should not blindly remove all entries for its classes because other software may have stored additional entries, such as a [TreatAs](treatas.md) key.</span></span>

<span data-ttu-id="23ff5-117">Wenn der Server in ein exe-Modul gepackt ist, wird der exe-Server von der Anwendung, die den Server registrieren möchte, mit dem Befehlszeilenargument **/RegServer** oder **-RegServer** (ohne Beachtung der Groß-/Kleinschreibung) gestartet.</span><span class="sxs-lookup"><span data-stu-id="23ff5-117">If the server is packaged in an EXE module, the application wishing to register the server launches the EXE server with the command-line argument **/RegServer** or **-RegServer** (case-insensitive).</span></span> <span data-ttu-id="23ff5-118">Wenn die Registrierung des Servers von der Anwendung aufgehoben werden soll, wird die exe-Datei mit dem Befehlszeilenargument **/unregserver** oder **-unregserver** gestartet.</span><span class="sxs-lookup"><span data-stu-id="23ff5-118">If the application wishes to unregister the server, it launches the EXE with the command-line argument **/UnregServer** or **-UnregServer**.</span></span> <span data-ttu-id="23ff5-119">Die selbst Registrierungs-exe erkennt diese Befehlszeilenargumente und ruft die gleichen Vorgänge wie eine DLL in [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)und [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)auf und registriert ihren Modulpfad unter [LocalServer32](localserver32.md) anstelle von **InProcServer32** oder **InprocHandler32**.</span><span class="sxs-lookup"><span data-stu-id="23ff5-119">The self-registering EXE detects these command-line arguments and invokes the same operations as a DLL would within [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver), respectively, registering its module path under [LocalServer32](localserver32.md) instead of **InprocServer32** or **InprocHandler32**.</span></span>

<span data-ttu-id="23ff5-120">Der Server muss den vollständigen Pfad zum Installations Speicherort des dll-oder exe-Moduls für die entsprechenden **InProcServer32**-, **InprocHandler32**-und **LocalServer32** -Schlüssel in der Registrierung registrieren.</span><span class="sxs-lookup"><span data-stu-id="23ff5-120">The server must register the full path to the installation location of the DLL or EXE module for their respective **InprocServer32**, **InprocHandler32**, and **LocalServer32** keys in the registry.</span></span> <span data-ttu-id="23ff5-121">Der Modulpfad kann problemlos über die [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) -Funktion abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="23ff5-121">The module path is easily obtained through the [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23ff5-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="23ff5-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23ff5-123">Installieren von als Dienst Anwendung</span><span class="sxs-lookup"><span data-stu-id="23ff5-123">Installing as a Service Application</span></span>](installing-as-a-service-application.md)
</dt> <dt>

[<span data-ttu-id="23ff5-124">Registrieren einer Klasse bei der Installation</span><span class="sxs-lookup"><span data-stu-id="23ff5-124">Registering a Class at Installation</span></span>](registering-a-class-at-installation.md)
</dt> <dt>

[<span data-ttu-id="23ff5-125">Registrieren eines ausführenden exe-Servers</span><span class="sxs-lookup"><span data-stu-id="23ff5-125">Registering a Running EXE Server</span></span>](registering-a-running-exe-server.md)
</dt> <dt>

[<span data-ttu-id="23ff5-126">Registrieren von Objekten in der rot</span><span class="sxs-lookup"><span data-stu-id="23ff5-126">Registering Objects in the ROT</span></span>](registering-objects-in-the-rot.md)
</dt> </dl>

 

 