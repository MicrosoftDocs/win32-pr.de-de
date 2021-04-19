---
description: Nachdem ein Gerätetreiber eine gesamte Journal Datei in unformatierte Geräte Befehle konvertiert hat, wird die Datei der konvertierten Befehle an den Spooler zurückgegeben.
ms.assetid: 149e44d0-052a-48ba-8f65-59eab193c785
title: Port Monitore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa4b00e4171b3fd6e366a66deae8f5e70578ca92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364050"
---
# <a name="port-monitors"></a><span data-ttu-id="9cb39-103">Port Monitore</span><span class="sxs-lookup"><span data-stu-id="9cb39-103">Port Monitors</span></span>

<span data-ttu-id="9cb39-104">Nachdem ein Gerätetreiber eine gesamte Journal Datei in unformatierte Geräte Befehle konvertiert hat, wird die Datei der konvertierten Befehle an den Spooler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9cb39-104">Once a device driver has converted an entire journal file into raw device commands, the file of converted commands is passed back to the spooler.</span></span> <span data-ttu-id="9cb39-105">Der Spooler sendet diese Befehle auf niedriger Ebene an einen Monitor.</span><span class="sxs-lookup"><span data-stu-id="9cb39-105">The spooler sends these low-level commands to a monitor.</span></span> <span data-ttu-id="9cb39-106">Bei einem Port Monitor handelt es sich um eine DLL, die die unformatierten Geräte Befehle über das Netzwerk, über einen parallelen Port oder über einen seriellen Anschluss an das Druckergerät übergibt.</span><span class="sxs-lookup"><span data-stu-id="9cb39-106">A port monitor is a .dll that passes the raw device commands over the network, through a parallel port, or through a serial port to the printer device.</span></span> <span data-ttu-id="9cb39-107">Benutzerdefinierte Port Monitore können installiert werden, um die Übergabe von Gerätedaten über andere Kommunikationsports zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9cb39-107">Custom port monitors can be installed to support passing device data through other communication ports.</span></span>

<span data-ttu-id="9cb39-108">Verwenden Sie die folgenden Funktionen, um mit Port Monitoren zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="9cb39-108">Use the following functions to work with port monitors.</span></span>



| <span data-ttu-id="9cb39-109">Funktion</span><span class="sxs-lookup"><span data-stu-id="9cb39-109">Function</span></span>                               | <span data-ttu-id="9cb39-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9cb39-110">Description</span></span>                                                                         |
|----------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="9cb39-111">**Addmonitor**</span><span class="sxs-lookup"><span data-stu-id="9cb39-111">**AddMonitor**</span></span>](addmonitor.md)       | <span data-ttu-id="9cb39-112">Installiert einen lokalen Port Monitor und verknüpft die Konfigurations-, Daten-und Überwachungs Dateien.</span><span class="sxs-lookup"><span data-stu-id="9cb39-112">Installs a local port monitor and links the configuration, data, and monitor files.</span></span> |
| [<span data-ttu-id="9cb39-113">**Deletemonitor**</span><span class="sxs-lookup"><span data-stu-id="9cb39-113">**DeleteMonitor**</span></span>](deletemonitor.md) | <span data-ttu-id="9cb39-114">Entfernt einen von der [**addmonitor**](addmonitor.md) -Funktion hinzugefügten Port Monitor.</span><span class="sxs-lookup"><span data-stu-id="9cb39-114">Removes a port monitor added by the [**AddMonitor**](addmonitor.md) function.</span></span>      |
| [<span data-ttu-id="9cb39-115">**Enumüberwachungen**</span><span class="sxs-lookup"><span data-stu-id="9cb39-115">**EnumMonitors**</span></span>](enummonitors.md)   | <span data-ttu-id="9cb39-116">Listet die auf einem angegebenen Server installierten Port Monitore auf.</span><span class="sxs-lookup"><span data-stu-id="9cb39-116">Enumerates the port monitors installed on a specified server.</span></span>                       |



 

 

 



