---
description: Quality of Service (QoS) wird in Windows über verschiedene QoS-Komponenten implementiert, die unter Windows Server 2003, Windows XP und Windows 2000 unterstützt werden.
ms.assetid: e55b085f-6f72-4aa4-a8b0-b7609b9010dc
title: Quality of Service in Windows Sockets 2 SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e87d37f2e30e0a4fb296fc340353e2f4d85b5b8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356897"
---
# <a name="quality-of-service-in-the-windows-sockets-2-spi"></a><span data-ttu-id="07b32-103">Quality of Service in Windows Sockets 2 SPI</span><span class="sxs-lookup"><span data-stu-id="07b32-103">Quality of Service in the Windows Sockets 2 SPI</span></span>

<span data-ttu-id="07b32-104">Quality of Service (QoS) wird in Windows über verschiedene QoS-Komponenten implementiert, die unter Windows Server 2003, Windows XP und Windows 2000 unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="07b32-104">Quality of Service (QoS) is implemented in Windows through various QoS components supported on Windows Server 2003, Windows XP, and Windows 2000.</span></span> <span data-ttu-id="07b32-105">Eine ausführliche Erläuterung der QoS und der zugehörigen Komponenten finden Sie in einem Abschnitt, der sich auf Quality of Service im Microsoft Windows Software Development Kit (SDK) befindet.</span><span class="sxs-lookup"><span data-stu-id="07b32-105">A detailed explanation of QoS and its components is located in a section dedicated to Quality of Service, located in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="07b32-106">Jede QoS-Komponente und die Rolle, die in der QoS-Implementierung abgespielt wird, werden in diesem QoS-Abschnitt erläutert, wobei zusätzliche Anleitungen für die Implementierung von QoS-fähigen Anwendungen und Diensten bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="07b32-106">Each QoS component, and the role it plays in the QoS implementation, is explained in this QoS section, with additional guidance provided for the implementation of QoS-enabled applications and services.</span></span> <span data-ttu-id="07b32-107">Ausführlichere Informationen finden Sie im Abschnitt [Quality of Service (QoS)](/previous-versions/windows/desktop/qos/qos-start-page) des Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="07b32-107">Please see the [Quality of Service (QoS)](/previous-versions/windows/desktop/qos/qos-start-page) section of the Windows SDK for more detailed information.</span></span>

<span data-ttu-id="07b32-108">In diesem Abschnitt werden die Quality of Service für Winsock-Entwickler verfügbaren Funktionen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="07b32-108">This section describes Quality of Service capabilities available to Winsock developers.</span></span> <span data-ttu-id="07b32-109">In der folgenden Liste werden die Themen in diesem Abschnitt beschrieben:</span><span class="sxs-lookup"><span data-stu-id="07b32-109">The following list describes the topics in this section:</span></span>

-   [<span data-ttu-id="07b32-110">Verwendungs Modell</span><span class="sxs-lookup"><span data-stu-id="07b32-110">Usage Model</span></span>](usage-model-2.md)
-   [<span data-ttu-id="07b32-111">QoS-Updates</span><span class="sxs-lookup"><span data-stu-id="07b32-111">QoS Updates</span></span>](qos-updates-2.md)
-   [<span data-ttu-id="07b32-112">Standardwerte in der SPI</span><span class="sxs-lookup"><span data-stu-id="07b32-112">Default Values in the SPI</span></span>](default-values-in-the-spi-2.md)
-   [<span data-ttu-id="07b32-113">QoS-Vorlagen in der SPI</span><span class="sxs-lookup"><span data-stu-id="07b32-113">QoS Templates in the SPI</span></span>](qos-templates-in-the-spi-2.md)

## <a name="related-topics"></a><span data-ttu-id="07b32-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="07b32-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07b32-115">Quality of Service (QoS, Dienstqualität)</span><span class="sxs-lookup"><span data-stu-id="07b32-115">Quality of Service (QoS)</span></span>](/previous-versions/windows/desktop/qos/qos-start-page)
</dt> <dt>

<span data-ttu-id="07b32-116">[Was ist QoS?](/previous-versions/windows/it-pro/windows-server-2003/cc757120(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="07b32-116">[What Is QoS?](/previous-versions/windows/it-pro/windows-server-2003/cc757120(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="07b32-117">Winsock ATM-QoS-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="07b32-117">Winsock ATM QoS Extension</span></span>](winsock-atm-qos-extension.md)
</dt> <dt>

[<span data-ttu-id="07b32-118">**Winsock IOCTLs**</span><span class="sxs-lookup"><span data-stu-id="07b32-118">**Winsock IOCTLs**</span></span>](winsock-ioctls.md)
</dt> </dl>

 

 
