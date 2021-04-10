---
title: DRM-Individualisierung
description: DRM-Individualisierung
ms.assetid: 8f129bc1-3db9-4b41-9d60-daff037237ff
keywords:
- Windows Media-Format-SDK, DRM-Individualisierung
- Digital Rights Management (DRM), Individualisierung
- DRM (Digital Rights Management), Individualisierung
- Individualisierung von DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 217be5cb5c1c7abef882c28961439baa93011c29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309615"
---
# <a name="drm-individualization"></a><span data-ttu-id="d8827-107">DRM-Individualisierung</span><span class="sxs-lookup"><span data-stu-id="d8827-107">DRM Individualization</span></span>

<span data-ttu-id="d8827-108">Besitzer geschützter Inhalte erfordern möglicherweise, dass Benutzer einige der im Windows Media SDK-SDK enthaltenen Digital Rights Management (DRM)-Komponenten aktualisieren, bevor Sie auf ihren Inhalt zugreifen.</span><span class="sxs-lookup"><span data-stu-id="d8827-108">Owners of protected content may require users to upgrade some of the digital rights management (DRM) components included in the Windows Media Format SDK before accessing their content.</span></span> <span data-ttu-id="d8827-109">Wenn ein Benutzer das Upgrade annimmt, wird eine individualisierte Version einer Sicherheits Datei (die für Ihren Computer eindeutig ist) von einer Microsoft-Website heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="d8827-109">If a user accepts the upgrade, an individualized version of a security file (one unique to their computer) will be downloaded from a Microsoft Web site.</span></span> <span data-ttu-id="d8827-110">Wenn der Benutzer das Upgrade ablehnt, ist er nicht in der Lage, auf den Inhalt zuzugreifen. Allerdings sind Sie weiterhin in der Lage, auf ungeschützte Inhalte und geschützte Inhalte zuzugreifen, für die das Upgrade nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d8827-110">If the user declines the upgrade, they will not be able to access the content; however, they will still be able to access unprotected content and protected content that does not require the upgrade.</span></span> <span data-ttu-id="d8827-111">Durch die Durchführung eines Sicherheits Upgrades wird die von DRM angebotene Schutz Ebene erhöht.</span><span class="sxs-lookup"><span data-stu-id="d8827-111">Performing a security upgrade helps increase the level of protection offered by DRM.</span></span>

<span data-ttu-id="d8827-112">Die Individualisierung kann entweder beim Setup oder bei einer Anwendung, die eine geschützte ASF-Datei findet, durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d8827-112">Individualization can be done either at setup time or when an application first encounters a protected ASF file that requires it.</span></span> <span data-ttu-id="d8827-113">Da bei diesem Prozess die Systemkomponenten eines Benutzers geändert werden, muss die Anwendung den Benutzer benachrichtigen und seine informierte Zustimmung erhalten, bevor das Upgrade durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d8827-113">Because this process modifies a user's system components, the application must notify the user and obtain their informed consent before performing the upgrade.</span></span> <span data-ttu-id="d8827-114">Microsoft Windows Media Player beispielsweise ein Dialogfeld mit dem folgenden Text anzeigen:</span><span class="sxs-lookup"><span data-stu-id="d8827-114">Microsoft Windows Media Player, for example, shows a dialog box with the following text:</span></span>

<span data-ttu-id="d8827-115">**Sicherheits Upgrade erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d8827-115">**Security Upgrade Required**</span></span>

<span data-ttu-id="d8827-116">**Der Besitzer des geschützten Inhalts, auf den Sie zugreifen möchten, erfordert, dass Sie zunächst einige der Microsoft Digital Rights Management (DRM)-Komponenten auf Ihrem Computer aktualisieren.**</span><span class="sxs-lookup"><span data-stu-id="d8827-116">**The owner of the protected content you are trying to access requires you to first upgrade some of the Microsoft digital rights management (DRM) components on your computer.**</span></span>

<span data-ttu-id="d8827-117">**Klicken Sie zum Aktualisieren der DRM-Komponenten auf OK.**</span><span class="sxs-lookup"><span data-stu-id="d8827-117">**Click OK to upgrade your DRM components.**</span></span>

<span data-ttu-id="d8827-118">**Einzel**</span><span class="sxs-lookup"><span data-stu-id="d8827-118">**Details:**</span></span>

<span data-ttu-id="d8827-119">**Wenn Sie auf "OK" klicken, werden ein eindeutiger Bezeichner und eine DRM-Sicherheits Datei an einen Microsoft-Dienst im Internet gesendet. Die Datei wird durch eine angepasste Version ersetzt, die ihren eindeutigen Bezeichner enthält. Dadurch wird die von DRM bereitgestellte Schutz Ebene erhöht.**</span><span class="sxs-lookup"><span data-stu-id="d8827-119">**When you click OK, a unique identifier and a DRM security file are sent to a Microsoft service on the Internet. The file is replaced with a customized version that contains your unique identifier. This increases the level of protection provided by DRM.**</span></span>

<span data-ttu-id="d8827-120">Jede Anwendung, die eine Individualisierung unterstützt, sollte denselben oder einen ähnlichen Wortlaut verwenden.</span><span class="sxs-lookup"><span data-stu-id="d8827-120">Any application that supports individualization should use the same or similar wording.</span></span> <span data-ttu-id="d8827-121">Weitere Informationen zur Datenschutzrichtlinie von Microsoft finden Sie im Abschnitt [Datenschutz](privacy-statement.md) Bestimmungen in dieser Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="d8827-121">For more information on Microsoft's Privacy Policy, see the [Privacy Statement](privacy-statement.md) section of this documentation.</span></span>

> [!Note]  
> <span data-ttu-id="d8827-122">DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d8827-122">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d8827-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d8827-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8827-124">**Features digitaler Rights Management**</span><span class="sxs-lookup"><span data-stu-id="d8827-124">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="d8827-125">**Individualisieren von DRM-Anwendungen**</span><span class="sxs-lookup"><span data-stu-id="d8827-125">**Individualizing DRM Applications**</span></span>](individualizing-drm-applications.md)
</dt> </dl>

 

 




