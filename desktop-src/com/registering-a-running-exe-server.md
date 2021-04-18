---
title: Registrieren eines ausführenden exe-Servers
description: Registrieren eines ausführenden exe-Servers
ms.assetid: 277f44bb-72b7-4409-955d-2cd53bc99467
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0c6cae15818e5cdb3931f71f0d4be1ac1baef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310832"
---
# <a name="registering-a-running-exe-server"></a><span data-ttu-id="96587-103">Registrieren eines ausführenden exe-Servers</span><span class="sxs-lookup"><span data-stu-id="96587-103">Registering a Running EXE Server</span></span>

<span data-ttu-id="96587-104">Wenn ein ausführbarer (exe-) Server gestartet wird, sollte er [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject)aufrufen, das die CLSID für den Server in der als Klassen Tabelle bezeichneten Tabelle registriert (eine andere Tabelle als die laufende Objekttabelle).</span><span class="sxs-lookup"><span data-stu-id="96587-104">When an executable (EXE) server is launched, it should call [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject), which registers the CLSID for the server in what is called the class table (a different table than the running object table).</span></span> <span data-ttu-id="96587-105">Wenn ein Server in der Klassen Tabelle registriert ist, kann der Dienststeuerungs-Manager (Service Control Manager, SCM) bestimmen, dass es nicht erforderlich ist, die Klasse erneut zu starten, da der Server bereits ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="96587-105">When a server is registered in the class table, it allows the service control manager (SCM) to determine that it is not necessary to launch the class again, because the server is already running.</span></span> <span data-ttu-id="96587-106">Nur wenn der Server nicht in der Klassen Tabelle aufgeführt ist, überprüft der SCM die Registrierung auf entsprechende Werte und startet den Server, der der angegebenen CLSID zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="96587-106">Only if the server is not listed in the class table will the SCM check the registry for appropriate values and launch the server associated with the given CLSID.</span></span>

<span data-ttu-id="96587-107">Sie übergeben [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) die CLSID für die Klasse und einen Zeiger auf die [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="96587-107">You pass [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) the CLSID for the class and a pointer to its [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="96587-108">Clients, die anschließend [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) mit dieser CLSID aufrufen, rufen einen Zeiger auf die angeforderte Schnittstelle ab, sofern Sie von der Sicherheit nicht unterbunden wird.</span><span class="sxs-lookup"><span data-stu-id="96587-108">Clients who subsequently call [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) with this CLSID will retrieve a pointer to their requested interface, as long as security does not forbid it.</span></span> <span data-ttu-id="96587-109">(Eine Beschreibung mehrerer Instanzen Erstellungs-und Aktivierungs Funktionen finden Sie unter [Hilfsfunktionen](instance-creation-helper-functions.md) für die Instanzerstellung.)</span><span class="sxs-lookup"><span data-stu-id="96587-109">(See [Instance Creation Helper Functions](instance-creation-helper-functions.md) for a description of several instance creation and activation functions.)</span></span>

<span data-ttu-id="96587-110">Der Server für ein Klassenobjekt sollte [**CoRevokeClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject) zum Widerrufen des Klassen Objekts (Entfernen der Registrierung) abrufen, wenn Folgendes zutrifft:</span><span class="sxs-lookup"><span data-stu-id="96587-110">The server for a class object should call [**CoRevokeClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject) to revoke the class object (remove its registration) when all of the following are true:</span></span>

-   <span data-ttu-id="96587-111">Es sind keine Instanzen der Objektdefinition vorhanden.</span><span class="sxs-lookup"><span data-stu-id="96587-111">There are no existing instances of the object definition.</span></span>
-   <span data-ttu-id="96587-112">Es sind keine Sperren für das Klassenobjekt vorhanden.</span><span class="sxs-lookup"><span data-stu-id="96587-112">There are no locks on the class object.</span></span>
-   <span data-ttu-id="96587-113">Die Anwendung, die Dienste für das Klassenobjekt bereitstellt, befindet sich nicht unter dem Benutzer Steuerelement (für den Benutzer auf der Anzeige nicht sichtbar).</span><span class="sxs-lookup"><span data-stu-id="96587-113">The application providing services to the class object is not under user control (not visible to the user on the display).</span></span>

## <a name="related-topics"></a><span data-ttu-id="96587-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="96587-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96587-115">Installieren von als Dienst Anwendung</span><span class="sxs-lookup"><span data-stu-id="96587-115">Installing as a Service Application</span></span>](installing-as-a-service-application.md)
</dt> <dt>

[<span data-ttu-id="96587-116">Registrieren einer Klasse bei der Installation</span><span class="sxs-lookup"><span data-stu-id="96587-116">Registering a Class at Installation</span></span>](registering-a-class-at-installation.md)
</dt> <dt>

[<span data-ttu-id="96587-117">Registrieren von Objekten in der rot</span><span class="sxs-lookup"><span data-stu-id="96587-117">Registering Objects in the ROT</span></span>](registering-objects-in-the-rot.md)
</dt> <dt>

[<span data-ttu-id="96587-118">Selbstregistrierung</span><span class="sxs-lookup"><span data-stu-id="96587-118">Self-Registration</span></span>](self-registration.md)
</dt> </dl>

 

 




