---
description: Jede com+-Anwendung kann als XML-Webdienst verfügbar gemacht werden.
ms.assetid: 03c3d5a7-eb98-4916-b6ef-ef6aac86c574
title: Erstellen von XML-Webdiensten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10652531e64fec38f2ac221184cb589a27b343d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346228"
---
# <a name="creating-xml-web-services"></a><span data-ttu-id="6b42f-103">Erstellen von XML-Webdiensten</span><span class="sxs-lookup"><span data-stu-id="6b42f-103">Creating XML Web Services</span></span>

<span data-ttu-id="6b42f-104">Jede com+-Anwendung kann als XML-Webdienst verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="6b42f-104">Any COM+ application can be exposed as an XML web service.</span></span> <span data-ttu-id="6b42f-105">Die Methoden in den Standardschnittstellen der von Anwendungen konfigurierten Komponenten (Komponenten im com+-Katalog der Server) können dann Remote aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6b42f-105">The methods in the default interfaces of the applications configured components (components in the servers COM+ catalog) can then be called remotely.</span></span> <span data-ttu-id="6b42f-106">Mit dem Verwaltungs Programmkomponenten Dienste können Sie ein virtuelles IIS-Stammverzeichnis erstellen, aus dem die Komponenten Methoden mithilfe von SOAP aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="6b42f-106">You can use the Component Services administrative tool to create an IIS virtual root directory from which the component methods can be called by using SOAP.</span></span>

> [!Note]  
> <span data-ttu-id="6b42f-107">Die .NET Framework muss auf Ihrem Computer installiert sein, um eine COM+-Anwendung als XML-Webdienst verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="6b42f-107">The .NET Framework must be installed on your computer in order to expose a COM+ application as an XML web service.</span></span>

 

<span data-ttu-id="6b42f-108">**So machen Sie eine COM+-Anwendung als XML-Webdienst verfügbar**</span><span class="sxs-lookup"><span data-stu-id="6b42f-108">**To expose a COM+ application as an XML web service**</span></span>

1.  <span data-ttu-id="6b42f-109">Öffnen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste unter **Komponenten Dienste** den Ordner **com+-Anwendungen** , der dem Computer zugeordnet ist, den Sie verwalten möchten.</span><span class="sxs-lookup"><span data-stu-id="6b42f-109">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you want to manage.</span></span>

2.  <span data-ttu-id="6b42f-110">Klicken Sie mit der rechten Maustaste auf die Anwendung, die Sie als XML-Webdienst verfügbar machen möchten, und wählen Sie **Eigenschaften** aus.</span><span class="sxs-lookup"><span data-stu-id="6b42f-110">Right-click the application you want to expose as an XML web service, and choose **Properties**.</span></span>

3.  <span data-ttu-id="6b42f-111">Klicken Sie im Dialogfeld Eigenschaften auf die Registerkarte **Aktivierung** .</span><span class="sxs-lookup"><span data-stu-id="6b42f-111">Click the **Activation** tab in the properties dialog.</span></span>

4.  <span data-ttu-id="6b42f-112">Aktivieren Sie das Kontrollkästchen **verwendet SOAP** .</span><span class="sxs-lookup"><span data-stu-id="6b42f-112">Select the **Uses SOAP** check box.</span></span>

5.  <span data-ttu-id="6b42f-113">Geben Sie im Textfeld **SOAP-vroot** den Namen des virtuellen IIS-Stamm Verzeichnisses ein, von dem aus auf die Komponenten Methoden Remote zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="6b42f-113">In the **SOAP VRoot** text box, enter the name of the IIS virtual root directory from which the components methods can be accessed remotely.</span></span> <span data-ttu-id="6b42f-114">Beachten Sie, dass ein SOAP-vroot kein Unterverzeichnis eines anderen SOAP-vroot-Verzeichnisses sein kann.</span><span class="sxs-lookup"><span data-stu-id="6b42f-114">Note that a SOAP VRoot cannot be a subdirectory of another SOAP VRoot directory.</span></span>

6.  <span data-ttu-id="6b42f-115">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="6b42f-115">Click **OK**.</span></span>

    <span data-ttu-id="6b42f-116">Wenn Sie das virtuelle IIS-Stammverzeichnis als *vroot* angeben und der voll qualifizierte Domänen Name des Servers Server *Name* ist, lautet die URL, unter der die Komponente als XML-Webdienst verfügbar gemacht wird, https://*Server* Name / *vroot*/.</span><span class="sxs-lookup"><span data-stu-id="6b42f-116">If you specify the IIS virtual root directory as *vroot* and if your servers fully qualified domain name is *servername*, the URL where your component is exposed as an XML web service is https://*servername*/*vroot*/.</span></span>

    <span data-ttu-id="6b42f-117">Das entsprechende Verzeichnis im Dateisystem ist \\ Windows \\ system32 \\ com \\ soapvroots \\ *vroot* \\ ; Com+ platziert mehrere Konfigurationsdateien und ASP.net-Programme.</span><span class="sxs-lookup"><span data-stu-id="6b42f-117">The corresponding directory in your file system is \\windows\\system32\\com\\SoapVRoots\\*vroot*\\; COM+ places several configuration files and ASP.NET programs there.</span></span> <span data-ttu-id="6b42f-118">Für einen XML-Webdienst, der stark ausgelastet ist, können Sie die in der Datei web.config gespeicherten Parameter anpassen. Weitere Informationen zu dieser Datei finden Sie in der IIS-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="6b42f-118">For an XML web service under heavy load, you may want to adjust the parameters stored in the file web.config. For information about this file, consult the IIS documentation.</span></span>

    <span data-ttu-id="6b42f-119">Die Standard Sicherheitseinstellungen für eine COM+-Anwendung, die als XML-Webdienst verfügbar gemacht wird, unterscheiden sich abhängig davon, welche Version des .NET Framework installiert ist.</span><span class="sxs-lookup"><span data-stu-id="6b42f-119">The default security settings for a COM+ application exposed as an XML web service differ depending on which version of the .NET Framework is installed.</span></span> <span data-ttu-id="6b42f-120">Wenn Version 1,0 installiert ist, sind XML-Webdienste standardmäßig nicht sicher. alle Aufrufe werden akzeptiert, und es wird keine Verschlüsselung verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b42f-120">If version 1.0 is installed, XML web services are nonsecure by default; all calls are accepted and no encryption is used.</span></span> <span data-ttu-id="6b42f-121">Wenn Version 1,1 oder höher installiert ist, sind XML-Webdienste standardmäßig sicher. Aufrufer müssen authentifiziert werden, und Verschlüsselung ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6b42f-121">If version 1.1 or later is installed, XML web services are secure by default; callers must be authenticated and encryption is required.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b42f-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6b42f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b42f-123">Zugreifen auf XML-Webdienste im Modus "Cao"</span><span class="sxs-lookup"><span data-stu-id="6b42f-123">Accessing XML Web Services in CAO Mode</span></span>](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[<span data-ttu-id="6b42f-124">Zugreifen auf XML-Webdienste im WKO-Modus</span><span class="sxs-lookup"><span data-stu-id="6b42f-124">Accessing XML Web Services in WKO Mode</span></span>](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[<span data-ttu-id="6b42f-125">Übersicht über den COM+ SOAP-Dienst</span><span class="sxs-lookup"><span data-stu-id="6b42f-125">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="6b42f-126">Sichern von XML-Webdiensten</span><span class="sxs-lookup"><span data-stu-id="6b42f-126">Securing XML Web Services</span></span>](securing-xml-web-services.md)
</dt> </dl>

 

 



