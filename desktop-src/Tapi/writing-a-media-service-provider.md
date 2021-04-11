---
description: Ein Medien Dienstanbieter muss eine minimale Teilmenge von MSPi-Schnittstellen implementieren, itmspaddress itterminalsupport itstreamcontrol und itstream.
ms.assetid: 59560bdf-953e-48e8-b565-46c3e0123c7e
title: Schreiben eines Media Service-Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782dddb9a87725bde7c104d459b71204a04de018
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351168"
---
# <a name="writing-a-media-service-provider"></a><span data-ttu-id="eb249-103">Schreiben eines Media Service-Anbieters</span><span class="sxs-lookup"><span data-stu-id="eb249-103">Writing a Media Service Provider</span></span>

<span data-ttu-id="eb249-104">Ein Medien Dienstanbieter muss eine minimale Teilmenge von MSPi-Schnittstellen implementieren: [**itmspaddress**](/windows/desktop/api/msp/nn-msp-itmspaddress), [**itterminalsupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport), [**itstreamcontrol**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)und [**itstream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).</span><span class="sxs-lookup"><span data-stu-id="eb249-104">A media service provider must implement a minimum subset of MSPI interfaces: [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress), [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport), [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol), and [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).</span></span> <span data-ttu-id="eb249-105">Die Unterstützung von Substreams ist optional.</span><span class="sxs-lookup"><span data-stu-id="eb249-105">SubStream support is optional.</span></span> <span data-ttu-id="eb249-106">Darüber hinaus kann ein bestimmtes MSP zusätzliche Methoden implementieren, z. b. Steuerelemente, die für spezialisierte Hardware erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="eb249-106">In addition, a given MSP may implement additional methods, such as controls required for specialized hardware.</span></span>

<span data-ttu-id="eb249-107">Die folgenden Material Dokumente:</span><span class="sxs-lookup"><span data-stu-id="eb249-107">The following material documents:</span></span>

-   <span data-ttu-id="eb249-108">Die [TAPI 3-MSP-Basisklassen](tapi-3-msp-base-classes.md), bei denen es sich um eine Reihe von C++-Klassen handelt, die die Aufgabe der Einrichtung eines DirectShow-basierten MSP vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="eb249-108">The [TAPI 3 MSP Base Classes](tapi-3-msp-base-classes.md), which are a set of C++ classes designed to simplify the task of building a DirectShow-based MSP.</span></span> <span data-ttu-id="eb249-109">Die Basisklassen implementieren alle MSPi-Schnittstellen auf generische Weise.</span><span class="sxs-lookup"><span data-stu-id="eb249-109">The base classes implement all the MSPI interfaces in a generic manner.</span></span> <span data-ttu-id="eb249-110">Verschiedene MSPs können MSP-spezifische Funktionen überschreiben und ihre eigenen Implementierungen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="eb249-110">Different MSPs can override MSP-specific functions and provide their own implementations.</span></span>
-   <span data-ttu-id="eb249-111">Der [TAPI 3-Terminal-Manager](tapi-3-terminal-manager.md), der Schnittstellen und Methoden bereitstellt, die von einem MSP zum Steuern von Terminals verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb249-111">The [TAPI 3 Terminal Manager](tapi-3-terminal-manager.md), which provides interfaces and methods used by an MSP to control terminals.</span></span>
-   <span data-ttu-id="eb249-112">[Austauschbare Terminals](writing-a-pluggable-terminal.md), mit denen eine Anwendung anstelle eines MSP Terminals erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="eb249-112">[Pluggable Terminals](writing-a-pluggable-terminal.md), which allow an application instead of an MSP to create terminals.</span></span> <span data-ttu-id="eb249-113">Entwickler, die bereits Erfahrung mit dem Schreiben von Dienstanbietern haben, sind die Haupt Ersteller von austauschbaren Terminals.</span><span class="sxs-lookup"><span data-stu-id="eb249-113">Developers who are already experienced at writing service providers will be the primary creators of pluggable terminals.</span></span> <span data-ttu-id="eb249-114">Die für diese Version implementierte anfängliche Version richtet sich an Konferenz Server Anwendungen, die nicht-Windows 2000-oder nicht-Multicast-Clients zu TAPI 3 Multi-Party-SDP/IP-Multicast Konferenzen hinzufügen müssen.</span><span class="sxs-lookup"><span data-stu-id="eb249-114">The initial version implemented for this release is aimed at conferencing server applications that need to add non-Windows 2000 or non-multicast clients to TAPI 3 multi-party SDP/IP multicast conferences.</span></span>

 

 
