---
description: Die Windows-Sensor-und-Speicherort Plattform beinhaltet Datenschutzeinstellungen zum Schutz der persönlichen Benutzerinformationen.
ms.assetid: 24425ed2-7b94-4b05-b117-9118d2074f49
title: Datenschutz und Sicherheit auf der Plattform für Windows-Sensoren und-Orte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cb0bf50cd27de1fc7fd4f42bd7a8455a549eea3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346503"
---
# <a name="privacy-and-security-in-the-windows-sensor-and-location-platform"></a><span data-ttu-id="93d39-103">Datenschutz und Sicherheit auf der Plattform für Windows-Sensoren und-Orte</span><span class="sxs-lookup"><span data-stu-id="93d39-103">Privacy and Security in the Windows Sensor and Location Platform</span></span>

<span data-ttu-id="93d39-104">Die Windows-Sensor-und-Speicherort Plattform beinhaltet Datenschutzeinstellungen zum Schutz der persönlichen Benutzerinformationen.</span><span class="sxs-lookup"><span data-stu-id="93d39-104">The Windows Sensor and Location platform includes privacy settings to help protect users' personal information.</span></span>

<span data-ttu-id="93d39-105">Mithilfe der-Plattform können Sie sicherstellen, dass die Sensordaten auf folgende Weise privat bleiben, wenn der Datenschutz erforderlich ist:</span><span class="sxs-lookup"><span data-stu-id="93d39-105">The platform helps to ensure that sensor data remains private, when privacy is required, in the following ways:</span></span>

-   <span data-ttu-id="93d39-106">Standardmäßig sind Sensoren deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="93d39-106">By default, sensors are off.</span></span> <span data-ttu-id="93d39-107">Da der Platt Form Entwurf voraussetzt, dass jeder Sensor persönliche Daten bereitstellen kann, wird jeder Sensor so lange deaktiviert, bis der Benutzer die explizite Zustimmung zum Zugriff auf die Sensordaten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="93d39-107">Because the platform design presumes that any sensor can provide personal data, each sensor is disabled until the user provides explicit consent to access the sensor data.</span></span>
-   <span data-ttu-id="93d39-108">Windows stellt offen legungs Meldungen und Hilfe Inhalte für den Benutzer bereit.</span><span class="sxs-lookup"><span data-stu-id="93d39-108">Windows provides disclosure messages and Help content for the user.</span></span> <span data-ttu-id="93d39-109">Dieser Inhalt hilft Benutzern zu verstehen, wie sich Sensoren auf den Datenschutz Ihrer persönlichen Daten auswirken können, und hilft Benutzern dabei, fundierte Entscheidungen zu treffen.</span><span class="sxs-lookup"><span data-stu-id="93d39-109">This content helps users understand how sensors can affect the privacy of their personal data and helps users make informed decisions.</span></span>
-   <span data-ttu-id="93d39-110">Zum Erteilen von Berechtigungen für einen Sensor sind Administratorrechte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="93d39-110">Providing permission for a sensor requires administrator rights.</span></span>
-   <span data-ttu-id="93d39-111">Wenn Sie aktiviert ist, kann ein Sensorgerät für alle Programme verwendet werden, die unter einem bestimmten Benutzerkonto ausgeführt werden (oder für alle Benutzerkonten).</span><span class="sxs-lookup"><span data-stu-id="93d39-111">When it is enabled, a sensor device works for all programs running under a particular user account (or for all user accounts).</span></span> <span data-ttu-id="93d39-112">Dies schließt nicht interaktive Benutzer und Dienste ein, z. b. ASPNET oder System.</span><span class="sxs-lookup"><span data-stu-id="93d39-112">This includes noninteractive users and services, such as ASPNET or SYSTEM.</span></span> <span data-ttu-id="93d39-113">Wenn Sie z. b. einen GPS-Sensor für Ihr Benutzerkonto aktivieren, haben nur Programme, die unter Ihrem Benutzerkonto ausgeführt werden, Zugriff auf das GPS.</span><span class="sxs-lookup"><span data-stu-id="93d39-113">For example, if you enable a GPS sensor for your user account, only programs running under your user account have access to the GPS.</span></span> <span data-ttu-id="93d39-114">Wenn Sie das GPS für alle Benutzer aktivieren, kann jedes Programm, das unter einem beliebigen Benutzerkonto ausgeführt wird, auf das GPS zugreifen.</span><span class="sxs-lookup"><span data-stu-id="93d39-114">If you enable the GPS for all users, any program running under any user account has access to the GPS.</span></span>
-   <span data-ttu-id="93d39-115">Programme, die Sensoren verwenden, können eine Methode zum Öffnen eines System Dialogfelds aufzurufen, in dem Benutzer aufgefordert werden, benötigte Sensorgeräte zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="93d39-115">Programs that use sensors can call a method to open a system dialog box that prompts users to enable needed sensor devices.</span></span> <span data-ttu-id="93d39-116">Mit dieser Funktion können Entwickler und Benutzer auf einfache Weise sicherstellen, dass die Sensoren funktionieren, wenn Programme Sie benötigen, während Sie die Kontrolle über die Offenlegung von Sensordaten behalten.</span><span class="sxs-lookup"><span data-stu-id="93d39-116">This feature makes it easy for developers and users to make sure that sensors work when programs need them, while maintaining user control of disclosure of sensor data.</span></span>
-   <span data-ttu-id="93d39-117">Sensor Treiber verwenden ein spezielles Objekt, das alle e/a-Anforderungen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="93d39-117">Sensor drivers use a special object that processes all I/O requests.</span></span> <span data-ttu-id="93d39-118">Dieses Objekt stellt sicher, dass nur Programme mit Benutzer Berechtigung auf Sensordaten zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="93d39-118">This object makes sure that only programs that have user permission can access sensor data.</span></span>

 

 



