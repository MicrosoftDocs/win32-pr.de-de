---
title: Richtlinien für das Schreiben von EAP-DLLs
description: Sie können EAP-DLLs oder-Plug-ins schreiben, um die Leistung in verschiedenen Szenarien zu optimieren.
ms.assetid: 79b9bc54-6eb0-4e01-822e-af83fc475ec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cdc2d437df61811e6fb24b3a9b4ff406ced4905
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "106340677"
---
# <a name="guidelines-for-writing-eap-dlls"></a><span data-ttu-id="b6800-103">Richtlinien für das Schreiben von EAP-DLLs</span><span class="sxs-lookup"><span data-stu-id="b6800-103">Guidelines for Writing EAP DLLs</span></span>

<span data-ttu-id="b6800-104">Sie können EAP-DLLs oder-Plug-ins schreiben, um die Leistung in verschiedenen Szenarien zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="b6800-104">EAP DLLs or Plug-ins can be written to optimize their performance in different scenarios.</span></span>

## <a name="general-guidelines"></a><span data-ttu-id="b6800-105">Allgemeine Richtlinien</span><span class="sxs-lookup"><span data-stu-id="b6800-105">General Guidelines</span></span>

-   <span data-ttu-id="b6800-106">Um eine verschlüsselte Verbindung zu erstellen, müssen die EAP-Plug-ins Verschlüsselungsschlüssel generieren und über die herstellerspezifischen RADIUS-Attribute von Microsoft, MS-MPPE-Send-Keys und MS-MPPE-Recv-Keys, zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b6800-106">In order to create an encrypted connection, EAP plug-ins must generate encryption keys and return them through the Microsoft vendor-specific RADIUS Attributes MS-MPPE-Send-Keys and MS-MPPE-Recv-Keys.</span></span> <span data-ttu-id="b6800-107">Weitere Informationen finden Sie im Abschnitt "Hinweise" in der [**PPP- \_ EAP- \_ Ausgabe**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) .</span><span class="sxs-lookup"><span data-stu-id="b6800-107">See the Remarks section in [**PPP\_EAP\_OUTPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) for more information.</span></span>

## <a name="wireless-guidelines"></a><span data-ttu-id="b6800-108">Drahtlos Richtlinien</span><span class="sxs-lookup"><span data-stu-id="b6800-108">Wireless Guidelines</span></span>

<span data-ttu-id="b6800-109">Im folgenden finden Sie Richtlinien und Empfehlungen zum Schreiben eines EAP-Plug-ins, das das Authentifizieren von Computern in drahtlosen Szenarios (802.1 x) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b6800-109">The following are guidelines and recommendations for writing an EAP Plug-in that supports authenticating machines in wireless (802.1X) scenarios.</span></span> <span data-ttu-id="b6800-110">Dieser Abschnitt gilt nicht für VPN-und einwählszenarien.</span><span class="sxs-lookup"><span data-stu-id="b6800-110">This section does not apply to VPN and Dial-up scenarios.</span></span>

-   <span data-ttu-id="b6800-111">Damit die Ausführung von unbeaufsichtigten Systemen nicht blockiert wird, dürfen keine Benutzeroberflächen Aufrufe von EAP-Plug-Ins ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b6800-111">In order not to block unattended systems' execution, EAP plug-ins must not make any user interface calls.</span></span>
-   <span data-ttu-id="b6800-112">Die EAP-Plug-in-Implementierung des Computers zur Computer Authentifizierung muss so schnell wie möglich ausgeführt werden, sodass der Start des Betriebssystems nicht beeinträchtigt wird.</span><span class="sxs-lookup"><span data-stu-id="b6800-112">The EAP Plug-in implementation of the machine authentication step must complete as quickly as possible so it does not hinder operating system startup.</span></span>
    > [!Note]  
    > <span data-ttu-id="b6800-113">Wenn das EAP-Protokoll keine Computer Authentifizierung unterstützt, muss es das computerauthentifizierungsflag, die **RAS- \_ EAP- \_ Flag- \_ Computer \_** Authentifizierung, die im Feld **fFlags** in der [**PPP- \_ EAP- \_ Eingabe**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input)verwendet wird, überprüfen und einen Fehler zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b6800-113">If your EAP protocol does not support machine authentication, it must check for the machine authentication flag, **RAS\_EAP\_FLAG\_MACHINE\_AUTH** used in the **fFlags** field in [**PPP\_EAP\_INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input), and return an error.</span></span>

     

 

 




