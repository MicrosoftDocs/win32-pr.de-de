---
description: Die Anwendung muss die verfügbaren Kommunikationsressourcen inventarisieren und TAPI darüber benachrichtigen, welche Ressourcen von der Anwendung verwendet werden und wie Sie verwendet werden.
ms.assetid: 2246c4d2-f8ca-4950-adc6-af9a6e214fe9
title: Ressourcen Inventur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e743934f225fa4f932460eba0bbf895cc1bc21f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106363460"
---
# <a name="resource-inventory"></a><span data-ttu-id="77c9c-103">Ressourcen Inventur</span><span class="sxs-lookup"><span data-stu-id="77c9c-103">Resource Inventory</span></span>

<span data-ttu-id="77c9c-104">Die Anwendung muss die verfügbaren Kommunikationsressourcen inventarisieren und TAPI darüber benachrichtigen, welche Ressourcen von der Anwendung verwendet werden und wie Sie verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="77c9c-104">The application must inventory the communications resources available to it, then notify TAPI about which resources it will use and how it will use them.</span></span> <span data-ttu-id="77c9c-105">Weitere Informationen zu den Arten von Ressourcen und Funktionen, auf die eine Anwendung zugreifen kann, finden Sie unter [Gerätesteuerung](device-control.md) .</span><span class="sxs-lookup"><span data-stu-id="77c9c-105">See [Device Control](device-control.md) for additional information on the types of resources and capabilities an application might access.</span></span>

<span data-ttu-id="77c9c-106">**TAPI 2. x:** Anwendungen erhalten die Anzahl der verfügbaren Zeilen, wenn [**lineinitializeex**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="77c9c-106">**TAPI 2.x:** Applications get the number of available lines when [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) returns.</span></span> <span data-ttu-id="77c9c-107">Anschließend können Sie [**linegetdevcaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) für jede Zeile, [**linegetaddresscaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) für jede Adresse und [**lineOpen**](/windows/win32/api/tapi/nf-tapi-lineopen) für jede zu verwendende Zeile ausführen.</span><span class="sxs-lookup"><span data-stu-id="77c9c-107">They can then perform [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) on each line, [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) for each address, and [**lineOpen**](/windows/win32/api/tapi/nf-tapi-lineopen) for each line that will be used.</span></span>

<span data-ttu-id="77c9c-108">**TAPI 3. x:** Anwendungen verwenden die Adressen [**ittapi:: enumerateadressen**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses) oder [**ittapi: \_ : Get**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses) , um die verfügbaren Adressen zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="77c9c-108">**TAPI 3.x:** Applications use [**ITTAPI::EnumerateAddresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses) or [**ITTAPI::get\_Addresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses) to discover the addresses available.</span></span> <span data-ttu-id="77c9c-109">[**Itmediasupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport) und [**itaddress-Funktionen**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) stellen Informationen zu Kommunikationstypen bereit, die für jede Adresse möglich sind.</span><span class="sxs-lookup"><span data-stu-id="77c9c-109">[**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport) and [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) supply information on communication types possible for each address.</span></span> <span data-ttu-id="77c9c-110">Durch die Implementierung durch den Dienstanbieter erhält [**itterminalsupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) eine Anwendung Zugriff auf zusätzliche Informationen und Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="77c9c-110">If implemented by the service provider, [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) gives an application access to additional information and controls.</span></span>

 

 
