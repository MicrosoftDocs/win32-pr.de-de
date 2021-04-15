---
title: Verwenden von NPS-Erweiterungen
description: Der Internet Authentifizierungsdienst (IAS) wurde umbenannt in Netzwerk Richtlinien Server (Network Policy Server, NPS).
ms.assetid: 3ee16279-7e11-4587-ae43-f0296b7e7594
ms.tgt_platform: multiple
keywords:
- Internet Authentifizierungsdienst IAS, Tasks
- Internet Authentication Service IAS, using
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1cc9f10c810ec9fe16618144db11686a1e2132
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "104516682"
---
# <a name="using-nps-extensions"></a><span data-ttu-id="f9265-105">Verwenden von NPS-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="f9265-105">Using NPS Extensions</span></span>

<span data-ttu-id="f9265-106">Der Internet Authentifizierungsdienst (IAS) wurde umbenannt in Netzwerk Richtlinien Server (Network Policy Server, NPS).</span><span class="sxs-lookup"><span data-stu-id="f9265-106">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS).</span></span> <span data-ttu-id="f9265-107">Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS.</span><span class="sxs-lookup"><span data-stu-id="f9265-107">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="f9265-108">Im gesamten Text wird NPS verwendet, um auf alle Versionen des Dienstanbieter zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="f9265-108">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

<span data-ttu-id="f9265-109">\* \* Windows Server 2008 R2 und Windows Server 2008: \* \*</span><span class="sxs-lookup"><span data-stu-id="f9265-109">\*\*Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="f9265-110">Die Beispiele für Dialin und mapname erweitern die NPS-Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="f9265-110">The DialIn and MapName samples extend NPS functionality.</span></span>



| <span data-ttu-id="f9265-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f9265-111">Sample</span></span>             | <span data-ttu-id="f9265-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9265-112">Description</span></span>                                                                                                                                                                                                     |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9265-113">Dialin</span><span class="sxs-lookup"><span data-stu-id="f9265-113">DialIn</span></span><br/>  | <span data-ttu-id="f9265-114">In diesem Beispiel wird eine RADIUS-Erweiterungs-DLL implementiert, mit der das einwählbit für den Benutzer überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="f9265-114">This sample implements a RADIUS extension DLL that checks the dial-in bit for the user.</span></span><br/>                                                                                                              |
| <span data-ttu-id="f9265-115">Mapname</span><span class="sxs-lookup"><span data-stu-id="f9265-115">MapName</span></span><br/> | <span data-ttu-id="f9265-116">Diese Beispiel Erweiterungs-DLL durchsucht alle vertrauenswürdigen Domänen nach dem vorgesehenen Konto.</span><span class="sxs-lookup"><span data-stu-id="f9265-116">This sample extension DLL searches all trusted domains for the designated account.</span></span> <span data-ttu-id="f9265-117">Dadurch können Benutzer aus mehreren Domänen authentifiziert werden, ohne dass die Benutzer ihren Domänen Namen angeben müssen.</span><span class="sxs-lookup"><span data-stu-id="f9265-117">This allows users from multiple domains to be authenticated without the users having to supply their domain name.</span></span><br/> |



 

<span data-ttu-id="f9265-118">Den Quellcode für die Beispielanwendungen mapname und Dialin finden Sie in der folgenden Liste.</span><span class="sxs-lookup"><span data-stu-id="f9265-118">You can find the source code for the MapName and DialIn sample applications in the following list.</span></span> <span data-ttu-id="f9265-119">*Speicherort*,% Installationspfad%, bestimmt das Basis Installationsverzeichnis für x64-Computer.</span><span class="sxs-lookup"><span data-stu-id="f9265-119">*Location*, %Install Path%, designates the base installation directory for x64 computers.</span></span> <span data-ttu-id="f9265-120">Weitere Informationen finden Sie unter Windows [Software Development Kit (SDK) für Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk), Microsoft Windows Software Development Kit (SDK) und [Downloads für die Entwicklung von Windows Store-Apps](https://msdn.microsoft.com/windows/apps/br229516).</span><span class="sxs-lookup"><span data-stu-id="f9265-120">See also [Windows Software Development Kit (SDK) for Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk), Microsoft Windows Software Development Kit (SDK), and [Downloads for Windows Store app development](https://msdn.microsoft.com/windows/apps/br229516).</span></span>

<dl> <dt>

<span data-ttu-id="f9265-121">Windows SDK für Windows 8</span><span class="sxs-lookup"><span data-stu-id="f9265-121">Windows SDK for Windows 8</span></span>
</dt> <dd>

<span data-ttu-id="f9265-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f9265-122">Windows Server 2012</span></span>

<span data-ttu-id="f9265-123">Download Link: N/v</span><span class="sxs-lookup"><span data-stu-id="f9265-123">Download link: N/A</span></span>

<span data-ttu-id="f9265-124">Mapname: Nein</span><span class="sxs-lookup"><span data-stu-id="f9265-124">MapName: No</span></span>

<span data-ttu-id="f9265-125">Dialin: Nein</span><span class="sxs-lookup"><span data-stu-id="f9265-125">DialIn: No</span></span>

<span data-ttu-id="f9265-126">Speicherort: N/v</span><span class="sxs-lookup"><span data-stu-id="f9265-126">Location: N/A</span></span>

</dd> <dt>

<span data-ttu-id="f9265-127">Microsoft Windows Software Development Kit (SDK) für Windows 7 und .NET Framework 4,0</span><span class="sxs-lookup"><span data-stu-id="f9265-127">Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0</span></span>
</dt> <dd>

<span data-ttu-id="f9265-128">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f9265-128">Windows Server 2008 R2</span></span>

<span data-ttu-id="f9265-129">Download Link: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279></span><span class="sxs-lookup"><span data-stu-id="f9265-129">Download link: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279></span></span>

<span data-ttu-id="f9265-130">Mapname: Ja</span><span class="sxs-lookup"><span data-stu-id="f9265-130">MapName: Yes</span></span>

<span data-ttu-id="f9265-131">Dialin: Nein</span><span class="sxs-lookup"><span data-stu-id="f9265-131">DialIn: No</span></span>

<span data-ttu-id="f9265-132">Speicherort:% Installationspfad% \\ Microsoft sdert \\ Windows \\ v 7.1 \\ Beispiele \\ netds \\ IAS</span><span class="sxs-lookup"><span data-stu-id="f9265-132">Location: %Install Path%\\Microsoft SDKs\\Windows\\v7.1\\Samples\\netds\\ias</span></span>

</dd> <dt>

<span data-ttu-id="f9265-133">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="f9265-133">Windows SDK</span></span>
</dt> <dd>

<span data-ttu-id="f9265-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9265-134">Windows Server 2008</span></span>

<span data-ttu-id="f9265-135">Download Link: <https://www.microsoft.com/download/details.aspx?id=5023></span><span class="sxs-lookup"><span data-stu-id="f9265-135">Download link: <https://www.microsoft.com/download/details.aspx?id=5023></span></span>

<span data-ttu-id="f9265-136">Mapname: Ja</span><span class="sxs-lookup"><span data-stu-id="f9265-136">MapName: Yes</span></span>

<span data-ttu-id="f9265-137">Dialin: Nein</span><span class="sxs-lookup"><span data-stu-id="f9265-137">DialIn: No</span></span>

<span data-ttu-id="f9265-138">Speicherort:% Installationspfad% \\ Microsoft sdert \\ Windows \\ v 6.1 \\ Beispiele \\ netds \\ IAS</span><span class="sxs-lookup"><span data-stu-id="f9265-138">Location: %Install Path%\\Microsoft SDKs\\Windows\\v6.1\\Samples\\NetDs\\IAS</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="f9265-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f9265-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9265-140">Downloads für Entwickler</span><span class="sxs-lookup"><span data-stu-id="f9265-140">Downloads for Developers</span></span>](https://msdn.microsoft.com/windows/apps/br229516)
</dt> <dt>

[<span data-ttu-id="f9265-141">Windows SDK für Windows 8</span><span class="sxs-lookup"><span data-stu-id="f9265-141">Windows SDK for Windows 8</span></span>](https://developer.microsoft.com/windows/downloads/windows-8-sdk)
</dt> </dl>

 

 





