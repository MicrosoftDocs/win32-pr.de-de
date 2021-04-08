---
title: Verwenden von Bluetooth
description: In diesem Abschnitt werden Aufgaben beschrieben, die sich auf das Schreiben von Windows-basierten Anwendungen für Bluetooth beziehen.
ms.assetid: a5eddf48-b548-44a8-ac09-ce16f8aa3943
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b9b396de2635f9d1e76005c6638abb1d49c0ff
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734529"
---
# <a name="using-bluetooth"></a><span data-ttu-id="97cac-103">Verwenden von Bluetooth</span><span class="sxs-lookup"><span data-stu-id="97cac-103">Using Bluetooth</span></span>

<span data-ttu-id="97cac-104">In diesem Abschnitt werden Aufgaben beschrieben, die sich auf das Schreiben von Windows-basierten Anwendungen für Bluetooth beziehen.</span><span class="sxs-lookup"><span data-stu-id="97cac-104">This section describes tasks that are related to writing Windows-based applications for Bluetooth.</span></span>

<span data-ttu-id="97cac-105">Bluetooth stellt Programmier Definitionen in den Dateien Ws2bth. h und bluetoothapis. h bereit.</span><span class="sxs-lookup"><span data-stu-id="97cac-105">Bluetooth provides programming definitions in the Ws2bth.h and BluetoothAPIs.h files.</span></span> <span data-ttu-id="97cac-106">Die Datei bthsdpdef. h muss vor bluetoothapis. h enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="97cac-106">The Bthsdpdef.h file must be included before BluetoothAPIs.h.</span></span> <span data-ttu-id="97cac-107">Die Datei Ws2bth. h muss nach Winsock2. h eingeschlossen werden, damit Bluetooth-Sockets verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="97cac-107">The Ws2bth.h file must be included after Winsock2.h to use Bluetooth sockets.</span></span> <span data-ttu-id="97cac-108">Verknüpfen Sie nur mit bthrequi. lib, und vermeiden Sie das Verknüpfen mit "unrequi. lib".</span><span class="sxs-lookup"><span data-stu-id="97cac-108">Link only to Bthprops.lib, and avoid linking to Irprops.lib.</span></span> <span data-ttu-id="97cac-109">"Uncompatibility. lib" wird nur aus Gründen der Abwärtskompatibilität bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="97cac-109">Irprops.lib is provided for backward compatibility only.</span></span> <span data-ttu-id="97cac-110">Bthrequi. lib ist im Windows Vista SDK verfügbar.</span><span class="sxs-lookup"><span data-stu-id="97cac-110">Bthprops.lib is available in the Windows Vista SDK.</span></span> <span data-ttu-id="97cac-111">Sie können das Windows Vista SDK zum Entwickeln von Anwendungen für Windows XP mit Service Pack 2 (SP2) verwenden.</span><span class="sxs-lookup"><span data-stu-id="97cac-111">You can use the Windows Vista SDK to develop applications for Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="97cac-112">Das Windows Vista SDK ist im [Download Center](https://download.microsoft.com/download/a/7/7/a7767f09-0136-4a96-a1f8-276bf0ee31fa/Setup.exe)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="97cac-112">The Windows Vista SDK is available from the [Download Center](https://download.microsoft.com/download/a/7/7/a7767f09-0136-4a96-a1f8-276bf0ee31fa/Setup.exe).</span></span>

<span data-ttu-id="97cac-113">Alle standardmäßigen synchronen und überlappenden Mechanismen zum Lesen und Schreiben von Daten, die derzeit mit anderen Adressfamilien unterstützt werden, funktionieren ebenfalls ordnungsgemäß mit der AF- \_ BTH-Adressfamilie.</span><span class="sxs-lookup"><span data-stu-id="97cac-113">All standard synchronous and overlapped mechanisms to read and write data that are currently supported with other address families operate properly with the AF\_BTH address family as well.</span></span>

<span data-ttu-id="97cac-114">Im SDK ist ein Beispielcode enthalten, der eine einfache Bluetooth-Anwendung mit dem Winsock 2,2-und RFCOMM-Protokoll anzeigt.</span><span class="sxs-lookup"><span data-stu-id="97cac-114">There is some example code included with the SDK that shows a simple Bluetooth application using Winsock 2.2 and RFCOMM protocol.</span></span> <span data-ttu-id="97cac-115">Den Quellcode für das Beispiel finden Sie im SDK-Installationsverzeichnis unter C: \\ Program Files \\ Microsoft SDKs \\ Windows \\ <version number> \\ Samples \\ netds \\ Winsock \\ Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="97cac-115">The source code for the sample can be found in the SDK installation location under C:\\Program Files\\Microsoft SDKs\\Windows\\<version number>\\Samples\\NetDs\\winsock\\Bluetooth.</span></span>

<span data-ttu-id="97cac-116">In diesem Abschnitt werden die folgenden Themen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="97cac-116">This section describes the following topics.</span></span>



| <span data-ttu-id="97cac-117">`Section`</span><span class="sxs-lookup"><span data-stu-id="97cac-117">Section</span></span>                                                                                      | <span data-ttu-id="97cac-118">Inhalt</span><span class="sxs-lookup"><span data-stu-id="97cac-118">Content</span></span>                                                                          |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="97cac-119">Bluetooth-Programmierung mit Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="97cac-119">Bluetooth Programming with Windows Sockets</span></span>](bluetooth-programming-with-windows-sockets.md) | <span data-ttu-id="97cac-120">Erläutert die Verwendung von Windows Sockets-Schnittstellen zum Implementieren eines Bluetooth-Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="97cac-120">Explains how to use Windows Sockets interfaces to implement a Bluetooth network.</span></span> |



 

 

 




