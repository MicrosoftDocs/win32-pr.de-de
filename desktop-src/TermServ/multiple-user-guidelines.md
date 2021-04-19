---
title: Richtlinien für mehrere Benutzer
description: Richtlinien für die Entwicklung von Anwendungen für mehrere Benutzer in einer Remotedesktopdienste Umgebung.
ms.assetid: c7acbedb-3bf2-4519-ab11-a50bf071e757
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06db01da6d9413684e3197aa9758d6e5c04643f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339235"
---
# <a name="multiple-user-guidelines"></a><span data-ttu-id="80834-103">Richtlinien für mehrere Benutzer</span><span class="sxs-lookup"><span data-stu-id="80834-103">Multiple-user guidelines</span></span>

<span data-ttu-id="80834-104">In den folgenden Abschnitten finden Sie Richtlinien zum Entwickeln von Anwendungen für mehrere Benutzer in einer Remotedesktopdienste Umgebung.</span><span class="sxs-lookup"><span data-stu-id="80834-104">The following sections provide guidelines for developing applications for multiple users in a Remote Desktop Services environment.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="80834-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="80834-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="80834-106">Anwendungseinrichtung</span><span class="sxs-lookup"><span data-stu-id="80834-106">Application setup</span></span>](application-setup-in-a-terminal-services-environment.md)
</dt> <dd>

<span data-ttu-id="80834-107">Durch die Installation einer Anwendung für einen einzelnen Benutzer können Probleme in einer mehr Benutzer Remotedesktopdienste Umgebung entstehen.</span><span class="sxs-lookup"><span data-stu-id="80834-107">Installing an application for a single user can create problems in a multiuser Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="80834-108">Speichern von benutzerspezifischen Informationen</span><span class="sxs-lookup"><span data-stu-id="80834-108">Storing user-specific information</span></span>](storing-user-specific-information.md)
</dt> <dd>

<span data-ttu-id="80834-109">Anwendungen sollten benutzerspezifische Informationen an benutzerspezifischen Speicherorten speichern, die von den globalen, auf alle Benutzer bezogenen Informationen getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="80834-109">Applications should store user-specific information in user-specific locations, separately from global information that applies to all users.</span></span>

</dd> <dt>

[<span data-ttu-id="80834-110">Kernelobjektnamespaces</span><span class="sxs-lookup"><span data-stu-id="80834-110">Kernel object namespaces</span></span>](kernel-object-namespaces.md)
</dt> <dd>

<span data-ttu-id="80834-111">Remotedesktopdienste verwendet mehrere Namespaces für Kernel Objekte. ein globaler Namespace wird hauptsächlich von Diensten in Client/Server-Anwendungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="80834-111">Remote Desktop Services uses multiple namespaces for kernel objects; a global namespace is used primarily by services in client/server applications.</span></span>

</dd> <dt>

[<span data-ttu-id="80834-112">IP-Adressen und Computernamen</span><span class="sxs-lookup"><span data-stu-id="80834-112">IP addresses and computer names</span></span>](ip-addresses-and-computer-names.md)
</dt> <dd>

<span data-ttu-id="80834-113">Es darf nicht davon ausgegangen werden, dass der Computername oder die dem Computer zugewiesene IP-Adresse mit einem einzelnen Benutzer zusammenhängen, da mehrere Benutzer gleichzeitig an einem Remote Desktop Session Host-Server (RD Session Host) angemeldet sein können.</span><span class="sxs-lookup"><span data-stu-id="80834-113">It is not safe to assume that the computer name or the IP address assigned to the computer are associated with a single user because multiple users can be logged on simultaneously to a Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> </dl>

<span data-ttu-id="80834-114">Sperren Sie wie immer Dateien und Datenbanken, während Sie Änderungen vornehmen, um unbeabsichtigte Datenverluste zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="80834-114">As always, lock files and databases while making changes to prevent inadvertent loss of data.</span></span>

<span data-ttu-id="80834-115">Die Anwendung darf keine Lauf Zeit Anwendungs Dateien sperren, bei denen es sich nicht um benutzerspezifische Dateien handelt.</span><span class="sxs-lookup"><span data-stu-id="80834-115">Your application must not lock any run-time application files that are not per-user files.</span></span> <span data-ttu-id="80834-116">Gesperrte Laufzeitdateien können die Ausführung mehrerer Instanzen der Anwendung oder der Prozesse unter der Anwendung, z. b. Assistenten, behalten.</span><span class="sxs-lookup"><span data-stu-id="80834-116">Locked run-time files can keep multiple instances of the application, or processes under the application such as wizards, from running.</span></span> <span data-ttu-id="80834-117">Eine gute Möglichkeit, um zu testen, welche Dateien Lauf Zeit Anwendungs Dateien sind, besteht darin, zu verfolgen, welche Dateien vom Anwendungs Setup installiert werden.</span><span class="sxs-lookup"><span data-stu-id="80834-117">A good way to test which files are run-time application files is to track which files are installed by the application setup.</span></span> <span data-ttu-id="80834-118">Benutzerspezifische Dateien werden nur selten vom-Setup installiert. Daher sind die meisten Dateien, die durch das-Setup installiert werden, Lauf Zeit Anwendungs Dateien.</span><span class="sxs-lookup"><span data-stu-id="80834-118">Per-user files are rarely installed by setup; therefore, most files installed by setup are run-time application files.</span></span>

 

 




