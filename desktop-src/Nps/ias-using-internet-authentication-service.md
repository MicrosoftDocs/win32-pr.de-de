---
title: Verwenden von NPS-Erweiterungen
description: Erfahren Sie mehr über die Verwendung von NPS-Erweiterungen. Internet Authentication Service (IAS) wurde in Network Policy Server (NPS) umbenannt.
ms.assetid: 3ee16279-7e11-4587-ae43-f0296b7e7594
ms.tgt_platform: multiple
keywords:
- Internet Authentication Service IAS , Tasks
- Internetauthentifizierungsdienst IAS mit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f422c005d6810a4035450e24de1324b28361f1
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989069"
---
# <a name="using-nps-extensions"></a><span data-ttu-id="8aeeb-106">Verwenden von NPS-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="8aeeb-106">Using NPS Extensions</span></span>

<span data-ttu-id="8aeeb-107">Internet Authentication Service (IAS) wurde in Network Policy Server (NPS) umbenannt.</span><span class="sxs-lookup"><span data-stu-id="8aeeb-107">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS).</span></span> <span data-ttu-id="8aeeb-108">Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS.</span><span class="sxs-lookup"><span data-stu-id="8aeeb-108">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="8aeeb-109">Im gesamten Text wird NPS verwendet, um auf alle Versionen des Diensts zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="8aeeb-109">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

<span data-ttu-id="8aeeb-110">\*\*Windows Server 2008 R2 und Windows Server 2008: \*\*</span><span class="sxs-lookup"><span data-stu-id="8aeeb-110">\*\*Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="8aeeb-111">Die Beispiele DialIn und MapName erweitern die NPS-Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="8aeeb-111">The DialIn and MapName samples extend NPS functionality.</span></span>



| <span data-ttu-id="8aeeb-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8aeeb-112">Sample</span></span>             | <span data-ttu-id="8aeeb-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8aeeb-113">Description</span></span>                                                                                                                                                                                                     |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8aeeb-114">Dialin</span><span class="sxs-lookup"><span data-stu-id="8aeeb-114">DialIn</span></span><br/>  | <span data-ttu-id="8aeeb-115">In diesem Beispiel wird eine RADIUS-Erweiterungs-DLL implementiert, die das Einwählbit für den Benutzer überprüft.</span><span class="sxs-lookup"><span data-stu-id="8aeeb-115">This sample implements a RADIUS extension DLL that checks the dial-in bit for the user.</span></span><br/>                                                                                                              |
| <span data-ttu-id="8aeeb-116">MapName</span><span class="sxs-lookup"><span data-stu-id="8aeeb-116">MapName</span></span><br/> | <span data-ttu-id="8aeeb-117">Diese Beispielerweiterungs-DLL durchsucht alle vertrauenswürdigen Domänen nach dem angegebenen Konto.</span><span class="sxs-lookup"><span data-stu-id="8aeeb-117">This sample extension DLL searches all trusted domains for the designated account.</span></span> <span data-ttu-id="8aeeb-118">Dadurch können Benutzer aus mehreren Domänen authentifiziert werden, ohne dass die Benutzer ihren Domänennamen angeben müssen.</span><span class="sxs-lookup"><span data-stu-id="8aeeb-118">This allows users from multiple domains to be authenticated without the users having to supply their domain name.</span></span><br/> |



 

<span data-ttu-id="8aeeb-119">Den Quellcode für die MapName- und DialIn-Beispielanwendungen finden Sie in der folgenden Liste.</span><span class="sxs-lookup"><span data-stu-id="8aeeb-119">You can find the source code for the MapName and DialIn sample applications in the following list.</span></span> <span data-ttu-id="8aeeb-120">*Speicherort*, %Installationspfad%, bestimmt das Basisinstallationsverzeichnis für x64-Computer.</span><span class="sxs-lookup"><span data-stu-id="8aeeb-120">*Location*, %Install Path%, designates the base installation directory for x64 computers.</span></span> <span data-ttu-id="8aeeb-121">Siehe auch [Windows Software Development Kit (SDK) für Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk), Microsoft Windows Software Development Kit (SDK) und Downloads für die Entwicklung von Windows [Store-Apps.](https://msdn.microsoft.com/windows/apps/br229516)</span><span class="sxs-lookup"><span data-stu-id="8aeeb-121">See also [Windows Software Development Kit (SDK) for Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk), Microsoft Windows Software Development Kit (SDK), and [Downloads for Windows Store app development](https://msdn.microsoft.com/windows/apps/br229516).</span></span>

<dl> <dt>

<span data-ttu-id="8aeeb-122">Windows SDK für Windows 8</span><span class="sxs-lookup"><span data-stu-id="8aeeb-122">Windows SDK for Windows 8</span></span>
</dt> <dd>

<span data-ttu-id="8aeeb-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8aeeb-123">Windows Server 2012</span></span>

<span data-ttu-id="8aeeb-124">Downloadlink: N/A</span><span class="sxs-lookup"><span data-stu-id="8aeeb-124">Download link: N/A</span></span>

<span data-ttu-id="8aeeb-125">MapName: Nein</span><span class="sxs-lookup"><span data-stu-id="8aeeb-125">MapName: No</span></span>

<span data-ttu-id="8aeeb-126">DialIn: Nein</span><span class="sxs-lookup"><span data-stu-id="8aeeb-126">DialIn: No</span></span>

<span data-ttu-id="8aeeb-127">Standort: N/A</span><span class="sxs-lookup"><span data-stu-id="8aeeb-127">Location: N/A</span></span>

</dd> <dt>

<span data-ttu-id="8aeeb-128">Microsoft Windows Software Development Kit (SDK) für Windows 7 und .NET Framework 4.0</span><span class="sxs-lookup"><span data-stu-id="8aeeb-128">Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0</span></span>
</dt> <dd>

<span data-ttu-id="8aeeb-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8aeeb-129">Windows Server 2008 R2</span></span>

<span data-ttu-id="8aeeb-130">Downloadlink: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279></span><span class="sxs-lookup"><span data-stu-id="8aeeb-130">Download link: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279></span></span>

<span data-ttu-id="8aeeb-131">MapName: Ja</span><span class="sxs-lookup"><span data-stu-id="8aeeb-131">MapName: Yes</span></span>

<span data-ttu-id="8aeeb-132">DialIn: Nein</span><span class="sxs-lookup"><span data-stu-id="8aeeb-132">DialIn: No</span></span>

<span data-ttu-id="8aeeb-133">Speicherort: %Install Path% \\ Microsoft SDKs \\ Windows \\ v7.1 \\ Samples \\ netds \\ ias</span><span class="sxs-lookup"><span data-stu-id="8aeeb-133">Location: %Install Path%\\Microsoft SDKs\\Windows\\v7.1\\Samples\\netds\\ias</span></span>

</dd> <dt>

<span data-ttu-id="8aeeb-134">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="8aeeb-134">Windows SDK</span></span>
</dt> <dd>

<span data-ttu-id="8aeeb-135">WindowsServer 2008</span><span class="sxs-lookup"><span data-stu-id="8aeeb-135">Windows Server 2008</span></span>

<span data-ttu-id="8aeeb-136">Downloadlink: <https://www.microsoft.com/download/details.aspx?id=5023></span><span class="sxs-lookup"><span data-stu-id="8aeeb-136">Download link: <https://www.microsoft.com/download/details.aspx?id=5023></span></span>

<span data-ttu-id="8aeeb-137">MapName: Ja</span><span class="sxs-lookup"><span data-stu-id="8aeeb-137">MapName: Yes</span></span>

<span data-ttu-id="8aeeb-138">DialIn: Nein</span><span class="sxs-lookup"><span data-stu-id="8aeeb-138">DialIn: No</span></span>

<span data-ttu-id="8aeeb-139">Speicherort: %Installationspfad% \\ Microsoft SDKs \\ Windows \\ v6.1 \\ Samples \\ NetDs \\ IAS</span><span class="sxs-lookup"><span data-stu-id="8aeeb-139">Location: %Install Path%\\Microsoft SDKs\\Windows\\v6.1\\Samples\\NetDs\\IAS</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="8aeeb-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8aeeb-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8aeeb-141">Downloads für Entwickler</span><span class="sxs-lookup"><span data-stu-id="8aeeb-141">Downloads for Developers</span></span>](https://msdn.microsoft.com/windows/apps/br229516)
</dt> <dt>

[<span data-ttu-id="8aeeb-142">Windows SDK für Windows 8</span><span class="sxs-lookup"><span data-stu-id="8aeeb-142">Windows SDK for Windows 8</span></span>](https://developer.microsoft.com/windows/downloads/windows-8-sdk)
</dt> </dl>

 

 





