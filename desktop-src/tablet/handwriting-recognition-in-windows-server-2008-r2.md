---
description: Windows Server 2008 R2 bietet Unterstützung für die Server seitige Handschrifterkennung für Windows. In diesem Thema wird beschrieben, wie Sie die Handschrift in Windows Server 2008 R2 erkennen.
ms.assetid: ec22391d-a6e8-49b0-8650-943a661cbcd3
title: Handschrifterkennung in Windows Server 2008 R2
ms.topic: article
ms.date: 06/02/2020
ms.openlocfilehash: e014a69919c6bdc87b149f761eece14bcc3d69a4
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104039805"
---
# <a name="handwriting-recognition-in-windows-server-2008-r2"></a><span data-ttu-id="e55c2-104">Handschrifterkennung in Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e55c2-104">Handwriting Recognition in Windows Server 2008 R2</span></span>

<span data-ttu-id="e55c2-105">Windows Server 2008 R2 unterstützt die Server seitige Handschrifterkennung.</span><span class="sxs-lookup"><span data-stu-id="e55c2-105">Windows Server 2008 R2 supports server-side handwriting recognition.</span></span> <span data-ttu-id="e55c2-106">Die serverseitige Erkennung ermöglicht einem Server, Inhalte aus Stift Eingaben auf Webseiten zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="e55c2-106">Server-side recognition lets a server recognize content from pen input on Web pages.</span></span> <span data-ttu-id="e55c2-107">Dies ist besonders nützlich, wenn Benutzer in einem Netzwerk Begriffe angeben, die mit einem benutzerdefinierten Wörterbuch interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="e55c2-107">This is particularly useful when users on a network will be specifying terms that are interpreted using a custom dictionary.</span></span> <span data-ttu-id="e55c2-108">Wenn Sie z. b. eine medizinische Anwendung haben, die eine Server Datenbank für Patientennamen abgefragt hat, könnten diese Namen einer anderen Datenbank hinzugefügt werden, auf die übergreifende Verweise aus einem handschriftlichen Silverlight-Formular verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="e55c2-108">For example, if you had a medical application that queried a server database for patient names, those names could be added to another database that would be cross-referenced when performing searches from a handwritten Silverlight form.</span></span>

## <a name="set-up-your-server-for-server-side-recognition"></a><span data-ttu-id="e55c2-109">Einrichten des Servers für die Server-Side Erkennung</span><span class="sxs-lookup"><span data-stu-id="e55c2-109">Set up your Server for Server-Side Recognition</span></span>

<span data-ttu-id="e55c2-110">Die folgenden Schritte müssen befolgt werden, um die serverseitige Erkennung einzurichten.</span><span class="sxs-lookup"><span data-stu-id="e55c2-110">The following steps should be followed to set up server-side recognition.</span></span>

- <span data-ttu-id="e55c2-111">Installieren von Freihand-und Handschriftdienste</span><span class="sxs-lookup"><span data-stu-id="e55c2-111">Install Ink and Handwriting Services</span></span>
- <span data-ttu-id="e55c2-112">Installieren der Unterstützung für Webserver (IIS) und Anwendungs Server</span><span class="sxs-lookup"><span data-stu-id="e55c2-112">Install Support for Web Server (IIS) and Application Server</span></span>
- <span data-ttu-id="e55c2-113">Aktivieren der Desktop Darstellung-Rolle</span><span class="sxs-lookup"><span data-stu-id="e55c2-113">Enable the Desktop Experience Role</span></span>
- <span data-ttu-id="e55c2-114">Starten Sie den Tablet PC-Eingabe Dienst.</span><span class="sxs-lookup"><span data-stu-id="e55c2-114">Start the Tablet PC Input Service</span></span>

### <a name="install-ink-and-handwriting-services"></a><span data-ttu-id="e55c2-115">Installieren von Freihand-und Handschriftdienste</span><span class="sxs-lookup"><span data-stu-id="e55c2-115">Install Ink and Handwriting Services</span></span>

<span data-ttu-id="e55c2-116">Öffnen Sie zum Installieren der Freihand-und Handschrift Dienste den Server-Manager, indem Sie in der Schnellstartleiste auf das Symbol Server-Manager klicken.</span><span class="sxs-lookup"><span data-stu-id="e55c2-116">To install Ink and Handwriting services, open the server manager by clicking the server manager icon from the Quick Launch tray.</span></span> <span data-ttu-id="e55c2-117">Klicken Sie im Menü **Features** auf **Features hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="e55c2-117">From the **Features** menu, click **Add Features**.</span></span> <span data-ttu-id="e55c2-118">Stellen Sie sicher, dass Sie das Kontrollkästchen **Freihand-und Handschriftdienste** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e55c2-118">Make sure that you select the **Ink and Handwriting Services** check box.</span></span> <span data-ttu-id="e55c2-119">In der folgenden Abbildung wird das Dialogfeld **Features auswählen** angezeigt, in dem **Freihand-und Handschriftdienste** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="e55c2-119">The following image shows the **Select Features** dialog box with **Ink and Handwriting Services** selected.</span></span>

<span data-ttu-id="e55c2-120">![Dialogfeld "Features auswählen" mit aktivierten Kontrollkästchen für frei Hand Eingabe und Handschrift](images/setup-server-1-ink-and-handwriting.png)</span><span class="sxs-lookup"><span data-stu-id="e55c2-120">![Select features dialog box with ink and handwriting services check box selected](images/setup-server-1-ink-and-handwriting.png)</span></span><br/>
<span data-ttu-id="e55c2-121">*Dialogfeld "Features auswählen" mit aktivierten Kontrollkästchen für frei Hand Eingabe und Handschrift*</span><span class="sxs-lookup"><span data-stu-id="e55c2-121">*Select features dialog box with ink and handwriting services check box selected*</span></span>

### <a name="installation-support-for-web-server-iis-and-application-server"></a><span data-ttu-id="e55c2-122">Installationsunterstützung für Webserver (IIS) und Anwendungs Server</span><span class="sxs-lookup"><span data-stu-id="e55c2-122">Installation Support for Web Server (IIS) and Application Server</span></span>

<span data-ttu-id="e55c2-123">Öffnen Sie den Server-Manager wie im ersten Schritt.</span><span class="sxs-lookup"><span data-stu-id="e55c2-123">Open the server manager as you did for the first step.</span></span> <span data-ttu-id="e55c2-124">Als nächstes müssen Sie die Rollen "Webserver (IIS)" und "Anwendungs Server" hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e55c2-124">Next, you will need to add the Web Server (IIS) and Application Server roles.</span></span> <span data-ttu-id="e55c2-125">Klicken Sie im Menü **Rollen** auf **Rollen hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="e55c2-125">From the **Roles** menu, click **Add Roles**.</span></span> <span data-ttu-id="e55c2-126">Der Assistent zum Hinzufügen von Rollen wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e55c2-126">The Add Roles wizard appears.</span></span> <span data-ttu-id="e55c2-127">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="e55c2-127">Click **Next**.</span></span> <span data-ttu-id="e55c2-128">Stellen Sie sicher, dass **Anwendungs Server** und **Webserver (IIS)** ausgewählt sind.</span><span class="sxs-lookup"><span data-stu-id="e55c2-128">Make sure **Application Server** and **Web Server (IIS)** are selected.</span></span> <span data-ttu-id="e55c2-129">In der folgenden Abbildung wird das Dialogfeld **Server Rollen auswählen** angezeigt, in dem die Rollen **Webserver (IIS)** und **Anwendungs Server** ausgewählt sind.</span><span class="sxs-lookup"><span data-stu-id="e55c2-129">The following image shows the **Select Server Roles** dialog box with the **Web Server (IIS)** and **Application Server** roles selected.</span></span>

<span data-ttu-id="e55c2-130">![Dialogfeld "Server Rollen auswählen", bei dem Webserver (IIS) und Anwendungsserver Rollen ausgewählt sind](images/setup-server-2-select-server-roles.png)</span><span class="sxs-lookup"><span data-stu-id="e55c2-130">![Select server roles dialog box with web server (iis) and application server roles selected](images/setup-server-2-select-server-roles.png)</span></span><br/>
<span data-ttu-id="e55c2-131">*Dialogfeld "Server Rollen auswählen", bei dem Webserver (IIS) und Anwendungsserver Rollen ausgewählt sind*</span><span class="sxs-lookup"><span data-stu-id="e55c2-131">*Select server roles dialog box with web server (iis) and application server roles selected*</span></span>

<span data-ttu-id="e55c2-132">Wenn Sie den **Anwendungs Server** auswählen, werden Sie aufgefordert, das ASP.NET Framework zu installieren.</span><span class="sxs-lookup"><span data-stu-id="e55c2-132">When you select **Application Server**, you will be asked to install the ASP.NET framework.</span></span> <span data-ttu-id="e55c2-133">Klicken Sie auf die Schaltfläche **erforderliche Features hinzufügen** .</span><span class="sxs-lookup"><span data-stu-id="e55c2-133">Click the **Add the Required Features** button.</span></span> <span data-ttu-id="e55c2-134">Nachdem Sie auf " **weiter**" klicken, wird ein Übersichts Dialogfeld angezeigt. Klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="e55c2-134">After you click **Next**, you will be presented with an overview dialog box; click **Next**.</span></span> <span data-ttu-id="e55c2-135">Das Dialogfeld **Rollen Dienste auswählen** sollte jetzt verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="e55c2-135">The **Select Role Services** dialog box should now be available.</span></span> <span data-ttu-id="e55c2-136">Stellen Sie sicher, dass **Webserver (IIS)** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="e55c2-136">Make sure that **Web Server (IIS)** is selected.</span></span> <span data-ttu-id="e55c2-137">In der folgenden Abbildung wird das Dialogfeld **Rollen Dienste auswählen** mit aktiviertem Webserver (IIS) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e55c2-137">The following image shows the **Select Role Services** dialog box with Web Server (IIS) enabled.</span></span>

<span data-ttu-id="e55c2-138">![Dialogfeld "Rollen Dienste auswählen" mit aktiviertem Webserver (IIS)](images/setup-server-3-select-role-services.png)</span><span class="sxs-lookup"><span data-stu-id="e55c2-138">![Select role services dialog box with web server (iis) enabled](images/setup-server-3-select-role-services.png)</span></span><br/>
<span data-ttu-id="e55c2-139">*Dialogfeld "Rollen Dienste auswählen" mit aktiviertem Webserver (IIS)*</span><span class="sxs-lookup"><span data-stu-id="e55c2-139">*Select role services dialog box with web server (iis) enabled*</span></span>

<span data-ttu-id="e55c2-140">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="e55c2-140">Click **Next**.</span></span> <span data-ttu-id="e55c2-141">Ein Übersichts Dialogfeld wird angezeigt. Klicken Sie erneut auf **weiter** .</span><span class="sxs-lookup"><span data-stu-id="e55c2-141">An overview dialog box appears; click **Next** again.</span></span> <span data-ttu-id="e55c2-142">Ihnen wird nun eine Seite angezeigt, auf der Sie Optionen für Rollen für Webserver (IIS) bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e55c2-142">You will now be presented with a page offering you options for roles for Web Server (IIS).</span></span> <span data-ttu-id="e55c2-143">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="e55c2-143">Click **Next**.</span></span> <span data-ttu-id="e55c2-144">Auf der nächsten Seite wird die Schaltfläche " **Installieren** " aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e55c2-144">On the next page, the **Install** button will become active.</span></span> <span data-ttu-id="e55c2-145">Klicken Sie auf **Installieren** , und installieren Sie die Unterstützung für Webserver (IIS) und Anwendungs Server.</span><span class="sxs-lookup"><span data-stu-id="e55c2-145">Click **Install** and you will install support for Web Server (IIS) and Application Server.</span></span>

### <a name="enable-the-desktop-experience-role"></a><span data-ttu-id="e55c2-146">Aktivieren der Desktop Darstellung-Rolle</span><span class="sxs-lookup"><span data-stu-id="e55c2-146">Enable the Desktop Experience Role</span></span>

<span data-ttu-id="e55c2-147">Um die Desktop Darstellung zu aktivieren, klicken Sie auf **Start**, klicken Sie auf **Verwaltung**, und klicken Sie dann auf **Server-Manager**.</span><span class="sxs-lookup"><span data-stu-id="e55c2-147">To enable the desktop experience, click **Start**, click **Administrative Tools**, and then click **Server Manager**.</span></span> <span data-ttu-id="e55c2-148">Wählen Sie **Dienste hinzufügen** und dann den **Desktop Darstellung-** Dienst aus.</span><span class="sxs-lookup"><span data-stu-id="e55c2-148">Select **Add Services** and then select the **Desktop Experience** service.</span></span> <span data-ttu-id="e55c2-149">In der folgenden Abbildung wird das Dialogfeld **Features auswählen** angezeigt, in dem das Element Desktop Darstellung installiert ist.</span><span class="sxs-lookup"><span data-stu-id="e55c2-149">The following image shows the **Select Features** dialog box with the Desktop Experience item installed.</span></span>

<span data-ttu-id="e55c2-150">![Dialogfeld "Features auswählen" mit ausgewähltem Desktop Darstellung-Dienst](images/setup-server-4-desktop-experience.png)</span><span class="sxs-lookup"><span data-stu-id="e55c2-150">![Select features dialog box with desktop experience service selected](images/setup-server-4-desktop-experience.png)</span></span><br/>
<span data-ttu-id="e55c2-151">*Dialogfeld "Features auswählen" mit ausgewähltem Desktop Darstellung-Dienst*</span><span class="sxs-lookup"><span data-stu-id="e55c2-151">*Select features dialog box with desktop experience service selected*</span></span>

<span data-ttu-id="e55c2-152">Klicken Sie auf **weiter** , um die Desktop Darstellung zu installieren.</span><span class="sxs-lookup"><span data-stu-id="e55c2-152">Click **Next** to install the Desktop Experience.</span></span>

### <a name="start-the-tablet-service"></a><span data-ttu-id="e55c2-153">Starten des Tablet-Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="e55c2-153">Start the Tablet Service</span></span>

<span data-ttu-id="e55c2-154">Nachdem Sie den Desktop Erfahrungs Dienst installiert haben, wird der Tablet PC-Eingabe Dienst im Menü **Dienste** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e55c2-154">After you have installed the Desktop Experience service, the Tablet PC Input service will appear in the **Services** menu.</span></span> <span data-ttu-id="e55c2-155">Um auf das Menü **Dienste** zuzugreifen, klicken Sie auf **Start**, klicken Sie auf **Verwaltung**, und klicken Sie dann auf **Dienste**.</span><span class="sxs-lookup"><span data-stu-id="e55c2-155">To access the **Services** menu, click **Start**, click **Administrative Tools**, and then click **Services**.</span></span> <span data-ttu-id="e55c2-156">Klicken Sie mit der rechten Maustaste auf **Tablet PC Input Service** , und klicken Sie dann auf **starten**.</span><span class="sxs-lookup"><span data-stu-id="e55c2-156">To start the service, right-click **Tablet PC Input Service** and then click **Start**.</span></span> <span data-ttu-id="e55c2-157">Die folgende Abbildung zeigt das Menü **Dienste** , in dem der Tablet PC-Eingabe Dienst gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="e55c2-157">The following image shows the **Services** menu with the Tablet PC Input Service started.</span></span>

<span data-ttu-id="e55c2-158">![Menü "Dienste" mit Start des Tablet PC-Eingabe Diensts](images/setup-server-5-tablet-pc-input-service.png)</span><span class="sxs-lookup"><span data-stu-id="e55c2-158">![Services menu with the tablet pc input service started](images/setup-server-5-tablet-pc-input-service.png)</span></span><br/>
<span data-ttu-id="e55c2-159">*Menü "Dienste" mit Start des Tablet PC-Eingabe Diensts*</span><span class="sxs-lookup"><span data-stu-id="e55c2-159">*Services menu with the tablet pc input service started*</span></span>

## <a name="performing-server-side-recognition-using-silverlight"></a><span data-ttu-id="e55c2-160">Durchführen Server-Side Erkennung mithilfe von Silverlight</span><span class="sxs-lookup"><span data-stu-id="e55c2-160">Performing Server-Side Recognition Using Silverlight</span></span>

<span data-ttu-id="e55c2-161">In diesem Abschnitt wird gezeigt, wie eine Webanwendung erstellt wird, die Silverlight zum Erfassen von Handschrift Eingaben verwendet.</span><span class="sxs-lookup"><span data-stu-id="e55c2-161">This section shows how to create a Web application that uses Silverlight to capture handwriting input.</span></span> <span data-ttu-id="e55c2-162">Führen Sie die folgenden Schritte aus, um die Erkennung in Visual Studio 2008 zu programmieren.</span><span class="sxs-lookup"><span data-stu-id="e55c2-162">Use the following steps to program the recognizer in Visual Studio 2008.</span></span>

- <span data-ttu-id="e55c2-163">Installieren und aktualisieren Sie Visual Studio 2008, um die Unterstützung für Silverlight hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e55c2-163">Install and update Visual Studio 2008 to add support for Silverlight.</span></span>
- <span data-ttu-id="e55c2-164">Erstellen Sie ein neues Silverlight-Projekt in Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="e55c2-164">Create a new Silverlight project in Visual Studio 2008.</span></span>
- <span data-ttu-id="e55c2-165">Fügen Sie dem Projekt die erforderlichen Dienst Verweise hinzu.</span><span class="sxs-lookup"><span data-stu-id="e55c2-165">Add the necessary service references to your project.</span></span>
- <span data-ttu-id="e55c2-166">Erstellen Sie einen Silverlight-WCF-Dienst für die frei Handerkennung.</span><span class="sxs-lookup"><span data-stu-id="e55c2-166">Create a Silverlight WCF Service for ink recognition.</span></span>
- <span data-ttu-id="e55c2-167">Fügen Sie dem Client Projekt den Dienst Verweis hinzu.</span><span class="sxs-lookup"><span data-stu-id="e55c2-167">Add the service reference to your client project.</span></span>
- <span data-ttu-id="e55c2-168">Fügen Sie die InkCollector-Klasse dem InkRecognition-Projekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="e55c2-168">Add the InkCollector class to the InkRecognition project.</span></span>
- <span data-ttu-id="e55c2-169">Entfernen von sicheren Transport Direktiven aus der Client Konfiguration</span><span class="sxs-lookup"><span data-stu-id="e55c2-169">Remove secure transport directives from the client configuration</span></span>

### <a name="install-and-update-visual-studio-2008-to-add-support-for-silverlight"></a><span data-ttu-id="e55c2-170">Installieren und Aktualisieren von Visual Studio 2008 zum Hinzufügen von Unterstützung für Silverlight</span><span class="sxs-lookup"><span data-stu-id="e55c2-170">Install and Update Visual Studio 2008 to Add Support for Silverlight</span></span>

<span data-ttu-id="e55c2-171">Bevor Sie beginnen, müssen Sie die folgenden Schritte auf Ihrem Windows Server 2008 R2-Server ausführen.</span><span class="sxs-lookup"><span data-stu-id="e55c2-171">Before you begin, you must perform the following steps on your Windows Server 2008 R2 server.</span></span>

- <span data-ttu-id="e55c2-172">Installieren Sie Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="e55c2-172">Install Visual Studio 2008.</span></span>
- <span data-ttu-id="e55c2-173">Installieren Sie [Microsoft Visual Studio 2008 Service Pack 1](https://www.microsoft.com/download/details.aspx?id=10986).</span><span class="sxs-lookup"><span data-stu-id="e55c2-173">Install [Microsoft Visual Studio 2008 Service Pack 1](https://www.microsoft.com/download/details.aspx?id=10986).</span></span>
- <span data-ttu-id="e55c2-174">Installieren Sie das [Microsoft Silverlight 5 SDK](https://www.microsoft.com/silverlight/).</span><span class="sxs-lookup"><span data-stu-id="e55c2-174">Install [Microsoft Silverlight 5 SDK](https://www.microsoft.com/silverlight/).</span></span>

<span data-ttu-id="e55c2-175">Nachdem Sie diese Anwendungen und Updates installiert haben, können Sie die serverseitige Erkennungs-Webanwendung erstellen.</span><span class="sxs-lookup"><span data-stu-id="e55c2-175">After you have installed these applications and updates, you are ready to create your server-side recognition Web application.</span></span>

### <a name="create-a-new-silverlight-web-project-in-visual-studio-2008"></a><span data-ttu-id="e55c2-176">Erstellen eines neuen Silverlight-Webprojekts in Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="e55c2-176">Create a new Silverlight Web Project in Visual Studio 2008</span></span>

<span data-ttu-id="e55c2-177">Klicken Sie im Menü **Datei** auf **Neues Projekt**.</span><span class="sxs-lookup"><span data-stu-id="e55c2-177">From the **File** menu, click **New Project**.</span></span> <span data-ttu-id="e55c2-178">Wählen Sie die Vorlage Silverlight-Anwendung aus der Liste Visual C- \# Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="e55c2-178">Select the Silverlight Application template from the Visual C\# project list.</span></span> <span data-ttu-id="e55c2-179">Nennen Sie Ihr Projekt InkRecognition, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="e55c2-179">Name your project InkRecognition and click **OK**.</span></span> <span data-ttu-id="e55c2-180">Die folgende Abbildung zeigt das \# ausgewählte C Silverlight-Projekt mit dem Namen InkRecognition.</span><span class="sxs-lookup"><span data-stu-id="e55c2-180">The following image shows the C\# Silverlight project selected and named InkRecognition.</span></span>

<span data-ttu-id="e55c2-181">![c \# Silverlight-Projekt mit dem Namen "InkRecognition" ausgewählt](images/project-1-new-project.png)</span><span class="sxs-lookup"><span data-stu-id="e55c2-181">![c\# silverlight project selected, with the name inkrecognition](images/project-1-new-project.png)</span></span><br/>
<span data-ttu-id="e55c2-182">*c \# Silverlight-Projekt mit dem Namen "InkRecognition" ausgewählt*</span><span class="sxs-lookup"><span data-stu-id="e55c2-182">*c\# silverlight project selected, with the name inkrecognition*</span></span>

<span data-ttu-id="e55c2-183">Nachdem Sie auf **OK** geklickt haben, werden Sie in einem Dialogfeld aufgefordert, dem Projekt eine Silverlight-Anwendung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e55c2-183">After you click **OK**, a dialog box prompts you to add a Silverlight application to your project.</span></span> <span data-ttu-id="e55c2-184">Wählen Sie **ein neues ASP.NET-Webprojekt zur Projekt Mappe hinzufügen aus, um Silverlight zu hosten,** **und klicken Sie**</span><span class="sxs-lookup"><span data-stu-id="e55c2-184">Select **Add a new ASP.NET Web project to the solution to host Silverlight** and click **OK**.</span></span> <span data-ttu-id="e55c2-185">In der folgenden Abbildung wird gezeigt, wie Sie das Beispiel Projekt einrichten, bevor Sie auf **OK** klicken.</span><span class="sxs-lookup"><span data-stu-id="e55c2-185">The following image shows how to set up the example project before you click **OK**.</span></span>

<span data-ttu-id="e55c2-186">![Dialog Feld mit der Aufforderung zum Hinzufügen einer Silverlight-Anwendung zu einem Projekt](images/project-2-add-a-new-aspnetproject.png)</span><span class="sxs-lookup"><span data-stu-id="e55c2-186">![Dialog box with prompt for adding a silverlight application to a project](images/project-2-add-a-new-aspnetproject.png)</span></span><br/>
<span data-ttu-id="e55c2-187">*Dialog Feld mit der Aufforderung zum Hinzufügen einer Silverlight-Anwendung zu einem Projekt*</span><span class="sxs-lookup"><span data-stu-id="e55c2-187">*Dialog box with prompt for adding a silverlight application to a project*</span></span>

### <a name="add-the-necessary-service-references-to-your-project"></a><span data-ttu-id="e55c2-188">Fügen Sie dem Projekt die erforderlichen Dienst Verweise hinzu.</span><span class="sxs-lookup"><span data-stu-id="e55c2-188">Add the Necessary Service References to your Project</span></span>

<span data-ttu-id="e55c2-189">Nun verfügen Sie über das generische Silverlight-Client Projekt (InkRecognition) mit einem Webprojekt (InkRecognition. Web), das in Ihrer Lösung eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="e55c2-189">Now you have your generic Silverlight client project (InkRecognition) with a Web project (InkRecognition.Web) set up in your solution.</span></span> <span data-ttu-id="e55c2-190">Das Projekt wird mit "page. XAML" und "default. aspx" geöffnet.</span><span class="sxs-lookup"><span data-stu-id="e55c2-190">The project will open with Page.xaml and Default.aspx open.</span></span> <span data-ttu-id="e55c2-191">Schließen Sie diese Fenster, und fügen Sie die Verweise "System. Runtime. Serialization" und "System. Service Model" dem Projekt "inkrekognition" hinzu, **indem Sie mit** der rechten Maustaste auf den Ordner "Verweise" im Projekt "inkrekognition" klicken</span><span class="sxs-lookup"><span data-stu-id="e55c2-191">Close these windows and add the System.Runtime.Serialization and System.ServiceModel references to the InkRecognition project by right-clicking on the references folder in the InkRecognition project and selecting **Add Reference**.</span></span> <span data-ttu-id="e55c2-192">In der folgenden Abbildung wird das Dialogfeld angezeigt, in dem die erforderlichen Verweise ausgewählt sind.</span><span class="sxs-lookup"><span data-stu-id="e55c2-192">The following image shows the dialog box with the requisite references selected.</span></span>

<span data-ttu-id="e55c2-193">![Verweise hinzufügen (Dialogfeld) mit System. Runtime. Serialization und System. Service Model ausgewählt](images/project-3a-add-references-to-inkreco.png)</span><span class="sxs-lookup"><span data-stu-id="e55c2-193">![Add references dialog box with system.runtime.serialization and system.servicemodel selected](images/project-3a-add-references-to-inkreco.png)</span></span><br/>
<span data-ttu-id="e55c2-194">*Verweise hinzufügen (Dialogfeld) mit System. Runtime. Serialization und System. Service Model ausgewählt*</span><span class="sxs-lookup"><span data-stu-id="e55c2-194">*Add references dialog box with system.runtime.serialization and system.servicemodel selected*</span></span>

<span data-ttu-id="e55c2-195">Als nächstes müssen Sie dem Projekt "InkRecognition. Web" die Verweise "System. Service Model" und "Microsoft. Ink" hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e55c2-195">Next, you need to add the System.ServiceModel and Microsoft.Ink references to the InkRecognition.Web project.</span></span> <span data-ttu-id="e55c2-196">Die Microsoft. Ink-Referenz wird nicht standardmäßig in den .net-verweisen angezeigt. Suchen Sie daher im Windows-Ordner nach Microsoft.Ink.dll.</span><span class="sxs-lookup"><span data-stu-id="e55c2-196">The Microsoft.Ink reference will not appear in the .NET references by default, so search your Windows folder for Microsoft.Ink.dll.</span></span> <span data-ttu-id="e55c2-197">Nachdem Sie die dll gefunden haben, fügen Sie die Assembly zu den Projekt verweisen hinzu: Wählen Sie die Registerkarte **Durchsuchen** aus, wechseln Sie in den Ordner mit Microsoft.Ink.dll, wählen Sie Microsoft.Ink.dll aus, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="e55c2-197">After you have located the DLL, add the assembly to the project references: select the **Browse** tab, change to the folder containing Microsoft.Ink.dll, select Microsoft.Ink.dll, and then click **OK**.</span></span> <span data-ttu-id="e55c2-198">Die folgende Abbildung zeigt die Projekt Mappe im Windows-Explorer mit allen hinzugefügten Verweisassemblys.</span><span class="sxs-lookup"><span data-stu-id="e55c2-198">The following image shows the project's solution in Windows Explorer with all of the reference assemblies added.</span></span>

<span data-ttu-id="e55c2-199">![InkRecognition-Projekt in Windows-Explorer mit hinzugefügten Verweisassemblys](images/project-3b-with-reference-assemblies.png)</span><span class="sxs-lookup"><span data-stu-id="e55c2-199">![inkrecognition project in windows explorer with all reference assemblies added](images/project-3b-with-reference-assemblies.png)</span></span><br/>
<span data-ttu-id="e55c2-200">*InkRecognition-Projekt in Windows-Explorer mit hinzugefügten Verweisassemblys*</span><span class="sxs-lookup"><span data-stu-id="e55c2-200">*inkrecognition project in windows explorer with all reference assemblies added*</span></span>

### <a name="create-a-silverlight-wcf-service-for-ink-recognition"></a><span data-ttu-id="e55c2-201">Erstellen eines Silverlight WCF-Dienstanbieter für die frei Handerkennung</span><span class="sxs-lookup"><span data-stu-id="e55c2-201">Create a Silverlight WCF Service for Ink Recognition</span></span>

<span data-ttu-id="e55c2-202">Als Nächstes fügen Sie einen WCF-Dienst für die frei Handerkennung zum Projekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="e55c2-202">Next, you will add a WCF service for ink recognition to the project.</span></span> <span data-ttu-id="e55c2-203">Klicken Sie mit der rechten Maustaste auf das Projekt InkRecognition. Web, klicken Sie auf **Hinzufügen** und dann auf **Neues Element**.</span><span class="sxs-lookup"><span data-stu-id="e55c2-203">Right-click your InkRecognition.Web project, click **Add**, and then click **New Item**.</span></span> <span data-ttu-id="e55c2-204">Wählen Sie die WCF Silverlight-Dienst Vorlage aus, ändern Sie den Namen in inkrecogitionservice, und klicken Sie dann auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="e55c2-204">Select the WCF Silverlight Service template, change the name to InkRecogitionService, and then click **Add**.</span></span> <span data-ttu-id="e55c2-205">Die folgende Abbildung zeigt das Dialogfeld **Neues Element hinzufügen** , bei dem der Silverlight-WCF-Dienst ausgewählt und benannt ist.</span><span class="sxs-lookup"><span data-stu-id="e55c2-205">The following image shows the **Add New Item** dialog box with the Silverlight WCF service selected and named.</span></span>

<span data-ttu-id="e55c2-206">![Dialogfeld "Neues Element hinzufügen" mit ausgewähltem Silverlight-WCF-Dienst](images/project-4-add-wcf-service.png)</span><span class="sxs-lookup"><span data-stu-id="e55c2-206">![Add new item dialog box with silverlight wcf service selected and named](images/project-4-add-wcf-service.png)</span></span><br/>
<span data-ttu-id="e55c2-207&quot;>*Dialogfeld &quot;Neues Element hinzufügen&quot; mit ausgewähltem Silverlight-WCF-Dienst*</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;e55c2-207&quot;>*Add new item dialog box with silverlight wcf service selected and named*</span></span>

<span data-ttu-id=&quot;e55c2-208&quot;>Nachdem Sie den WCF Silverlight-Dienst hinzugefügt haben, wird der Dienst Code &quot;inkrecognitionservice. cs&quot; geöffnet.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;e55c2-208&quot;>After you add the WCF Silverlight service, the service code behind, InkRecognitionService.cs, will open.</span></span> <span data-ttu-id=&quot;e55c2-209&quot;>Ersetzen Sie den Dienst Code durch den folgenden Code.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;e55c2-209&quot;>Replace the service code with the following code.</span></span>

```CSharp
using System;
using System.Linq;
using System.Runtime.Serialization;
using System.ServiceModel;
using System.ServiceModel.Activation;
using System.Collections.Generic;
using System.Text;
using Microsoft.Ink;

namespace InkRecognition.Web
{
    [ServiceContract(Namespace = &quot;")]
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class InkRecognitionService
    {
        [OperationContract]
        public string[] Recognize(int[][] packets)
        {
            // Deserialize ink.
            Ink ink = new Ink();
            Tablet tablet = new Tablets().DefaultTablet;
            TabletPropertyDescriptionCollection desc = new TabletPropertyDescriptionCollection();
            desc.Add(new TabletPropertyDescription(PacketProperty.X, tablet.GetPropertyMetrics(PacketProperty.X)));
            desc.Add(new TabletPropertyDescription(PacketProperty.Y, tablet.GetPropertyMetrics(PacketProperty.Y)));
            int numOfStrokes = packets.GetUpperBound(0) + 1;
            for (int i = 0; i < numOfStrokes; i++)
            {
                ink.CreateStroke(packets[i], desc);
            }

            // Recognize ink.
            RecognitionStatus recoStatus;
            RecognizerContext recoContext = new RecognizerContext();
            recoContext.RecognitionFlags = RecognitionModes.LineMode | RecognitionModes.TopInkBreaksOnly;
            recoContext.Strokes = ink.Strokes;
            RecognitionResult recoResult = recoContext.Recognize(out recoStatus);
            RecognitionAlternates alternates = recoResult.GetAlternatesFromSelection();
            string[] results = new string[alternates.Count];
            for (int i = 0; i < alternates.Count; i++)
            {
                results[i] = alternates[i].ToString();
            }

            // Send results to client.
            return results;
        }
    }
}
```

### <a name="add-the-service-reference-to-your-client-project"></a><span data-ttu-id="e55c2-210">Hinzufügen des Dienst Verweises zu Ihrem Client Projekt</span><span class="sxs-lookup"><span data-stu-id="e55c2-210">Add the Service Reference to your Client Project</span></span>

<span data-ttu-id="e55c2-211">Nachdem Sie den Silverlight-WCF-Dienst für InkRecognition erstellt haben, nutzen Sie den Dienst von Ihrer Client Anwendung.</span><span class="sxs-lookup"><span data-stu-id="e55c2-211">Now that you have your Silverlight WCF service for InkRecognition, you will consume the service from your client application.</span></span> <span data-ttu-id="e55c2-212">Klicken Sie mit der rechten Maustaste auf das Projekt InkRecognition, und wählen Sie **Dienstverweis hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="e55c2-212">Right-click the InkRecognition project and select **Add Service Reference**.</span></span> <span data-ttu-id="e55c2-213">Wählen Sie im angezeigten Dialogfeld **Dienstverweis hinzufügen** die Option **ermitteln** aus, um die Dienste aus der aktuellen Projekt Mappe zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="e55c2-213">From the **Add Service Reference** dialog box that appears, select **Discover** to discover services from the current solution.</span></span> <span data-ttu-id="e55c2-214">Inkrecognitionservice wird im Bereich Dienste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e55c2-214">InkRecognitionService will appear in the Services pane.</span></span> <span data-ttu-id="e55c2-215">Doppelklicken Sie im Bereich Dienste auf inkrecognitionservice, ändern Sie den Namespace in inkrecognitionservicereferen, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="e55c2-215">Double-click InkRecognitionService from the Services pane, change the namespace to InkRecognitionServiceReference, and then click **OK**.</span></span> <span data-ttu-id="e55c2-216">In der folgenden Abbildung wird das Dialogfeld **Dienstverweis hinzufügen** angezeigt, in dem inkrecognitionservice ausgewählt und der Namespace geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="e55c2-216">The following image shows the **Add Service Reference** dialog box with InkRecognitionService selected and the namespace changed.</span></span>

<span data-ttu-id="e55c2-217">![Dialogfeld "Dienst Verweis hinzufügen", bei dem inkrecognitionservice ausgewählt und der Namespace geändert wurde](images/project-5-discover-service-reference.png)</span><span class="sxs-lookup"><span data-stu-id="e55c2-217">![Add service reference dialog box with inkrecognitionservice selected and namespace changed](images/project-5-discover-service-reference.png)</span></span><br/>
<span data-ttu-id="e55c2-218">*Dialogfeld "Dienst Verweis hinzufügen", bei dem inkrecognitionservice ausgewählt und der Namespace geändert wurde*</span><span class="sxs-lookup"><span data-stu-id="e55c2-218">*Add service reference dialog box with inkrecognitionservice selected and namespace changed*</span></span>

### <a name="add-the-inkcollector-class-to-the-inkrecognition-project"></a><span data-ttu-id="e55c2-219">Hinzufügen der InkCollector-Klasse zum InkRecognition-Projekt</span><span class="sxs-lookup"><span data-stu-id="e55c2-219">Add the InkCollector Class to the InkRecognition Project</span></span>

<span data-ttu-id="e55c2-220">Klicken Sie mit der rechten Maustaste auf das Projekt InkRecognition, klicken Sie auf **Hinzufügen** und dann auf **Neues Element**.</span><span class="sxs-lookup"><span data-stu-id="e55c2-220">Right-click the InkRecognition project, click **Add**, and then click **New Item**.</span></span> <span data-ttu-id="e55c2-221">Wählen Sie im **Visual \# C** -Menü die Option **C- \# Klasse** aus.</span><span class="sxs-lookup"><span data-stu-id="e55c2-221">From the **Visual C\#** menu, select **C\# class**.</span></span> <span data-ttu-id="e55c2-222">Benennen Sie die Klasse "InkCollector".</span><span class="sxs-lookup"><span data-stu-id="e55c2-222">Name the class InkCollector.</span></span> <span data-ttu-id="e55c2-223">In der folgenden Abbildung wird das Dialogfeld angezeigt, in dem die C \# -Klasse ausgewählt und benannt ist.</span><span class="sxs-lookup"><span data-stu-id="e55c2-223">The following image shows the dialog box with the C\# class selected and named.</span></span>

<span data-ttu-id="e55c2-224">![Dialogfeld "Neues Element hinzufügen" mit \# ausgewählter c-Klasse und Namen](images/project-6-add-ink-collector.png)</span><span class="sxs-lookup"><span data-stu-id="e55c2-224">![Add new item dialog box with c\# class selected and named](images/project-6-add-ink-collector.png)</span></span><br/>
<span data-ttu-id="e55c2-225">*Dialogfeld "Neues Element hinzufügen" mit \# ausgewählter c-Klasse und Namen*</span><span class="sxs-lookup"><span data-stu-id="e55c2-225">*Add new item dialog box with c\# class selected and named*</span></span>

<span data-ttu-id="e55c2-226">Nachdem Sie die InkCollector-Klasse hinzugefügt haben, wird die Klassendefinition geöffnet.</span><span class="sxs-lookup"><span data-stu-id="e55c2-226">After you add the InkCollector class, the class definition will open.</span></span> <span data-ttu-id="e55c2-227">Ersetzen Sie den Code im Ink Collector durch den folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="e55c2-227">Replace the code in the Ink Collector with the following code.</span></span>

```CSharp
using System;
using System.Net;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Documents;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Animation;
using System.Windows.Shapes;

namespace InkRecognition
{
    public class InkCollector : IDisposable
    {
        public InkCollector(InkPresenter presenter)
        {
            _presenter = presenter;
            _presenter.Cursor = Cursors.Stylus;
            _presenter.MouseLeftButtonDown += new MouseButtonEventHandler(_presenter_MouseLeftButtonDown);
            _presenter.MouseMove += new MouseEventHandler(_presenter_MouseMove);
            _presenter.MouseLeftButtonUp += new MouseButtonEventHandler(_presenter_MouseLeftButtonUp);
        }

        void _presenter_MouseLeftButtonDown(object sender, MouseButtonEventArgs e)
        {
            _presenter.CaptureMouse();
            if (!e.StylusDevice.Inverted)
            {
                _presenter.Cursor = Cursors.Stylus;
                _stroke = new Stroke(e.StylusDevice.GetStylusPoints(_presenter));
                _stroke.DrawingAttributes = _drawingAttributes;
                _presenter.Strokes.Add(_stroke);
            }
            else
            {
                _presenter.Cursor = Cursors.Eraser;
                _erasePoints = e.StylusDevice.GetStylusPoints(_presenter);
            }
        }

        void _presenter_MouseMove(object sender, MouseEventArgs e)
        {
            if (!e.StylusDevice.Inverted)
            {
                _presenter.Cursor = Cursors.Stylus;
            }
            else
            {
                _presenter.Cursor = Cursors.Eraser;
            }
            if (_stroke != null)
            {
                _stroke.StylusPoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
            }
            else if (_erasePoints != null)
            {
                _erasePoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
                StrokeCollection hitStrokes = _presenter.Strokes.HitTest(_erasePoints);
                if (hitStrokes.Count > 0)
                {
                    foreach (Stroke hitStroke in hitStrokes)
                    {
                        _presenter.Strokes.Remove(hitStroke);
                    }
                }
            }
        }

        void _presenter_MouseLeftButtonUp(object sender, MouseButtonEventArgs e)
        {
            _presenter.ReleaseMouseCapture();
            if (_stroke != null)
            {
                _stroke.StylusPoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
            }
            _stroke = null;
            _erasePoints = null;
        }

        public DrawingAttributes DefaultDrawingAttributes
        {
            get { return _drawingAttributes; }
            set { _drawingAttributes = value; }
        }

        public void Dispose()
        {
            _presenter.MouseLeftButtonDown -= new MouseButtonEventHandler(_presenter_MouseLeftButtonDown);
            _presenter.MouseMove -= new MouseEventHandler(_presenter_MouseMove);
            _presenter.MouseLeftButtonUp -= new MouseButtonEventHandler(_presenter_MouseLeftButtonUp);
            _presenter = null;
        }

        private InkPresenter _presenter = null;
        private Stroke _stroke = null;
        private StylusPointCollection _erasePoints = null;
        private DrawingAttributes _drawingAttributes = new DrawingAttributes();
    }
}
```

### <a name="update-the-xaml-for-the-default-page-and-add-a-code-behind-for-handwriting-recognition"></a><span data-ttu-id="e55c2-228">Aktualisieren der XAML-Datei für die Standardseite und Hinzufügen eines Code Behind für die Handschrifterkennung</span><span class="sxs-lookup"><span data-stu-id="e55c2-228">Update the XAML for the Default Page and Add a Code Behind for Handwriting Recognition</span></span>

<span data-ttu-id="e55c2-229">Nachdem Sie nun über eine Klasse verfügen, die frei Hand Eingaben sammelt, müssen Sie den XAML-Code in Page. XAML mit dem folgenden XAML-Code aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="e55c2-229">Now that you have a class that collects ink, you will need to update the XAML in page.xaml with the following XAML.</span></span> <span data-ttu-id="e55c2-230">Der folgende Code fügt dem Eingabebereich einen gelben Farbverlauf, ein InkCanvas-Steuerelement und eine Schaltfläche hinzu, die die Erkennung auslöst.</span><span class="sxs-lookup"><span data-stu-id="e55c2-230">The following code adds a yellow gradient to the input area, an InkCanvas control, and a button that will trigger recognition.</span></span>

```XML
<UserControl x:Class="InkRecognition.Page"
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation" 
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml">
    <Grid x:Name="LayoutRoot" Background="White">
        <Grid.RowDefinitions>
            <RowDefinition Height="Auto"/>
            <RowDefinition Height="Auto"/>
        </Grid.RowDefinitions>
        <Border Margin="5" Grid.Row="0" BorderThickness="4" BorderBrush="Black" CornerRadius="5" Height="200">
            <Grid>
                <InkPresenter x:Name="inkCanvas">
                    <InkPresenter.Background>
                        <LinearGradientBrush StartPoint="0.5,0" EndPoint="0.5,1">
                            <GradientStop Offset="0" Color="Yellow"/>
                            <GradientStop Offset="1" Color="LightYellow"/>
                        </LinearGradientBrush>
                    </InkPresenter.Background>
                </InkPresenter>
                <Button Grid.Row="0" HorizontalAlignment="Right" VerticalAlignment="Bottom" Margin="10" Content="Recognize" Click="RecoButton_Click"/>
            </Grid>
        </Border>
        <Grid Grid.Row="1">
            <Grid.ColumnDefinitions>
                <ColumnDefinition Width="Auto"/>
                <ColumnDefinition Width="*"/>
            </Grid.ColumnDefinitions>
            <TextBlock Grid.Column="0" FontSize="28" Text="Result: "/>
            <ComboBox x:Name="results" Grid.Column="1" FontSize="28"/>
        </Grid>
    </Grid>
</UserControl>
```

<span data-ttu-id="e55c2-231">Ersetzen Sie die Code Behind-Seite Page. XAML. cs durch den folgenden Code, mit dem ein Ereignishandler für die Schaltfläche " **erkennen** " hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="e55c2-231">Replace the code behind page, Page.xaml.cs, with the following code that will add an event handler for the **Recognize** button.</span></span>

```CSharp
using System;
using System.Collections.Generic;
using System.Collections.ObjectModel;
using System.Linq;
using System.Net;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Animation;
using System.Windows.Shapes;
using InkRecognition.InkRecognitionServiceReference;

namespace InkRecognition
{
    public partial class Page : UserControl
    {
        public Page()
        {
            InitializeComponent();
            inkCol = new InkCollector(inkCanvas);
            recoClient = new InkRecognitionServiceClient();
            recoClient.RecognizeCompleted += new EventHandler<RecognizeCompletedEventArgs>(recoClient_RecognizeCompleted);
        }

        private void RecoButton_Click(object sender, RoutedEventArgs e)
        {
            // Serialize the ink into an array on ints.
            ObservableCollection<ObservableCollection<int>> packets = new ObservableCollection<ObservableCollection<int>>();
            double pixelToHimetricMultiplier = 2540d / 96d;

            foreach (Stroke stroke in inkCanvas.Strokes)
            {
                packets.Add(new ObservableCollection<int>());
                int index = inkCanvas.Strokes.IndexOf(stroke);
                for (int i = 0; i < stroke.StylusPoints.Count; i += 2)
                {
                    packets[index].Add(Convert.ToInt32(stroke.StylusPoints[i].X * pixelToHimetricMultiplier));
                    packets[index].Add(Convert.ToInt32(stroke.StylusPoints[i].Y * pixelToHimetricMultiplier));
                }
            }

            // Call the Web service.
            recoClient.RecognizeAsync(packets);
        }

        void recoClient_RecognizeCompleted(object sender, RecognizeCompletedEventArgs e)
        {
            // We have received results from the server, now display them.
            results.ItemsSource = e.Result;
            UpdateLayout();
            results.SelectedIndex = 0;
            inkCanvas.Strokes.Clear();
        }

        private InkRecognitionServiceClient recoClient = null;
        private InkCollector inkCol = null;
    }
}
```

### <a name="remove-secure-transport-directives-from-the-client-configuration"></a><span data-ttu-id="e55c2-232">Entfernen von sicheren Transport Direktiven aus der Client Konfiguration</span><span class="sxs-lookup"><span data-stu-id="e55c2-232">Remove Secure Transport Directives from the Client Configuration</span></span>

<span data-ttu-id="e55c2-233">Bevor Sie den WCF-Dienst nutzen können, müssen Sie alle sicheren Transport Optionen aus der Dienst Konfiguration entfernen, da sichere Transporte in den WCF-Diensten von Silverlight 2,0 derzeit nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e55c2-233">Before you can consume the WCF service, you must remove all secure transport options from the service configuration because secure transports are not currently supported in Silverlight 2.0 WCF services.</span></span> <span data-ttu-id="e55c2-234">Aktualisieren Sie aus dem Projekt inkrekognition die Sicherheitseinstellungen in ServiceReferences. ClientConfig.</span><span class="sxs-lookup"><span data-stu-id="e55c2-234">From the InkRecognition project, update the security settings in ServiceReferences.ClientConfig.</span></span> <span data-ttu-id="e55c2-235">Ändern der Sicherheits-XML-Datei</span><span class="sxs-lookup"><span data-stu-id="e55c2-235">Change the security XML from</span></span>

```XML
          <security mode="None">
            <transport>
              <extendedProtectionPolicy policyEnforcement="WhenSupported" />
            </transport>
          </security>
```

<span data-ttu-id="e55c2-236">zu</span><span class="sxs-lookup"><span data-stu-id="e55c2-236">to</span></span>

```XML
       <security mode="None"/>
```

<span data-ttu-id="e55c2-237">Nun sollte Ihre Anwendung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e55c2-237">Now, your application should run.</span></span> <span data-ttu-id="e55c2-238">In der folgenden Abbildung wird gezeigt, wie die Anwendung in awebpagemit einem im Erkennungs Feld eingegebenen Handschrift aussieht.</span><span class="sxs-lookup"><span data-stu-id="e55c2-238">The following image shows how the application looks within awebpagewith some handwriting entered into the recognition box.</span></span>

<span data-ttu-id="e55c2-239">![Anwendung in awebpage, bei der eine Handschrift in das Erkennungs Feld eingegeben wurde](images/demo-1.png)</span><span class="sxs-lookup"><span data-stu-id="e55c2-239">![Application within awebpagewith some handwriting entered into recognition box](images/demo-1.png)</span></span><br/>
<span data-ttu-id="e55c2-240">*Anwendung in awebpage, bei der eine Handschrift in das Erkennungs Feld eingegeben wurde*</span><span class="sxs-lookup"><span data-stu-id="e55c2-240">*Application within awebpagewith some handwriting entered into recognition box*</span></span>

<span data-ttu-id="e55c2-241">Die folgende Abbildung zeigt den erkannten Text in der Dropdown Liste " **Ergebnis** ".</span><span class="sxs-lookup"><span data-stu-id="e55c2-241">The following image shows the recognized text in the **Result** drop-down list.</span></span>

<span data-ttu-id="e55c2-242">![Anwendung innerhalb von awebpagewith erkannter Text in der Dropdown Liste "Ergebnis"](images/demo-2.png)</span><span class="sxs-lookup"><span data-stu-id="e55c2-242">![Application within awebpagewith recognized text in result drop-down list](images/demo-2.png)</span></span><br/>
<span data-ttu-id="e55c2-243">*Anwendung innerhalb von awebpagewith erkannter Text in der Dropdown Liste "Ergebnis"*</span><span class="sxs-lookup"><span data-stu-id="e55c2-243">*Application within awebpagewith recognized text in result drop-down list*</span></span>

 

 



