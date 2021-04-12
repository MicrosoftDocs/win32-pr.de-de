---
title: Bibliotheks Zugriff
description: Bibliotheks Zugriff
ms.assetid: 9f722531-a551-4ca9-be5f-01a291a180b0
keywords:
- Windows-Media Player, Bibliothek
- Windows Media Player-Objektmodell, Bibliothek
- Objektmodell, Bibliothek
- Windows Media Player Mobile, Bibliothek für Objektmodell
- Windows Media Player ActiveX-Steuerelement, Bibliothek für Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement, Bibliothek für Objektmodell
- ActiveX-Steuerelement, Bibliothek für Objektmodell
- Windows Media Player-Bibliothek, Zugriff
- Bibliothek, zugreifen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1a8fcc34324775d968f6eab49003c28452f76c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309979"
---
# <a name="library-access"></a><span data-ttu-id="98609-112">Bibliotheks Zugriff</span><span class="sxs-lookup"><span data-stu-id="98609-112">Library Access</span></span>

<span data-ttu-id="98609-113">Eigenschaften und Methoden des Windows Media Player-Objektmodells, die auf die Bibliothek zugreifen, benötigen entweder Lese-oder Lese-/Schreibzugriff auf die Datenbank.</span><span class="sxs-lookup"><span data-stu-id="98609-113">Properties and methods of the Windows Media Player object model that access the library require either read-only or read/write access to the database.</span></span> <span data-ttu-id="98609-114">Die Bibliothek enthält Informationen, die einige Benutzer als privat aufbewahren möchten und auf die nur mit Ihrer Zustimmung zugegriffen werden soll.</span><span class="sxs-lookup"><span data-stu-id="98609-114">The library contains information that some users want to keep private and that should be accessed or altered only with their consent.</span></span>

<span data-ttu-id="98609-115">Für Windows Media Player 9-Serie oder höher können Sie die Zugriffsebene Programm gesteuert festlegen.</span><span class="sxs-lookup"><span data-stu-id="98609-115">For Windows Media Player 9 Series or later, you can programmatically determine access level.</span></span> <span data-ttu-id="98609-116">Rufen Sie die *Einstellungen* ab, um die aktuelle Zugriffsebene zu ermitteln, die dem Code gewährt wurde. **mediaaccessrights** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="98609-116">To determine the current level of access granted to your code, retrieve the *Settings*.**mediaAccessRights** property.</span></span> <span data-ttu-id="98609-117">Diese Eigenschaft gibt "None", "Read" oder "Full" (Lese-/Schreibzugriff) zurück.</span><span class="sxs-lookup"><span data-stu-id="98609-117">That property returns "none", "read", or "full" (read/write).</span></span> <span data-ttu-id="98609-118">Um bestimmte Zugriffsrechte anzufordern, müssen Sie die *Einstellungen* aufrufen. **requestmediaaccessrights** -Methode, die einen Parameter übergibt, der die von Ihnen angeforderte Ebene angibt.</span><span class="sxs-lookup"><span data-stu-id="98609-118">To request specific access rights, call the *Settings*.**requestMediaAccessRights** method, passing a parameter that specifies the level you are requesting.</span></span> <span data-ttu-id="98609-119">Die-Methode zeigt dem Benutzer eine Meldung an, die die angeforderte Zugriffsebene erläutert, und gibt einen **booleschen** Wert zurück, der angibt, ob der Zugriff gewährt wurde.</span><span class="sxs-lookup"><span data-stu-id="98609-119">The method displays a message to the user explaining the requested level of access, and returns a **Boolean** value indicating whether the access was granted.</span></span>

<span data-ttu-id="98609-120">Bestimmte Zugriffsrechte werden automatisch abhängig davon erteilt, wo der Code in Relation zum Computer des Benutzers ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="98609-120">Certain access rights are granted automatically depending on where your code is running relative to the user's computer.</span></span>

-   <span data-ttu-id="98609-121">Wenn sich die Webseite oder das Programm auf dem Computer des Benutzers befindet, werden standardmäßig vollständige Zugriffsrechte gewährt.</span><span class="sxs-lookup"><span data-stu-id="98609-121">If your webpage or program is located on the user's computer, full access rights are granted by default.</span></span>
-   <span data-ttu-id="98609-122">Webseiten haben Lesezugriff auf den *Player*. **currentMedia**, *Player*. **currentwiedergabe** und *Medium*. **SourceUrl** , wenn sich die Webseite in einer Internet Explorer-Sicherheitszone befindet, die der gleichen oder weniger eingeschränkt ist als die Sicherheitszone des Medien Elements oder der Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="98609-122">Web pages have read access to *Player*.**currentMedia**, *Player*.**currentPlaylist**, and *Media*.**sourceURL** when the webpage is located in an Internet Explorer security zone that is the same as or less restricted than the security zone of the media item or playlist.</span></span>

    <span data-ttu-id="98609-123">Die Sicherheitszonen reichen von der geringsten Beschränkung bis zu den am meisten eingeschränkten Einschränkungen, sind die **Vertrauenswürdige** Zone (einschließlich des lokalen Computers des Benutzers), die **lokale Intranetzone** , die **Internet** Zone und die **Eingeschränkte** Zone.</span><span class="sxs-lookup"><span data-stu-id="98609-123">Ranging from least restricted to most restricted, the security zones are the **Trusted** zone (including the user's local computer), the **Local intranet** zone, the **Internet** zone, and the **Restricted** zone.</span></span>

    <span data-ttu-id="98609-124">Beispielsweise verfügt eine Webseite in der **lokalen Intranetzone** über vollständige Zugriffsrechte für *Player*. **currentMedia** wenn sich das entsprechende Medien Element im lokalen Intranet oder im Internet befindet, müssen Zugriffsrechte für Medienelemente, die sich auf dem lokalen Computer eines Benutzers oder auf einer Website in der **vertrauenswürdigen** Zone befinden, angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="98609-124">For example, a webpage in the **Local intranet** zone has full access rights to *Player*.**currentMedia** when the corresponding media item is on the local intranet or the Internet, but access rights must be requested for media items located on a user's local computer or on a website in the **Trusted** zone.</span></span>

<span data-ttu-id="98609-125">Sie sollten Ihre webbasierte oder Windows-basierte Anwendung in allen Sicherheitszonen testen, auf die Sie möglicherweise stoßen.</span><span class="sxs-lookup"><span data-stu-id="98609-125">You should test your Web-based or Windows-based application in all of the security zones it may encounter.</span></span> <span data-ttu-id="98609-126">Die Anwendung sollte so entworfen werden, dass Denial-of-Access-Anforderungen ordnungsgemäß verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="98609-126">The application should be designed to handle denial of an access request correctly.</span></span>

<span data-ttu-id="98609-127">Für Windows Media Player-Objektmodell Versionen vor Windows Media Player 9-Reihe sind **mediaaccessrights** oder **requestmediaaccessrights** nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="98609-127">Windows Media Player object model versions prior to Windows Media Player 9 Series do not include **mediaAccessRights** or **requestMediaAccessRights**.</span></span> <span data-ttu-id="98609-128">Diese früheren Versionen von Windows Media Player es dem Benutzer ermöglichen, Zugriffsebenen mithilfe des Dialog Felds **Optionen** festzulegen.</span><span class="sxs-lookup"><span data-stu-id="98609-128">These earlier versions of Windows Media Player enable the user to set access levels using the **Options** dialog box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="98609-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="98609-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98609-130">**Einstellungs Objekt**</span><span class="sxs-lookup"><span data-stu-id="98609-130">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="98609-131">**Arbeiten mit der Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="98609-131">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




