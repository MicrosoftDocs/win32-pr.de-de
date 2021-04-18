---
title: Entwickeln von universelle Windows-Plattform-Apps (UWP)
description: Entwickeln von universelle Windows-Plattform-Apps (UWP)
ms.assetid: 215256D7-CBBA-43B0-A99C-490A25D1F82C
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b3654c1c8773a813fcc7f88b21a86c2ef6049184
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "106340888"
---
# <a name="develop-universal-windows-platform-uwp-apps"></a><span data-ttu-id="d47fc-103">Entwickeln von universelle Windows-Plattform-Apps (UWP)</span><span class="sxs-lookup"><span data-stu-id="d47fc-103">Develop Universal Windows Platform (UWP) apps</span></span>

<span data-ttu-id="d47fc-104">Wir empfehlen, dass alle Microsoft Desktop-Apps (Win32) Ihre Desktop-Apps über die Desktop Bridge in die [universelle Windows-Plattform (UWP)](https://developer.microsoft.com/windows/bridges/desktop/) übertragen.</span><span class="sxs-lookup"><span data-stu-id="d47fc-104">We encourage all desktop (Win32) app ISVs to bring your desktop apps to the [Universal Windows Platform (UWP)](https://developer.microsoft.com/windows/bridges/desktop/) via the Desktop Bridge.</span></span> <span data-ttu-id="d47fc-105">Da UWP-Apps außerdem im [Windows Store](https://blogs.windows.com/buildingapps/2016/02/04/windows-store-trends-february-2016/) unterstützt werden, ist es für Sie einfacher, Ihrer Benutzerbasis ein automatisches Update auf eine konsistente Version zu bieten und Ihre Supportkosten zu senken.</span><span class="sxs-lookup"><span data-stu-id="d47fc-105">UWP apps are also supported in the [Windows Store](https://blogs.windows.com/buildingapps/2016/02/04/windows-store-trends-february-2016/), so it’s easier for you to update your users to a consistent version automatically, lowering your support costs.</span></span>

<span data-ttu-id="d47fc-106">Wenn Ihre Desktop-Apps nicht über die Desktop Bridge konvertiert werden können, wird dringend empfohlen, dass Sie ein Installationsprogramm verwenden, das die bewährten Methoden befolgt, und sicherstellen, dass dies vollständig getestet ist.</span><span class="sxs-lookup"><span data-stu-id="d47fc-106">If your desktop apps cannot be converted using the Desktop Bridge, we highly recommend that you use an installer that follows best practices, and ensure this is fully tested.</span></span> <span data-ttu-id="d47fc-107">Ein Installer ist die erste Benutzerfreundlichkeit Ihrer APP.</span><span class="sxs-lookup"><span data-stu-id="d47fc-107">An installer is your user or customer's first experience with your app.</span></span> <span data-ttu-id="d47fc-108">Dies ist häufig nicht der Fall, u. a. auch, weil das Programm nicht für alle Szenarien getestet wurde.</span><span class="sxs-lookup"><span data-stu-id="d47fc-108">All too often, this doesn’t work well or it hasn’t been fully tested for all scenarios.</span></span> <span data-ttu-id="d47fc-109">Das [zertifizierungskit für Windows-apps](https://dev.windows.com/develop/app-certification-kit) kann Ihnen helfen, die Installation und Deinstallation ihrer Win32-APP zu testen und die Verwendung nicht dokumentierter APIs sowie andere grundlegende leistungsbezogene Probleme zu identifizieren, die vor ihren Benutzern auftreten.</span><span class="sxs-lookup"><span data-stu-id="d47fc-109">The [Windows App Certification Kit](https://dev.windows.com/develop/app-certification-kit) can help you test install and uninstall of your Win32 app and help you identify use of undocumented APIs, as well as other basic performance-related best-practice issues before your users do.</span></span>

## <a name="best-practices"></a><span data-ttu-id="d47fc-110">Bewährten Methoden:</span><span class="sxs-lookup"><span data-stu-id="d47fc-110">Best practices:</span></span>

-   <span data-ttu-id="d47fc-111">Verwenden Sie Installationsprogramme, die die 32-Bit- und 64-Bit-Version von Windows unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d47fc-111">Use installers that work for both 32-bit and 64-bit versions of Windows.</span></span>
-   <span data-ttu-id="d47fc-112">Achten Sie beim Entwickeln Ihrer Installationsprogramme darauf, dass sie mehrere Szenarien (sowohl benutzer- als auch computerspezifisch) abdecken.</span><span class="sxs-lookup"><span data-stu-id="d47fc-112">Design your installers to run on multiple scenarios (user or machine level).</span></span>
-   <span data-ttu-id="d47fc-113">Alle weitervertreibbaren Windows-Komponenten sollten im Originalpaket verbleiben. Durch ein Umpacken kann das Installationsprogramm beschädigt werden.</span><span class="sxs-lookup"><span data-stu-id="d47fc-113">Keep all Windows redistributables in the original packaging – if you repackage these, it’s possible that this will break the installer.</span></span>
-   <span data-ttu-id="d47fc-114">Planen Sie Entwicklungszeit für Ihre Installationsprogramme ein. Häufig wird im Lebenszyklus der Softwareentwicklung übersehen, dass sie zum Lieferumfang dazugehören.</span><span class="sxs-lookup"><span data-stu-id="d47fc-114">Schedule development time for your installers—these are often overlooked as a deliverable during the software development lifecycle.</span></span>

 

 




