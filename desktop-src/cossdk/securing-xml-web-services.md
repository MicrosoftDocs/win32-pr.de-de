---
description: Der Zugriff auf COM+-Anwendungen, die als XML-Webdienste verfügbar gemacht werden, wird vom IIS-Webserver gesteuert, der die eingehenden Anforderungen verarbeitet.
ms.assetid: 440b0636-8afc-4fb3-a179-140958948b94
title: Sichern von XML-Webdiensten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94953ce0769c44ddaeda27cacdac99ab4ff252d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343196"
---
# <a name="securing-xml-web-services"></a><span data-ttu-id="50e36-103">Sichern von XML-Webdiensten</span><span class="sxs-lookup"><span data-stu-id="50e36-103">Securing XML Web Services</span></span>

<span data-ttu-id="50e36-104">Der Zugriff auf COM+-Anwendungen, die als XML-Webdienste verfügbar gemacht werden, wird vom IIS-Webserver gesteuert, der die eingehenden Anforderungen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="50e36-104">Access to COM+ applications exposed as XML web services is controlled by the IIS web server, which processes the incoming requests.</span></span> <span data-ttu-id="50e36-105">Sie können IIS auch so konfigurieren, dass die Kommunikation mit dem Aufrufer über einen sicheren Kanal erfolgen muss, der mit dem Secure Sockets Layer (SSL)-Protokoll festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="50e36-105">You can also configure IIS to require the communications with the caller take place over a secure channel established using the Secure Sockets Layer (SSL) protocol.</span></span>

> [!Note]  
> <span data-ttu-id="50e36-106">Ein geschützter XML-Webdienst unterstützt den WKO-Zugriff über WSDL nicht.</span><span class="sxs-lookup"><span data-stu-id="50e36-106">A secured XML web service does not support WKO access via WSDL.</span></span> <span data-ttu-id="50e36-107">Stattdessen können Clients, auf denen die .NET Framework Version 1,1 installiert ist, im Modus "Cao" aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="50e36-107">Instead, clients that have installed the .NET Framework version 1.1 can call it in CAO mode.</span></span> <span data-ttu-id="50e36-108">Wenn Clients von Drittanbietern über WSDL auf Ihren XML-Webdienst zugreifen müssen, müssen Sie den anonymen Zugriff zulassen.</span><span class="sxs-lookup"><span data-stu-id="50e36-108">If third-party clients need to access your XML web service via WSDL, you must allow anonymous access.</span></span>

 

> [!Note]  
> <span data-ttu-id="50e36-109">Wenn Sie das SSL-Protokoll verwenden möchten, um einen sicheren Kommunikationskanal einzurichten, müssen Sie ein SSL-Zertifikat abrufen und installieren.</span><span class="sxs-lookup"><span data-stu-id="50e36-109">To use the SSL protocol to establish a secure communication channel, you must obtain and install an SSL certificate.</span></span>

 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="50e36-110">Verwaltungs Tool für Komponenten Dienste</span><span class="sxs-lookup"><span data-stu-id="50e36-110">Component Services Administrative Tool</span></span>

<span data-ttu-id="50e36-111">Führen Sie die folgenden Schritte aus, um den Authentifizierungsmechanismus für einen XML-Webdienst auszuwählen:</span><span class="sxs-lookup"><span data-stu-id="50e36-111">To select the authentication mechanism for an XML web service, use the following steps:</span></span>

1.  <span data-ttu-id="50e36-112">Klicken Sie mit der rechten Maustaste auf das Symbol **Arbeitsplatz** auf Ihrem Desktop, und klicken Sie auf **Verwalten**.</span><span class="sxs-lookup"><span data-stu-id="50e36-112">Right-click the **My Computer** icon on your desktop, and click **Manage**.</span></span>

2.  <span data-ttu-id="50e36-113">Suchen Sie unter **Dienste und Anwendungen** und **Internet Informationsdienste** das Symbol, das dem virtuellen Stammverzeichnis für den XML-Webdienst entspricht.</span><span class="sxs-lookup"><span data-stu-id="50e36-113">Under **Services and Applications** and **Internet Information Service**, locate the icon corresponding to the virtual root directory for your XML web service.</span></span> <span data-ttu-id="50e36-114">Klicken Sie mit der rechten Maustaste auf das Verzeichnis Symbol, und wählen Sie **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="50e36-114">Right-click the directory icon, and choose **Properties**.</span></span>

3.  <span data-ttu-id="50e36-115">Suchen Sie auf der Registerkarte **Verzeichnis Sicherheit** des Dialog Felds Eigenschaften nach **Authentifizierung und Zugriffs Steuerung** , und klicken Sie auf die entsprechende Schaltfläche **Bearbeiten** .</span><span class="sxs-lookup"><span data-stu-id="50e36-115">On the **Directory Security** tab of the properties dialog, locate **Authentication and access control** and click the corresponding **Edit** button.</span></span>

4.  <span data-ttu-id="50e36-116">Verwenden Sie im Dialogfeld **Authentifizierungsmethoden** unter **Authentifizierter Zugriff** die Kontrollkästchen, um die Authentifizierungsmechanismen auszuwählen, die Sie zulassen möchten.</span><span class="sxs-lookup"><span data-stu-id="50e36-116">In the **Authentication Methods** dialog box, under **Authenticated access**, use the check boxes to select the authentication mechanisms you wish to allow.</span></span> <span data-ttu-id="50e36-117">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="50e36-117">Click **OK**.</span></span>

    > [!Note]  
    > <span data-ttu-id="50e36-118">Sie können IIS zum Authentifizieren von Aufrufern konfigurieren, indem Sie eine der folgenden Optionen im Dialogfeld IIS- **Authentifizierungsmethoden** verwenden: **integrierte Windows-Authentifizierung**, Digestauthentifizierung **für Windows-Domänen Server**, Standard **Authentifizierung (Kennwort wird als Klartext gesendet)** oder **.NET Passport-Authentifizierung**.</span><span class="sxs-lookup"><span data-stu-id="50e36-118">You can configure IIS to authenticate callers by using any of the following options on the IIS **Authentication Methods** dialog: **Integrated Windows authentication**, **Digest authentication for Windows domain servers**, **Basic authentication (password is sent in clear text)**, or **.NET Passport authentication**.</span></span> <span data-ttu-id="50e36-119">Sie können auch anonymen Zugriff zulassen.</span><span class="sxs-lookup"><span data-stu-id="50e36-119">You can also allow anonymous access.</span></span>

     

5.  <span data-ttu-id="50e36-120">Klicken Sie im Dialogfeld "Eigenschaften" auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="50e36-120">In the properties dialog, click **OK**.</span></span>

<span data-ttu-id="50e36-121">Um einen nicht sicheren, anonymen Zugriff auf einen XML-Webdienst zuzulassen, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="50e36-121">To allow nonsecure, anonymous access to an XML web service, use the following steps:</span></span>

1.  <span data-ttu-id="50e36-122">Klicken Sie mit der rechten Maustaste auf das Symbol **Arbeitsplatz** auf Ihrem Desktop, und klicken Sie auf **Verwalten**.</span><span class="sxs-lookup"><span data-stu-id="50e36-122">Right-click the **My Computer** icon on your desktop, and click **Manage**.</span></span>

2.  <span data-ttu-id="50e36-123">Suchen Sie unter **Dienste und Anwendungen** und **Internet Informationsdienste** das Symbol, das dem virtuellen Stammverzeichnis für den XML-Webdienst entspricht.</span><span class="sxs-lookup"><span data-stu-id="50e36-123">Under **Services and Applications** and **Internet Information Service**, locate the icon corresponding to the virtual root directory for your XML web service.</span></span> <span data-ttu-id="50e36-124">Klicken Sie mit der rechten Maustaste auf das Verzeichnis Symbol, und wählen Sie **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="50e36-124">Right-click the directory icon, and choose **Properties**.</span></span>

3.  <span data-ttu-id="50e36-125">Suchen Sie auf der Registerkarte **Verzeichnis Sicherheit** des Dialog Felds Eigenschaften nach **Authentifizierung und Zugriffs Steuerung**, und klicken Sie auf die entsprechende Schaltfläche **Bearbeiten** .</span><span class="sxs-lookup"><span data-stu-id="50e36-125">On the **Directory Security** tab of the properties dialog, locate **Authentication and access control** and click the corresponding **Edit** button.</span></span> <span data-ttu-id="50e36-126">Aktivieren Sie das Kontrollkästchen **anonymen Zugriff aktivieren** .</span><span class="sxs-lookup"><span data-stu-id="50e36-126">Select the **Enable anonymous access** check box.</span></span> <span data-ttu-id="50e36-127">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="50e36-127">Click **OK**.</span></span>

4.  <span data-ttu-id="50e36-128">Suchen Sie im Dialogfeld Eigenschaften auf der Registerkarte **Verzeichnis Sicherheit** die Schaltfläche **sichere Kommunikation** , und klicken Sie auf die entsprechende Schaltfläche **Bearbeiten** .</span><span class="sxs-lookup"><span data-stu-id="50e36-128">On the **Directory Security** tab of the properties dialog, locate **Secure communications** and click the corresponding **Edit** button.</span></span> <span data-ttu-id="50e36-129">Deaktivieren Sie das Kontrollkästchen **Secure Channel (SSL) erforderlich** .</span><span class="sxs-lookup"><span data-stu-id="50e36-129">Uncheck the **Require secure channel (SSL)** check box.</span></span> <span data-ttu-id="50e36-130">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="50e36-130">Click **OK**.</span></span>

5.  <span data-ttu-id="50e36-131">Klicken Sie im Dialogfeld "Eigenschaften" auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="50e36-131">In the properties dialog, click **OK**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="50e36-132">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="50e36-132">Visual Basic</span></span>

<span data-ttu-id="50e36-133">Nicht anwendbar.</span><span class="sxs-lookup"><span data-stu-id="50e36-133">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="50e36-134">C/C++</span><span class="sxs-lookup"><span data-stu-id="50e36-134">C/C++</span></span>

<span data-ttu-id="50e36-135">Nicht anwendbar.</span><span class="sxs-lookup"><span data-stu-id="50e36-135">Does not apply.</span></span>

## <a name="additional-security-considerations"></a><span data-ttu-id="50e36-136">Weitere Überlegungen zur Sicherheit</span><span class="sxs-lookup"><span data-stu-id="50e36-136">Additional Security Considerations</span></span>

<span data-ttu-id="50e36-137">Wenn Sie einen sicheren Kanal benötigen, können Sie die Vertraulichkeit der ausgetauschten Daten schützen, indem Sie die Kommunikation zwischen dem Client und dem XML-Webdienst verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="50e36-137">By requiring a secure channel, you help protect the confidentiality of the data exchanged by encrypting the communications between the client and your XML web service.</span></span> <span data-ttu-id="50e36-138">Wenn Sie die Authentifizierung mithilfe von Klartext-Kenn Wörtern zulassen, benötigen Sie einen sicheren Kanal, um zu verhindern, dass Kenn Wörter im Netzwerk verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="50e36-138">If you allow authentication using clear text passwords, you should require a secure channel in order to avoid exposing passwords on the network.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50e36-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="50e36-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50e36-140">Zugreifen auf XML-Webdienste im Modus "Cao"</span><span class="sxs-lookup"><span data-stu-id="50e36-140">Accessing XML Web Services in CAO Mode</span></span>](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[<span data-ttu-id="50e36-141">Zugreifen auf XML-Webdienste im WKO-Modus</span><span class="sxs-lookup"><span data-stu-id="50e36-141">Accessing XML Web Services in WKO Mode</span></span>](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[<span data-ttu-id="50e36-142">Sicherheitsüberlegungen für COM+-SOAP-Dienste</span><span class="sxs-lookup"><span data-stu-id="50e36-142">COM+ SOAP Service Security Considerations</span></span>](com--soap-service-security-considerations.md)
</dt> <dt>

[<span data-ttu-id="50e36-143">Erstellen von XML-Webdiensten</span><span class="sxs-lookup"><span data-stu-id="50e36-143">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> </dl>

 

 



