---
title: Benutzer Identifizierungs Attribute
description: Die Identität des Benutzers, der die Authentifizierung anfordert, wird für die NPS-Erweiterungs-DLLs in einer Reihe unterschiedlicher Attribute bereitgestellt.
ms.assetid: 2f741a81-e432-47fe-a14a-8b77ecd41e28
ms.tgt_platform: multiple
keywords:
- Attribute, Benutzeridentifikation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527bdffad376ce92fa2fd7c5d5330fb752fea6aa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341739"
---
# <a name="user-identification-attributes"></a><span data-ttu-id="f6a92-104">Benutzer Identifizierungs Attribute</span><span class="sxs-lookup"><span data-stu-id="f6a92-104">User Identification Attributes</span></span>

> [!Note]  
> <span data-ttu-id="f6a92-105">Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt.</span><span class="sxs-lookup"><span data-stu-id="f6a92-105">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="f6a92-106">Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS.</span><span class="sxs-lookup"><span data-stu-id="f6a92-106">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="f6a92-107">Im gesamten Text wird NPS verwendet, um auf alle Versionen des Dienstanbieter zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="f6a92-107">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="f6a92-108">Die Identität des Benutzers, der die Authentifizierung anfordert, wird für die NPS-Erweiterungs-DLLs in einer Reihe unterschiedlicher Attribute bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="f6a92-108">The identity of the user requesting authentication is supplied to the NPS Extension DLLs in a number of different attributes.</span></span>

-   <span data-ttu-id="f6a92-109">**ratusername**</span><span class="sxs-lookup"><span data-stu-id="f6a92-109">**ratUserName**</span></span>
-   <span data-ttu-id="f6a92-110">**ratstrippeer Name**</span><span class="sxs-lookup"><span data-stu-id="f6a92-110">**ratStrippedUserName**</span></span>
-   <span data-ttu-id="f6a92-111">**ratsqusername**</span><span class="sxs-lookup"><span data-stu-id="f6a92-111">**ratFQUserName**</span></span>

<span data-ttu-id="f6a92-112">Jedes Attribut stellt die Benutzeridentität in einem anderen Format bereit.</span><span class="sxs-lookup"><span data-stu-id="f6a92-112">Each attribute provides the user identity in a different format.</span></span> <span data-ttu-id="f6a92-113">Im Allgemeinen sollten Entwickler **ratstripetdusername** verwenden.</span><span class="sxs-lookup"><span data-stu-id="f6a92-113">In general, developers should use **ratStrippedUserName**.</span></span> <span data-ttu-id="f6a92-114">Die Verwendung des **ratusername** -Attributs und des **ratf qusername** -Attributs ist spezialisiertere.</span><span class="sxs-lookup"><span data-stu-id="f6a92-114">The uses of the **ratUserName** and **ratFQUserName** attributes are more specialized.</span></span>

> [!Note]  
> <span data-ttu-id="f6a92-115">Das User-Password-Attribut, **ratuserpassword**, wurde bereits entschlüsselt, wenn es an die Erweiterungs-DLL gesendet wird und in diesem Formular verwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="f6a92-115">The User-Password attribute, **ratUserPassword**, has already been decrypted when it is sent to the extension DLL and is usable in that form.</span></span>

 

## <a name="ratusername"></a><span data-ttu-id="f6a92-116">ratusername</span><span class="sxs-lookup"><span data-stu-id="f6a92-116">ratUserName</span></span>

<span data-ttu-id="f6a92-117">Das **ratusername** -Attribut enthält den Namen, der tatsächlich gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="f6a92-117">The **ratUserName** attribute contains the name that was actually sent "over the wire."</span></span> <span data-ttu-id="f6a92-118">NPS hat den Inhalt dieses Attributs in keiner Weise verarbeitet oder überprüft.</span><span class="sxs-lookup"><span data-stu-id="f6a92-118">NPS has not, in any way, processed or validated the contents of this attribute.</span></span> <span data-ttu-id="f6a92-119">Dieses Attribut ist möglicherweise überhaupt nicht verfügbar, da der Benutzer möglicherweise über eine Methode, z. b. eine Aufruferkennung, identifiziert worden ist.</span><span class="sxs-lookup"><span data-stu-id="f6a92-119">This attribute may not be available at all because the user may have been identified through a means such as caller ID.</span></span>

<span data-ttu-id="f6a92-120">Wenn dieses Attribut verfügbar ist, ist es bei Verwendung von [**radiusextensionprocess/Ex**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)nur im Plug-in-Punkt der Authentifizierungs Erweiterung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f6a92-120">When using [**RadiusExtensionProcess/Ex**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), if this attribute is available, it is available only at the Authentication Extension DLL plug-in point.</span></span> <span data-ttu-id="f6a92-121">Das **ratusername** -Attribut ist im Plug-in-Punkt der Autorisierungs Erweiterung nicht verfügbar, da die **radiusextensionprocess/Ex-** Funktionen in Autorisierungs Erweiterungs-DLLs nur die "ausgehenden" Attribute sehen.</span><span class="sxs-lookup"><span data-stu-id="f6a92-121">The **ratUserName** attribute is not available at the Authorization Extension DLL plug-in point because in Authorization Extension DLLs the **RadiusExtensionProcess/Ex** functions see only the "outbound" attributes.</span></span>

<span data-ttu-id="f6a92-122">Wenn dieses Attribut bei Verwendung von [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)verfügbar ist, ist es sowohl unter dem Plug-in-Endpunkt der Authentifizierungs Erweiterung als auch im Plug-in-Punkt der Autorisierungs Erweiterung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f6a92-122">When using [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), if this attribute is available, it is available at both the Authentication Extension DLL plug-in point and the Authorization Extension DLL plug-in point.</span></span>

## <a name="ratstrippedusername"></a><span data-ttu-id="f6a92-123">ratstrippeer Name</span><span class="sxs-lookup"><span data-stu-id="f6a92-123">ratStrippedUserName</span></span>

<span data-ttu-id="f6a92-124">" **Ratstripetdusername** " ist die Identität des Benutzers nach "Bereichs Einschränkung".</span><span class="sxs-lookup"><span data-stu-id="f6a92-124">The **ratStrippedUserName** is the user's identity after "realm stripping."</span></span> <span data-ttu-id="f6a92-125">Weitere Informationen zum Entfernen von Bereichen finden Sie im Thema " [Bereichs Namen](/previous-versions/windows/it-pro/windows-server-2003/cc779938(v=ws.10)) " unter http: \\ \\ technet2.Microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="f6a92-125">For more information on realm stripping, see the [Realm names](/previous-versions/windows/it-pro/windows-server-2003/cc779938(v=ws.10)) topic on http:\\\\technet2.microsoft.com.</span></span>

<span data-ttu-id="f6a92-126">Dieses Attribut ist möglicherweise im Plug-in-Endpunkt der Authentifizierungs Erweiterung, dem Plug-in-Endpunkt für die Autorisierungs Erweiterung oder beides vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f6a92-126">This attribute may be present at the Authentication Extension DLL plug-in point, the Authorization Extension DLL plug-in point, or both.</span></span> <span data-ttu-id="f6a92-127">Dieses Attribut weist garantiert folgendes Format auf:</span><span class="sxs-lookup"><span data-stu-id="f6a92-127">This attribute is guaranteed to have the format:</span></span>

<span data-ttu-id="f6a92-128">*Domänen ***\\*** Benutzername*</span><span class="sxs-lookup"><span data-stu-id="f6a92-128">*Domain ***\\*** UserName*</span></span>

<span data-ttu-id="f6a92-129">Dabei ist *Domäne* der NetBIOS-Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="f6a92-129">Where *Domain* is the NetBIOS domain name.</span></span>

## <a name="ratfqusername"></a><span data-ttu-id="f6a92-130">ratsqusername</span><span class="sxs-lookup"><span data-stu-id="f6a92-130">ratFQUserName</span></span>

<span data-ttu-id="f6a92-131">Das **ratfqusername** -Attribut ist der "voll qualifizierte" Benutzername.</span><span class="sxs-lookup"><span data-stu-id="f6a92-131">The **ratFQUserName** attribute is the "fully qualified" user name.</span></span>

<span data-ttu-id="f6a92-132">Dieses Attribut ist möglicherweise im Plug-in-Endpunkt der Authentifizierungs Erweiterung, dem Plug-in-Endpunkt für die Autorisierungs Erweiterung oder beides vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f6a92-132">This attribute may be present in the Authentication Extension DLL plug-in point, the Authorization Extension DLL plug-in point, or both.</span></span> <span data-ttu-id="f6a92-133">Allerdings kann sich das Format des-Attributs zwischen den beiden Plug-in-Punkten unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="f6a92-133">However, the format of the attribute may differ between the two plug-in points.</span></span> <span data-ttu-id="f6a92-134">Beim Plug-in-Plug-in für Authentifizierungs Erweiterungen weist dieses Attribut immer folgendes Format auf:</span><span class="sxs-lookup"><span data-stu-id="f6a92-134">At the Authentication Extension DLL plug-in point, this attribute will always be of the form:</span></span>

<span data-ttu-id="f6a92-135">*Domänen ***\\*** Benutzername*</span><span class="sxs-lookup"><span data-stu-id="f6a92-135">*Domain ***\\*** UserName*</span></span>

<span data-ttu-id="f6a92-136">Das Format des **ratsqusername** -Attributs am Plug-in-Punkt der Autorisierungs Erweiterung ist davon abhängig, ob der Benutzer ein Active Directory Benutzer ist.</span><span class="sxs-lookup"><span data-stu-id="f6a92-136">The format of the **ratFQUserName** attribute at the Authorization Extension DLL plug-in point depends on whether the user is an Active Directory user.</span></span>

-   <span data-ttu-id="f6a92-137">Wenn es sich bei dem Benutzer um einen lokalen Benutzer handelt **, hat das** gleiche Format wie für den Plug-in-Endpunkt der Authentifizierungs Erweiterungs-DLL:</span><span class="sxs-lookup"><span data-stu-id="f6a92-137">If the user is a local user **ratFQUserName** has the same format as for the Authentication Extension DLL plug-in point:</span></span>

    <span data-ttu-id="f6a92-138">*Domänen ***\\*** Benutzername*</span><span class="sxs-lookup"><span data-stu-id="f6a92-138">*Domain ***\\*** UserName*</span></span>

    <span data-ttu-id="f6a92-139">.</span><span class="sxs-lookup"><span data-stu-id="f6a92-139">.</span></span>

-   <span data-ttu-id="f6a92-140">Wenn der Benutzer ein Active Directory Benutzer ist, kann " **ratsqusername** " den Namen des Benutzers im "kanonischen" Format enthalten.</span><span class="sxs-lookup"><span data-stu-id="f6a92-140">If the user is an Active Directory user, **ratFQUserName** may contain the user's name in "canonical" format.</span></span> <span data-ttu-id="f6a92-141">Das kanonische Format ist das Format, das vom Active Directory verwendet wird, um den Benutzer zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f6a92-141">Canonical format is the format used by the Active Directory to identify the user.</span></span> <span data-ttu-id="f6a92-142">Dabei handelt es sich um den Pfad aus dem Stammverzeichnis der Active Directory Struktur, der die Organisationseinheit (OU) des Benutzers enthält.</span><span class="sxs-lookup"><span data-stu-id="f6a92-142">It is the path from the root of the Active Directory tree, and includes the user's Organizational Unit (OU).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6a92-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f6a92-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6a92-144">Einrichten der Erweiterungs-DLLs</span><span class="sxs-lookup"><span data-stu-id="f6a92-144">Setting Up the Extension DLLs</span></span>](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
</dt> <dt>

[<span data-ttu-id="f6a92-145">Aufrufen der Erweiterungs-DLLs</span><span class="sxs-lookup"><span data-stu-id="f6a92-145">Invoking the Extension DLLs</span></span>](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> </dl>

 

 