---
title: Glossar für den Gerätezugriff
description: Die folgenden Begriffe werden in der gesamten Dokumentation für die Geräte Zugriffs-API verwendet.
Robots: noindex, nofollow
ms.assetid: A6311538-D7CC-4A23-A145-14AF3BBFC4C4
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 8406c41a2666f9014bac27452572c6f88b84e6bf
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "104389820"
---
# <a name="device-access-glossary"></a><span data-ttu-id="23052-103">Glossar für den Gerätezugriff</span><span class="sxs-lookup"><span data-stu-id="23052-103">Device Access Glossary</span></span>

<span data-ttu-id="23052-104">Die folgenden Begriffe werden in der gesamten Dokumentation für die Geräte Zugriffs-API verwendet.</span><span class="sxs-lookup"><span data-stu-id="23052-104">The following are terms used throughout the documentation for the Device Access API.</span></span>

<dl> <dt>

<span data-ttu-id="23052-105">**AppContainer**</span><span class="sxs-lookup"><span data-stu-id="23052-105">**AppContainer**</span></span>
</dt> <dd>

<span data-ttu-id="23052-106">Eine stark eingeschränkte Ausführungsumgebung, in der ein Prozess mit einer verringerten Teilmenge der Berechtigungen des Benutzers ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="23052-106">A highly restricted execution environment in which a process runs with a reduced subset of the user's privileges.</span></span> <span data-ttu-id="23052-107">Ein Prozess, der in einem appcontainer ausgeführt wird, wird als appcontainer-Prozess bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="23052-107">A process that's running within an AppContainer is called an AppContainer process.</span></span> <span data-ttu-id="23052-108">Ein appcontainer-Prozess ist von anderen appcontainer-Prozessen und vom Benutzerprofil isoliert.</span><span class="sxs-lookup"><span data-stu-id="23052-108">An AppContainer process is isolated from other AppContainer processes and from the user's profile.</span></span> <span data-ttu-id="23052-109">Der Zugriff auf eine sehr kleine Teilmenge von Systemressourcen wie Dateien, Geräte, Registrierungsschlüssel, IPC-Endpunkte (prozessübergreifende Communication, prozessübergreifende Communication) und Netzwerkressourcen ist beschränkt.</span><span class="sxs-lookup"><span data-stu-id="23052-109">It has limited access to a very small subset of system resources like files, devices, registry keys, interprocess communication (IPC)/remote procedure call (RPC) endpoints, and network resources.</span></span>

</dd> <dt>

<span data-ttu-id="23052-110">**Binding**</span><span class="sxs-lookup"><span data-stu-id="23052-110">**Binding**</span></span>
</dt> <dd>

<span data-ttu-id="23052-111">Zuordnen eines Geräte Zugriffs Objekts zu einer bestimmten Geräteschnittstelle</span><span class="sxs-lookup"><span data-stu-id="23052-111">Associating a device access object with a particular device interface.</span></span> <span data-ttu-id="23052-112">Wenn die Bindung erfolgreich ist, können Windows Store-Apps das Geräte Zugriffs Objekt als Broker für die Kommunikation mit dem Gerätetreiber verwenden.</span><span class="sxs-lookup"><span data-stu-id="23052-112">If binding is successful, Windows Store apps can use the device access object as a broker to communicate with the device driver.</span></span>

</dd> <dt>

<span data-ttu-id="23052-113">**Broker**</span><span class="sxs-lookup"><span data-stu-id="23052-113">**Broker**</span></span>
</dt> <dd>

<span data-ttu-id="23052-114">Eine Komponente, die Zugriff auf eine Ressource bereitstellt, die nicht standardmäßig erteilt wird.</span><span class="sxs-lookup"><span data-stu-id="23052-114">A component that provides access to a resource that isn't granted by default.</span></span>

</dd> <dt>

<span data-ttu-id="23052-115">**Privilegierte App**</span><span class="sxs-lookup"><span data-stu-id="23052-115">**Privileged App**</span></span>
</dt> <dd>

<span data-ttu-id="23052-116">Eine APP, die in den Metadaten eines bestimmten Geräts identifiziert wird, die dem Gerät zugeordnet ist, damit Sie mit der eingeschränkten Benutzeroberfläche des Gerätetreibers kommunizieren kann.</span><span class="sxs-lookup"><span data-stu-id="23052-116">An app that's identified in a particular device's metadata as associated with that device, so that it can communicate with the device driver's restricted interface.</span></span> <span data-ttu-id="23052-117">Ein Beispiel für eine solche APP könnte eine proprietäre Musikwiedergabe-APP sein, die über exklusive Berechtigungen für die Synchronisierung mit einem tragbaren Musikplayer verfügt, wenn apps von Wettbewerbern dies nicht tun können.</span><span class="sxs-lookup"><span data-stu-id="23052-117">An example of such an app might be a proprietary music playback app that has exclusive permission to sync with a portable music player, when apps from competitors can't.</span></span> <span data-ttu-id="23052-118">Weitere Informationen zum Festlegen der Metadaten eines Geräts oder zum Einschränken eines Treibers auf privilegierte apps finden Sie unter [UWP-Geräte-Apps für interne Geräte](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices).</span><span class="sxs-lookup"><span data-stu-id="23052-118">For more information about how to set a device's metadata or how to restrict a driver to privileged apps, see [UWP device apps for internal devices](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices).</span></span>

</dd> </dl>
