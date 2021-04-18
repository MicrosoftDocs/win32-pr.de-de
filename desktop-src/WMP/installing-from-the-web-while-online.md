---
title: Installation über das Web während der Online Installation
description: Installation über das Web während der Online Installation
ms.assetid: 891483b0-6ba4-4ed4-b043-c6c109dc696b
keywords:
- Windows Media Player Online Stores, die Installation über das Web während der Online Dokumentation
- Online Stores, Installation über das Web während der Online Dokumentation
- Geben Sie 1 Online Stores ein, und installieren Sie Sie online.
- Geben Sie 2 Online Stores ein, und installieren Sie Sie online.
- Windows Media Player Online Stores, Online Installationen aus dem Web
- Online-Stores, Online Installationen aus dem Web
- Typ 1 Online Stores, Online Installationen aus dem Web
- Typ 2 Online Stores, Online Installationen aus dem Web
- Online-Stores werden online aus dem Web installiert.
- Online Installationen von Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd342d3fc79cf3012d5bc290561a9b63167e044f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341459"
---
# <a name="installing-from-the-web-while-online"></a><span data-ttu-id="b2109-113">Installation über das Web während der Online Installation</span><span class="sxs-lookup"><span data-stu-id="b2109-113">Installing from the Web While Online</span></span>

<span data-ttu-id="b2109-114">Benutzer können Windows Media Player als Webdownload installieren, während eine Verbindung mit dem Internet besteht.</span><span class="sxs-lookup"><span data-stu-id="b2109-114">Users can install Windows Media Player as a Web download while connected to the Internet.</span></span> <span data-ttu-id="b2109-115">In diesem Fall kann Microsoft den von Ihnen angegebenen anfänglichen Onlinespeicher konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b2109-115">In this case, Microsoft can configure the initial online store that you specify.</span></span>

<span data-ttu-id="b2109-116">Verwenden Sie zum erneuten Verteilen von Windows Media Player auf diese Weise die folgende URL:</span><span class="sxs-lookup"><span data-stu-id="b2109-116">To redistribute Windows Media Player in this manner, use the following URL:</span></span>

<span data-ttu-id="b2109-117"> https://go.microsoft.com/fwlink/p/?linkid=32981&SV=*Version*&UserLocale =*localId*&Service =*Key*</span><span class="sxs-lookup"><span data-stu-id="b2109-117">https://go.microsoft.com/fwlink/p/?linkid=32981&SV=*version*&UserLocale=*localID*&Service=*key*</span></span>

<span data-ttu-id="b2109-118">Legen Sie in der vorangehenden URL *Key* auf den Schlüsselnamen für Ihren Online Store fest, und legen Sie *LocaleID* auf den Bezeichner des Gebiets Schemas fest, in dem der Speicherdienst bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="b2109-118">In the preceding URL, set *key* to the key name for your online store, and set *localeID* to the identifier of the locale where your store provides service.</span></span> <span data-ttu-id="b2109-119">Legen Sie für Windows Media Player 11 unter Windows XP oder 1 für Windows Media Player 10 *Version* auf 2 fest.</span><span class="sxs-lookup"><span data-stu-id="b2109-119">Set *version* to 2 for Windows Media Player 11 on Windows XP or 1 for Windows Media Player 10.</span></span> <span data-ttu-id="b2109-120">Die URL installiert Windows Media Player und legt den ersten aktiven Speicher auf den durch *Key* angegebenen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="b2109-120">The URL installs Windows Media Player and sets the initial active store to the one specified by *key*.</span></span>

<span data-ttu-id="b2109-121">Das folgende Beispiel zeigt eine URL, mit der Windows Media Player 11 installiert wird und Proseware als ersten aktiven Speicher festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="b2109-121">The following example shows a URL that installs Windows Media Player 11 and sets Proseware as the initial active store.</span></span> <span data-ttu-id="b2109-122">Der Wert 409 für *LocaleID* gibt an, dass Proseware Dienst im USA bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="b2109-122">The value of 409 for *localeID* indicates that Proseware provides service in the United States.</span></span>

https://go.microsoft.com/fwlink/p/?linkid=32981&SV=2&UserLocale=409&Service=Proseware

<span data-ttu-id="b2109-123">Wenn das serviceInfo-Dokument für den Online Shop ein install-Element enthält, wird der Setup Vorgang von Windows Media Player Setup angepasst.</span><span class="sxs-lookup"><span data-stu-id="b2109-123">If the ServiceInfo document for the online store includes an Install element, Windows Media Player setup will customize the setup process.</span></span> <span data-ttu-id="b2109-124">Wenn Sie die Attributwerte verwenden, werden Ihre Endbenutzer-Lizenzbedingungen (EULA) und ihre Datenschutzbestimmungen angezeigt. Außerdem wird die CAB-Datei auf dem Computer des Benutzers abgerufen und installiert.</span><span class="sxs-lookup"><span data-stu-id="b2109-124">Using the attribute values, setup displays your End User License Agreement (EULA) and your privacy statement, and also retrieves and installs your .cab file to the user's computer.</span></span> <span data-ttu-id="b2109-125">Beispielsweise können Sie diese Funktion verwenden, um die neueste Version eines COM-Objekts zu installieren, das für den Online Shop erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b2109-125">For example, you can use this feature to install the latest version of a COM object that your online store requires.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2109-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b2109-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2109-127">**Informationen, die von Typ 1 und Typ 2 Online Stores gemeinsam sind**</span><span class="sxs-lookup"><span data-stu-id="b2109-127">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="b2109-128">**Install-Element**</span><span class="sxs-lookup"><span data-stu-id="b2109-128">**Install Element**</span></span>](install-element.md)
</dt> <dt>

[<span data-ttu-id="b2109-129">**Servicinfo-Dokument**</span><span class="sxs-lookup"><span data-stu-id="b2109-129">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> <dt>

[<span data-ttu-id="b2109-130">**Festlegen des ersten Online Stores**</span><span class="sxs-lookup"><span data-stu-id="b2109-130">**Setting the Initial Online Store**</span></span>](setting-the-initial-online-store.md)
</dt> </dl>

 

 




