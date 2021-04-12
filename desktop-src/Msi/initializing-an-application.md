---
description: Um die Installer-Funktionalität zu aktivieren, muss eine Anwendung bei der Initialisierung eine Reihe von Funktionen aufzurufen.
ms.assetid: cfeaf9b9-f772-49f9-8b6f-e7fd0c93cc9f
title: Initialisieren einer Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221c5d97f0febb23ba73f98605ee6ec0e853940c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215697"
---
# <a name="initializing-an-application"></a><span data-ttu-id="ebf6a-103">Initialisieren einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="ebf6a-103">Initializing an Application</span></span>

<span data-ttu-id="ebf6a-104">Um die Installer-Funktionalität zu aktivieren, muss eine Anwendung bei der Initialisierung eine Reihe von Funktionen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="ebf6a-104">To enable installer functionality, an application must call a number of functions when it is initializing.</span></span> <span data-ttu-id="ebf6a-105">Weitere Informationen finden Sie unter [Installationsmechanismus](installation-mechanism.md).</span><span class="sxs-lookup"><span data-stu-id="ebf6a-105">For more information, see [Installation Mechanism](installation-mechanism.md).</span></span> <span data-ttu-id="ebf6a-106">In den folgenden Schritten wird beschrieben, wie Sie mit dem Installationsprogramm eine Anwendung initialisieren:</span><span class="sxs-lookup"><span data-stu-id="ebf6a-106">The following steps describe how to use the installer to initialize an application:</span></span>

<span data-ttu-id="ebf6a-107">**So initialisieren Sie eine Anwendung**</span><span class="sxs-lookup"><span data-stu-id="ebf6a-107">**To initialize an application**</span></span>

1.  <span data-ttu-id="ebf6a-108">Aufrufen der Funktion " [**msigetproductcode**](/windows/desktop/api/Msi/nf-msi-msigetproductcodea) ", damit die Anwendung sich selbst beim Installer identifizieren kann.</span><span class="sxs-lookup"><span data-stu-id="ebf6a-108">Call the [**MsiGetProductCode**](/windows/desktop/api/Msi/nf-msi-msigetproductcodea) function so the application can identify itself to the installer.</span></span>

    <span data-ttu-id="ebf6a-109">Der Produktcode ist ein erforderlicher Parameter für viele Installer-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="ebf6a-109">The product code is a required parameter for many installer functions.</span></span>

2.  <span data-ttu-id="ebf6a-110">Rufen Sie die [**msigetuserinfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) -Funktion auf, um Benutzerinformationen beim ersten Start der Anwendung zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="ebf6a-110">Call the [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) function to collect user information the first time the application starts.</span></span>

    <span data-ttu-id="ebf6a-111">Wenn der [**msigetuserinfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) -Rückruf fehlschlägt, rufen Sie die [**msicollectuserinfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) -Funktion auf, um Benutzerinformationen zu sammeln.</span><span class="sxs-lookup"><span data-stu-id="ebf6a-111">If the call to [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) fails, call the [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) function to collect user information.</span></span>

3.  <span data-ttu-id="ebf6a-112">Zeigen Sie ggf. eine Standardbenutzer Oberfläche an, indem Sie die [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ebf6a-112">Display a default user interface, if necessary, by calling the [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) function.</span></span>

    <span data-ttu-id="ebf6a-113">Wenn Sie Ihre eigene Benutzeroberfläche erstellen möchten, registrieren Sie Sie beim Installer, indem Sie die Funktion [**msitentexternalui**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ebf6a-113">To author your own user interface, register it with the installer by calling the [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) function.</span></span>

4.  <span data-ttu-id="ebf6a-114">Ruft die [**msienablelog**](/windows/desktop/api/Msi/nf-msi-msienableloga) -Funktion auf, um den Protokolliergrad festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ebf6a-114">Call the [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) function to set the logging level.</span></span>
5.  <span data-ttu-id="ebf6a-115">Stellen Sie dem Benutzer verfügbare Funktionen bereit, indem Sie die Funktionen der Anwendung auflisten.</span><span class="sxs-lookup"><span data-stu-id="ebf6a-115">Present the user with available features by enumerating the features of your application.</span></span> <span data-ttu-id="ebf6a-116">Sie können Funktionen wie folgt auflisten:</span><span class="sxs-lookup"><span data-stu-id="ebf6a-116">You can enumerate features in the following ways:</span></span>
    -   <span data-ttu-id="ebf6a-117">Fragen Sie den Installer Feature-by-Feature ab.</span><span class="sxs-lookup"><span data-stu-id="ebf6a-117">Query the installer feature-by-feature.</span></span> <span data-ttu-id="ebf6a-118">Bevor die Anwendung z. b. eine Schaltfläche oder ein Menü Element zeichnet, ruft die Anwendung die [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) -Funktion auf, damit das Installationsprogramm überprüfen kann, ob die Funktion verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ebf6a-118">For example, before the application draws a button or a menu item, the application calls the [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) function so the installer can check that the feature is available.</span></span>
    -   <span data-ttu-id="ebf6a-119">Auflisten aller verfügbaren Features auf einmal durch Aufrufen der Funktion " [**msienumfeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) ".</span><span class="sxs-lookup"><span data-stu-id="ebf6a-119">Enumerate all of the available features at once by calling the [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) function.</span></span> <span data-ttu-id="ebf6a-120">Um diese Funktion verwenden zu können, muss die Anwendung **msienumschlag-Features** wiederholt beim Inkrementieren eines Indexes aufruft.</span><span class="sxs-lookup"><span data-stu-id="ebf6a-120">To use this function, the application must call **MsiEnumFeatures** repeatedly while incrementing an index.</span></span>
6.  <span data-ttu-id="ebf6a-121">Rufen Sie ausführliche Informationen über die aktuelle Installation ab, indem Sie die folgenden Enumerationsfunktionen wiederholt aufrufen und eine Index Variable für jeden Aufruf erhöhen:</span><span class="sxs-lookup"><span data-stu-id="ebf6a-121">Get detailed information about the current installation by calling the following enumeration functions repeatedly, incrementing an index variable for each call:</span></span>

    -   <span data-ttu-id="ebf6a-122">Wenden Sie die Funktion " [**msienumproducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) " an, um beim Installer registrierte Produkte aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="ebf6a-122">Call the [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) function to enumerate products registered with the installer.</span></span>
    -   <span data-ttu-id="ebf6a-123">Zum Auflisten von Komponenten müssen Sie die Funktion [**msienumcomponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa) aufzählen.</span><span class="sxs-lookup"><span data-stu-id="ebf6a-123">Call the [**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa) function to enumerate components.</span></span>
    -   <span data-ttu-id="ebf6a-124">Mit der Funktion " [**msienumcomponentqualifizierer**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa) " können Sie Komponenten Qualifizierer auflisten.</span><span class="sxs-lookup"><span data-stu-id="ebf6a-124">Call the [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa) function to enumerate component qualifiers.</span></span>
    -   <span data-ttu-id="ebf6a-125">Ruft die [**msienumclients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa) -Funktion auf, um die Produkte für eine bestimmte Komponente aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="ebf6a-125">Call the [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa) function to enumerate the products for a particular component.</span></span>

    <span data-ttu-id="ebf6a-126">Wenn der Rückgabewert einer Enumerationsfunktion ein Fehler \_ Erfolg ist, sind noch weitere Elemente aufzuzählen, und die Funktion sollte erneut mit einer inkrementierten Index Variable aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ebf6a-126">If the return value on an enumeration function is ERROR\_SUCCESS, there are still more items to be enumerated and the function should be called again with an incremented index variable.</span></span> <span data-ttu-id="ebf6a-127">Wenn der Rückgabewert fehlerhaft \_ ist \_ \_ , werden alle Elemente aufgezählt, und die Funktion sollte nicht erneut aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ebf6a-127">If the return value is ERROR\_NO\_MORE\_ITEMS, then all of the items have been enumerated, and the function should not be called again.</span></span>

 

 



