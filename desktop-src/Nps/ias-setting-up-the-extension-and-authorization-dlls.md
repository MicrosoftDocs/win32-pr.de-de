---
title: Einrichten der Erweiterungs-DLLs
description: Beim Start überprüft NPS die Registrierung auf eine Liste der aufzurufenden DLLs von Drittanbietern.
ms.assetid: fbbd9031-3ebe-47b8-8d8b-e359fa7d4b67
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e8589f31144f12b120f9a77f281dd57a9f30ce
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039309"
---
# <a name="setting-up-the-extension-dlls"></a><span data-ttu-id="2e041-103">Einrichten der Erweiterungs-DLLs</span><span class="sxs-lookup"><span data-stu-id="2e041-103">Setting Up the Extension DLLs</span></span>

> [!Note]  
> <span data-ttu-id="2e041-104">Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt.</span><span class="sxs-lookup"><span data-stu-id="2e041-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="2e041-105">Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS.</span><span class="sxs-lookup"><span data-stu-id="2e041-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="2e041-106">Im gesamten Text wird NPS verwendet, um auf alle Versionen des Dienstanbieter zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="2e041-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="2e041-107">Beim Start überprüft NPS die Registrierung auf eine Liste der aufzurufenden DLLs von Drittanbietern.</span><span class="sxs-lookup"><span data-stu-id="2e041-107">At startup, NPS checks the registry for a list of third-party DLLs to call.</span></span>

<span data-ttu-id="2e041-108">Wenn Sie eine Authentifizierungs-oder Autorisierungs-dll auf einem NPS-Server einrichten möchten, können Sie die Pfade zu den DLLs in Werten unter dem folgenden Registrierungsschlüssel auflisten:</span><span class="sxs-lookup"><span data-stu-id="2e041-108">To set up an Authentication or Authorization DLL on an NPS server, list the paths to the DLLs in values below the following registry key:</span></span>

<span data-ttu-id="2e041-109">**"HKLM \\ System \\ CurrentControlSet \\ Services \\ authsrv \\ Parameters"\\**</span><span class="sxs-lookup"><span data-stu-id="2e041-109">**HKLM\\System\\CurrentControlSet\\Services\\AuthSrv\\Parameters\\**</span></span>

<span data-ttu-id="2e041-110">Wenn die Parameter " **authsrv** " und " **Parameters** " nicht vorhanden sind, erstellen Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="2e041-110">If the **AuthSrv** and **Parameters** keys do not exist, create them.</span></span>

<span data-ttu-id="2e041-111">Der Wert zum Auflisten der authentifizierungserweiterungs-DLLs lautet:</span><span class="sxs-lookup"><span data-stu-id="2e041-111">The value in which to list the Authentication Extension DLLs is:</span></span>

<span data-ttu-id="2e041-112">**Extensiondlls**</span><span class="sxs-lookup"><span data-stu-id="2e041-112">**ExtensionDLLs**</span></span>

<span data-ttu-id="2e041-113">Der Wert für die Liste der Autorisierungs Erweiterungs-DLLs lautet:</span><span class="sxs-lookup"><span data-stu-id="2e041-113">The value in which to list the Authorization Extension DLLs is:</span></span>

<span data-ttu-id="2e041-114">**Authorizationdlls**</span><span class="sxs-lookup"><span data-stu-id="2e041-114">**AuthorizationDLLs**</span></span>

<span data-ttu-id="2e041-115">Die Werte für " **extensiondlls** " und " **authorizationdlls** " müssen den Typ " **reg \_ \_ MultiSZ**" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2e041-115">Both the **ExtensionDLLs** and **AuthorizationDLLs** values must be of type **REG\_MULTI\_SZ**.</span></span> <span data-ttu-id="2e041-116">Mit diesem Typ können Sie mehrere DLLs auflisten.</span><span class="sxs-lookup"><span data-stu-id="2e041-116">This type allows you to list multiple DLLs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e041-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2e041-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e041-118">Aufrufen der Erweiterungs-DLLs</span><span class="sxs-lookup"><span data-stu-id="2e041-118">Invoking the Extension DLLs</span></span>](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> <dt>

[<span data-ttu-id="2e041-119">Benutzer Identifizierungs Attribute</span><span class="sxs-lookup"><span data-stu-id="2e041-119">User Identification Attributes</span></span>](/windows/desktop/Nps/ias-user-identification-attributes)
</dt> </dl>

 

 