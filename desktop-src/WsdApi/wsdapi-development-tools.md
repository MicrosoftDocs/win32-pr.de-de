---
description: Die WSDAPI-Entwicklungs Tools, die im Windows SDK (WSD-CodeGen, WSD-debughost und WSD-Debugclient) enthalten sind, ermöglichen Entwicklern das Erstellen und Debuggen von WSDAPI-basierten Clients und Geräten.
ms.assetid: 8bf6424e-1eed-4b0a-9d56-7aaf03a47992
title: WSDAPI-Entwicklungs Tools
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd245e347cab6205a8883126dcae281646a3488f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345846"
---
# <a name="wsdapi-development-tools"></a><span data-ttu-id="97276-103">WSDAPI-Entwicklungs Tools</span><span class="sxs-lookup"><span data-stu-id="97276-103">WSDAPI Development Tools</span></span>

<span data-ttu-id="97276-104">Die WSDAPI-Entwicklungs Tools, die im Windows SDK (WSD-CodeGen, WSD-debughost und WSD-Debugclient) enthalten sind, ermöglichen Entwicklern das Erstellen und Debuggen von WSDAPI-basierten Clients und Geräten.</span><span class="sxs-lookup"><span data-stu-id="97276-104">The WSDAPI development tools included in the Windows SDK (WSD CodeGen, WSD Debug Host, and WSD Debug Client) enable developers to create and debug WSDAPI-based clients and devices.</span></span> <span data-ttu-id="97276-105">Der Quellcode für diese Tools ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="97276-105">The source code for these tools is not available.</span></span> <span data-ttu-id="97276-106">Die SDK-Tools befinden sich im folgenden Verzeichnis: <Windows SDK Install Folder> \\ bin.</span><span class="sxs-lookup"><span data-stu-id="97276-106">SDK tools are located in the following directory: <Windows SDK Install Folder>\\Bin.</span></span>

<span data-ttu-id="97276-107">WSD CodeGen (wsdcodegen.exe) konvertiert einen WSDL-Vertrag in generierten C++-Code, der von Entwicklern direkt in aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="97276-107">WSD CodeGen (wsdcodegen.exe) converts a WSDL contract into generated C++ code, which developers can call directly into.</span></span> <span data-ttu-id="97276-108">Sie behandelt die Datenserialisierung und die Netzwerkdarstellung, damit Entwickler sich auf das Entwerfen von Anwendungen konzentrieren können.</span><span class="sxs-lookup"><span data-stu-id="97276-108">It handles the data serialization and wire representation so developers can focus on designing applications.</span></span> <span data-ttu-id="97276-109">Weitere Informationen zu WSD CodeGen finden Sie unter [Code-Generator für Webdienste auf Geräten](web-services-for-devices-code-generator.md).</span><span class="sxs-lookup"><span data-stu-id="97276-109">For more information about WSD CodeGen, see [Web Services on Devices Code Generator](web-services-for-devices-code-generator.md).</span></span> <span data-ttu-id="97276-110">Dieses Tool ist im Microsoft Windows Software Development Kit (SDK) und im Windows-Treiberkit (WDK) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="97276-110">This tool is available in the Microsoft Windows Software Development Kit (SDK) and in the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="97276-111">Die Tools WSD Debug Host (wsddebug \_host.exe) und WSD Debug Client (wsddebug \_client.exe) helfen Entwicklern beim Debuggen Ihrer Clients und Hosts.</span><span class="sxs-lookup"><span data-stu-id="97276-111">The WSD Debug Host (wsddebug\_host.exe) and WSD Debug Client (wsddebug\_client.exe) tools help developers debug their clients and hosts.</span></span> <span data-ttu-id="97276-112">Diese Tools können zum Überprüfen und Überprüfen von WS-Discovery-und Metadatenaustausch-Datenverkehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="97276-112">These tools can be used to verify and inspect WS-Discovery and metadata exchange traffic.</span></span> <span data-ttu-id="97276-113">Weitere Informationen zum WSD-debughost und zum WSD-Debugclient finden Sie unter [Debugtools](debugging-tools.md).</span><span class="sxs-lookup"><span data-stu-id="97276-113">For more information about WSD Debug Host and WSD Debug Client, see [Debugging Tools](debugging-tools.md).</span></span> <span data-ttu-id="97276-114">Diese Tools sind nur in der Windows SDK verfügbar.</span><span class="sxs-lookup"><span data-stu-id="97276-114">These tools are available only in the Windows SDK.</span></span>

<span data-ttu-id="97276-115">Es gibt ein zusätzliches Entwicklungs Tool namens [WSDAPI Basic Interoperabilitäts Tool (wsdbit)](https://msdn.microsoft.com/library/cc264250.aspx), das nur im WDK verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="97276-115">There is an additional development tool, named [WSDAPI Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx), that is available only in the WDK.</span></span> <span data-ttu-id="97276-116">Dieses Tool wird zum Testen von Dienst Methoden, MTOM (Message Transmission Optimization Mechanism), Anlagen oder WS-Eventing verwendet.</span><span class="sxs-lookup"><span data-stu-id="97276-116">This tool is used for testing service methods, Message Transmission Optimization Mechanism (MTOM), attachments or WS-Eventing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97276-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="97276-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97276-118">WSD-Anwendungsentwicklung unter Windows</span><span class="sxs-lookup"><span data-stu-id="97276-118">WSD Application Development on Windows</span></span>](wsd-application-development-on-windows.md)
</dt> <dt>

[<span data-ttu-id="97276-119">Code-Generator für Webdienste auf Geräten</span><span class="sxs-lookup"><span data-stu-id="97276-119">Web Services on Devices Code Generator</span></span>](web-services-for-devices-code-generator.md)
</dt> <dt>

[<span data-ttu-id="97276-120">WSDAPI Basic Interoperabilitäts Tool (wsdbit)</span><span class="sxs-lookup"><span data-stu-id="97276-120">WSDAPI Basic Interoperability Tool (WSDBIT)</span></span>](https://msdn.microsoft.com/library/cc264250.aspx)
</dt> <dt>

[<span data-ttu-id="97276-121">Debugtools</span><span class="sxs-lookup"><span data-stu-id="97276-121">Debugging Tools</span></span>](debugging-tools.md)
</dt> </dl>

 

 



