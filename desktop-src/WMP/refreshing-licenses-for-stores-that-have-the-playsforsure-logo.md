---
title: Aktualisieren von Lizenzen für Filialen mit dem PlaysForSure-Logo
description: Aktualisieren von Lizenzen für Filialen mit dem PlaysForSure-Logo
ms.assetid: d08d6b6e-937e-4dec-b7ca-376cdad069f9
keywords:
- Windows Media Player Online Stores, Aktualisieren von Lizenzen
- Online Stores, Lizenz Aktualisierung
- Windows Media Player Online Stores, Lizenz Aktualisierung
- Online Stores, Aktualisieren von Lizenzen
- Windows Media Player Online Stores, PlaysForSure-Logo
- Online Stores, PlaysForSure-Logo
- Aktualisieren von Lizenzen
- Lizenzen, aktualisieren
- PlaysForSure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e48a3ddfd2b0670e3720f7c71587d0330a69a7
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104101290"
---
# <a name="refreshing-licenses-for-stores-that-have-the-playsforsure-logo"></a><span data-ttu-id="21508-112">Aktualisieren von Lizenzen für Filialen mit dem PlaysForSure-Logo</span><span class="sxs-lookup"><span data-stu-id="21508-112">Refreshing Licenses for Stores That Have the PlaysForSure Logo</span></span>

<span data-ttu-id="21508-113">Bestimmte Online-Musikspeicher verfügen über das PlaysForSure-Logo, sind aber nicht in Windows Media Player 11 integriert.</span><span class="sxs-lookup"><span data-stu-id="21508-113">Certain online music stores have the PlaysForSure logo but are not integrated with Windows Media Player 11.</span></span> <span data-ttu-id="21508-114">Diese Speicher müssen ein serviceInfo-Dokument und eine Lightweight-Komponente bereitstellen, damit Windows Media Player 11 Lizenzen für Ihre Inhalte abrufen und aktualisieren kann.</span><span class="sxs-lookup"><span data-stu-id="21508-114">Those stores must provide a ServiceInfo document and a lightweight component so that Windows Media Player 11 can obtain and update licenses for their content.</span></span>

<span data-ttu-id="21508-115">Im folgenden Beispiel wird veranschaulicht, wie der Lizenz Aktualisierungsprozess funktioniert.</span><span class="sxs-lookup"><span data-stu-id="21508-115">The following example illustrates how the license updating process works.</span></span>

1.  <span data-ttu-id="21508-116">Der Benutzer erhält 50 Musiktitel aus dem Proseware Online Store.</span><span class="sxs-lookup"><span data-stu-id="21508-116">The user obtains 50 music tracks from the Proseware online store.</span></span> <span data-ttu-id="21508-117">Jede Spur ist eine Datei mit der Dateinamenerweiterung ". wma".</span><span class="sxs-lookup"><span data-stu-id="21508-117">Each track is a file with the .wma file name extension.</span></span> <span data-ttu-id="21508-118">Zusammen mit den Spuren erhält der Benutzerlizenzen, um die Spuren zu spielen.</span><span class="sxs-lookup"><span data-stu-id="21508-118">Along with the tracks, the user obtains licenses to play the tracks.</span></span>
2.  <span data-ttu-id="21508-119">Der Benutzer kopiert die 50-Spuren auf einen neuen Computer, auf dem Windows Media Player 11 installiert ist, und fügt die Spuren der Windows Media Player-Bibliothek hinzu.</span><span class="sxs-lookup"><span data-stu-id="21508-119">The user copies the 50 tracks to a new computer that has Windows Media Player 11 installed and adds the tracks to the Windows Media Player library.</span></span>
3.  <span data-ttu-id="21508-120">Zu einem späteren Zeitpunkt überprüft das License Refresh Module (LRM), das Teil von Windows Media Player 11 ist, die Metadaten in den 50-Spuren und bestimmt, dass Proseware der Inhaltsanbieter ist.</span><span class="sxs-lookup"><span data-stu-id="21508-120">At some later time, the License Refresh Module (LRM), which is part of Windows Media Player 11, inspects the metadata in the fifty tracks and determines that Proseware is the content provider.</span></span>
    > [!Note]  
    > <span data-ttu-id="21508-121">In Windows Media Player kann der Inhaltsanbieter identifiziert werden, indem das **contentdistributor** -Attribut in einer Mediendatei überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="21508-121">Windows Media Player is able to identify the content provider by inspecting the **ContentDistributor** attribute in a media file.</span></span> <span data-ttu-id="21508-122">Wenn ein Online Shop mit dem PlaysForSure-Logo eine Mediendatei bereitstellt, die Windows Media Digital Rights Management (WMDRM) verwendet, muss der Onlinespeicher das **contentdistributor** -Attribut in der Mediendatei platzieren.</span><span class="sxs-lookup"><span data-stu-id="21508-122">If an online store that has the PlaysForSure logo provides a media file that uses Windows Media Digital Rights Management (WMDRM), the online store must place the **ContentDistributor** attribute in the media file.</span></span> <span data-ttu-id="21508-123">Weitere Informationen finden Sie unter Hinzufügen des Content Distributor-Attributs im Windows Media Player SDK.</span><span class="sxs-lookup"><span data-stu-id="21508-123">For more information, see Adding the Content Distributor Attribute in the Windows Media Player SDK.</span></span>

     

4.  <span data-ttu-id="21508-124">Die LRM sucht nach der URL des serviceInfo-Dokuments von Proseware, lädt das Dokument herunter und überprüft das **install** -Element des Dokuments, um die URL eines Pakets abzurufen, das von der LRM zum Installieren der Komponente von Proseware verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="21508-124">The LRM looks up the URL of Proseware's ServiceInfo document, downloads the document, and inspects the document's **Install** element to obtain the URL of a package that the LRM can use to install Proseware's component.</span></span> <span data-ttu-id="21508-125">Der LRM installiert und lädt die Komponente.</span><span class="sxs-lookup"><span data-stu-id="21508-125">The LRM installs and loads the component.</span></span>
5.  <span data-ttu-id="21508-126">Für jede der 50-Spuren Ruft die LRM die [iwmpabonneptionservice:: allowplay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay) -Methode der Proseware-Komponente auf.</span><span class="sxs-lookup"><span data-stu-id="21508-126">For each of the 50 tracks, the LRM calls the Proseware component's [IWMPSubscriptionService::allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay) method.</span></span> <span data-ttu-id="21508-127">Mit der **allowplay** -Methode wird eine Lizenz für den einzelnen Titel auf dem neuen Computer platziert, und der Parameter " *pfallowplay* " gibt " **true** " zurück.</span><span class="sxs-lookup"><span data-stu-id="21508-127">The **allowPlay** method places a license for the individual track on the new computer and returns **TRUE** in the *pfAllowPlay* parameter.</span></span>
    > [!Note]  
    > <span data-ttu-id="21508-128">Die Proseware-Komponente muss alle Lizenzen bereitstellen, die für die Wiedergabe der einzelnen Spur erforderlich sind. Das heißt, die Komponente muss bei Bedarf sowohl eine Stamm Lizenz als auch eine Blatt Lizenz bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="21508-128">The Proseware component must provide all licenses required to play the individual track. That is, the component must provide both a root license and a leaf license if needed.</span></span>

     

    <span data-ttu-id="21508-129">Beim ersten Aufrufen der **allowplay** -Methode muss die Proseware-Komponente ein Dialogfeld anzeigen, um zu überprüfen, ob der aktuelle Benutzer über ein Proseware-Konto verfügt und über das Recht zum Wiedergeben des Titels verfügt. Bei nachfolgenden Aufrufen von **allowplay** kann die Komponente die Anmelde Informationen verwenden, die im ersten Aufruf abgerufen wurden, um zu überprüfen, ob der Benutzer über das Recht zum Wiedergeben der restlichen Spuren verfügt.</span><span class="sxs-lookup"><span data-stu-id="21508-129">During the first call to the **allowPlay** method, the Proseware component must display a dialog box to verify that the current user has a Proseware account and has the right to play the track. During subsequent calls to **allowPlay**, the component can use the credentials that it obtained in the first call to verify that the user has the right to play the remaining tracks.</span></span>

<span data-ttu-id="21508-130">Die Komponente, die vom Online Store geschrieben wird, muss die **allowplay** -Methode der **iwmpabonneptionservice** -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="21508-130">The component, which is written by the online store, must implement the **allowPlay** method of the **IWMPSubscriptionService** interface.</span></span> <span data-ttu-id="21508-131">Die Komponente muss E \_ notimpl von jeder der drei folgenden Methoden zurückgeben: **allowcdburn**, **allowpdatransfer** und **startbackgroundprocessing**.</span><span class="sxs-lookup"><span data-stu-id="21508-131">The component must return E\_NOTIMPL from each of the other three methods: **allowCDBurn**, **allowPDATransfer**, and **startBackgroundProcessing**.</span></span> <span data-ttu-id="21508-132">Außerdem muss die Komponente den Wert des Registrierungs Eintrags " **Funktionen** " auf "1" festlegen. Das heißt, dass das Abonnement \_ Cap \_ -allowplay-funktionsflag festgelegt werden muss, und alle anderen funktionsflags müssen gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="21508-132">Also, the component must set the value of the **Capabilities** registry entry to 1; that is, the SUBSCRIPTION\_CAP\_ALLOWPLAY capability flag must be set, and all other capability flags must be cleared.</span></span> <span data-ttu-id="21508-133">Weitere Informationen zum Registrieren der Komponente finden Sie unter [Registrierungsschlüssel und Einträge für den Online Store vom Typ 2](registry-keys-and-entries-for-a-type-2-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="21508-133">For more information about registering the component, see [Registry Keys and Entries for a Type 2 Online Store](registry-keys-and-entries-for-a-type-2-online-store.md).</span></span>

<span data-ttu-id="21508-134">Informationen zum Erstellen einer Komponente, die die **iwmpabonneptionservice** -Schnittstelle implementiert, finden Sie unter [Erstellen des Plug-Ins für einen Typ 2-Online Store](building-the-plug-in-for-a-type-2-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="21508-134">For information about creating a component that implements the **IWMPSubscriptionService** interface, see [Building the Plug-in for a Type 2 Online Store](building-the-plug-in-for-a-type-2-online-store.md).</span></span>

<span data-ttu-id="21508-135">Um Informationen zur Bereitstellung von Microsoft mit einem serviceInfo-Dokument zu erhalten, senden Sie eine e-Mail an das Windows Media Player Virtual Services-Team.</span><span class="sxs-lookup"><span data-stu-id="21508-135">For information about providing Microsoft with a ServiceInfo document, send email to the Windows Media Player Virtual Services team.</span></span> <span data-ttu-id="21508-136">Die e-Mail-Adresse des Teams lautet mpsvctm@microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="21508-136">The team's email address is mpsvctm@microsoft.com.</span></span>

<span data-ttu-id="21508-137">Technische Anleitungen zur Verwendung einer Vielzahl von Windows Media SDOs zum Erstellen eines Dienstanbieter, der lizenzierte Digital Media-Inhalte bietet, finden Sie im [Microsoft Windows Media Developer Center](https://msdn.microsoft.com/windowsmedia/default.aspx) , und suchen Sie nach "Erstellen eines Windows Media Player 10-Abonnements Online Store".</span><span class="sxs-lookup"><span data-stu-id="21508-137">For technical guidance on using a variety of Windows Media SDKs to create a service that offers licensed digital media content, go to the [Microsoft Windows Media Developer Center](https://msdn.microsoft.com/windowsmedia/default.aspx) and search for "Creating a Windows Media Player 10 Subscription Online Store".</span></span>

## <a name="related-topics"></a><span data-ttu-id="21508-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="21508-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21508-139">**Servicinfo-Dokument**</span><span class="sxs-lookup"><span data-stu-id="21508-139">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> <dt>

[<span data-ttu-id="21508-140">**Windows Media Player Online Stores**</span><span class="sxs-lookup"><span data-stu-id="21508-140">**Windows Media Player Online Stores**</span></span>](windows-media-player-online-stores.md)
</dt> </dl>

 

 




