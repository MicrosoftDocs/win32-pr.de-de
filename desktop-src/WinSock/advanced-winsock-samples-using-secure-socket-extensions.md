---
description: Erweiterte Winsock-Beispiele mit Secure Socket Extensions
ms.assetid: 9c429363-f9bb-4394-89be-f87507f5cbdd
title: Erweiterte Winsock-Beispiele mit Secure Socket Extensions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6701809ad97c7d39acf1f0eae646e7555e5c967f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958931"
---
# <a name="advanced-winsock-samples-using-secure-socket-extensions"></a><span data-ttu-id="477ed-103">Erweiterte Winsock-Beispiele mit Secure Socket Extensions</span><span class="sxs-lookup"><span data-stu-id="477ed-103">Advanced Winsock Samples Using Secure Socket Extensions</span></span>

## <a name="secure-tcp-client-and-server-sample"></a><span data-ttu-id="477ed-104">Beispiel für sicheres TCP-Client und-Server</span><span class="sxs-lookup"><span data-stu-id="477ed-104">Secure TCP Client and Server Sample</span></span>

<span data-ttu-id="477ed-105">Im Microsoft Windows Software Development Kit (SDK) finden Sie ein erweitertes Winsock-Beispiel, das die Verwendung von Secure Socket Extensions veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="477ed-105">A more advanced Winsock sample that demonstrates the use of secure socket extensions is included with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="477ed-106">Das Beispiel enthält einen TCP-Client und-Server, die sicher mithilfe der Winsock-und Secure Socket-Erweiterungen eine Verbindung herstellen.</span><span class="sxs-lookup"><span data-stu-id="477ed-106">The sample includes a TCP client and server that connect securely using the Winsock and the secure socket extensions.</span></span>

<span data-ttu-id="477ed-107">Der Winsock-Beispiel Quellcode wird standardmäßig im folgenden Verzeichnis installiert:</span><span class="sxs-lookup"><span data-stu-id="477ed-107">By default, the Winsock sample source code is installed in the following directory:</span></span>

<span data-ttu-id="477ed-108">*C: \\ Programmdateien \\ Microsoft sdert \\ Windows \\ v 6.0 \\ Beispiele \\ netds \\ Winsock*</span><span class="sxs-lookup"><span data-stu-id="477ed-108">*C:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Samples\\NetDs\\winsock*</span></span>

<span data-ttu-id="477ed-109">Ein Beispiel befindet sich im folgenden Ordner:</span><span class="sxs-lookup"><span data-stu-id="477ed-109">A sample is located under the following folder:</span></span>

<span data-ttu-id="477ed-110">*Securesocket*</span><span class="sxs-lookup"><span data-stu-id="477ed-110">*securesocket*</span></span>

<span data-ttu-id="477ed-111">Der Beispielcode ist wie unten beschrieben in separate Verzeichnisse unterteilt:</span><span class="sxs-lookup"><span data-stu-id="477ed-111">The sample code is split into separate directories as described below:</span></span>

-   <span data-ttu-id="477ed-112">stcpclient: der Ordner, der den sicheren TCP-Client Code enthält.</span><span class="sxs-lookup"><span data-stu-id="477ed-112">stcpclient - the folder that contains the secure TCP client code.</span></span>
-   <span data-ttu-id="477ed-113">stcpcommon: der Ordner, der allgemeinen Bibliotheks Code enthält, der vom sicheren TCP-Client und-Server gemeinsam genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="477ed-113">stcpcommon - the folder that contains common library code that is shared between the secure TCP client and server.</span></span>
-   <span data-ttu-id="477ed-114">stcpserver: der Ordner, der den sicheren TCP-Servercode enthält.</span><span class="sxs-lookup"><span data-stu-id="477ed-114">stcpserver - the folder that contains the secure TCP server code.</span></span>

<span data-ttu-id="477ed-115">Beachten Sie, dass die Beispiele auf zwei verschiedenen Computern mit Windows Vista oder höher ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="477ed-115">It should be noted that the samples are meant to be run on two different computers running Windows Vista or later.</span></span> <span data-ttu-id="477ed-116">Zusätzlich müssen die IPSec-Anmelde Informationen auf beiden Computern bereitgestellt werden, damit die Verbindung erfolgreich hergestellt werden kann, da im Beispiel IPSec zum Sichern des Datenverkehrs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="477ed-116">Additionally, IPsec credentials must be provisioned on both the computers for the connection to succeed, because the sample uses IPsec for securing its traffic.</span></span> <span data-ttu-id="477ed-117">Weitere Informationen zum Einrichten von IPSec-Anmelde Informationen finden Sie in der Dokumentation zur [IPSec-Konfiguration](/windows/desktop/FWP/ipsec-configuration) .</span><span class="sxs-lookup"><span data-stu-id="477ed-117">Please refer to the documentation on [IPsec Configuration](/windows/desktop/FWP/ipsec-configuration) for more information on setting up IPsec credentials.</span></span>

<span data-ttu-id="477ed-118">Beim Erstellen des Beispiels werden zwei ausführbare Dateien generiert:</span><span class="sxs-lookup"><span data-stu-id="477ed-118">Building the sample will generate two executable files:</span></span>

<span data-ttu-id="477ed-119">*stcpclient.exe* und *stcpserver.exe*.</span><span class="sxs-lookup"><span data-stu-id="477ed-119">*stcpclient.exe* and *stcpserver.exe*.</span></span>

<span data-ttu-id="477ed-120">Kopieren Sie *stcpclient.exe* auf Computer a, und kopieren Sie *stcpserver.exe* auf Computer B. Starten Sie auf Computer B den TCP-Server, indem Sie den folgenden Befehl an einer Eingabeaufforderung ausführen:</span><span class="sxs-lookup"><span data-stu-id="477ed-120">Copy *stcpclient.exe* to computer A and copy *stcpserver.exe* to computer B. On computer B, start the TCP server by executing the following in a Command Prompt:</span></span>

<span data-ttu-id="477ed-121">**stcpserver.exe**</span><span class="sxs-lookup"><span data-stu-id="477ed-121">**stcpserver.exe**</span></span>

<span data-ttu-id="477ed-122">Führen Sie den folgenden Befehl aus, um weitere Verwendungs Optionen für den Server zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="477ed-122">Execute the following command for more usage options for the server:</span></span>

<span data-ttu-id="477ed-123">**stcpserver.exe/?**</span><span class="sxs-lookup"><span data-stu-id="477ed-123">**stcpserver.exe /?**</span></span>

<span data-ttu-id="477ed-124">Starten Sie dann auf Computer A den TCP-Client, indem Sie den folgenden Befehl an einer Eingabeaufforderung ausführen:</span><span class="sxs-lookup"><span data-stu-id="477ed-124">Then on computer A, start the TCP client by executing the following in a Command Prompt:</span></span>

<span data-ttu-id="477ed-125">**stcpclient.exe <voll qualifizierter DNS-Name-for-Machine-B->**</span><span class="sxs-lookup"><span data-stu-id="477ed-125">**stcpclient.exe <fully-qualified-DNS-name-for-machine-B>**</span></span>

<span data-ttu-id="477ed-126">An diesem Punkt sollte die Verbindung sicher hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="477ed-126">At this point the connection should get established securely.</span></span>

<span data-ttu-id="477ed-127">Führen Sie den folgenden Befehl aus, um weitere Verwendungs Optionen für den-Client zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="477ed-127">Execute the following command for more usage options for the client:</span></span>

<span data-ttu-id="477ed-128">**stcpclient.exe/?**</span><span class="sxs-lookup"><span data-stu-id="477ed-128">**stcpclient.exe /?**</span></span>

## <a name="related-topics"></a><span data-ttu-id="477ed-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="477ed-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="477ed-130">Informationen zur Windows-Filter Plattform</span><span class="sxs-lookup"><span data-stu-id="477ed-130">About Windows Filtering Platform</span></span>](/windows/desktop/FWP/about-windows-filtering-platform)
</dt> <dt>

[<span data-ttu-id="477ed-131">Durchsetzung der Anwendungsschicht (ALE)</span><span class="sxs-lookup"><span data-stu-id="477ed-131">Application Layer Enforcement (ALE)</span></span>](/windows/desktop/FWP/application-layer-enforcement--ale-)
</dt> <dt>

[<span data-ttu-id="477ed-132">IPSec-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="477ed-132">IPsec Configuration</span></span>](/windows/desktop/FWP/ipsec-configuration)
</dt> <dt>

[<span data-ttu-id="477ed-133">IPSec-Funktionen</span><span class="sxs-lookup"><span data-stu-id="477ed-133">IPsec Functions</span></span>](/windows/desktop/FWP/fwp-ipsec-functions)
</dt> <dt>

[<span data-ttu-id="477ed-134">Verwenden von Secure Socket Extensions</span><span class="sxs-lookup"><span data-stu-id="477ed-134">Using Secure Socket Extensions</span></span>](using-secure-socket-extensions.md)
</dt> <dt>

[<span data-ttu-id="477ed-135">Security Support Provider Interface (SSPI)</span><span class="sxs-lookup"><span data-stu-id="477ed-135">Security Support Provider Interface (SSPI)</span></span>](/windows/desktop/Rpc/security-support-provider-interface-sspi-)
</dt> <dt>

[<span data-ttu-id="477ed-136">Windows-Filterplattform</span><span class="sxs-lookup"><span data-stu-id="477ed-136">Windows Filtering Platform</span></span>](/windows/desktop/FWP/windows-filtering-platform-start-page)
</dt> <dt>

[<span data-ttu-id="477ed-137">API-Funktionen der Windows-Filter Plattform</span><span class="sxs-lookup"><span data-stu-id="477ed-137">Windows Filtering Platform API Functions</span></span>](/windows/desktop/FWP/fwp-functions)
</dt> <dt>

[<span data-ttu-id="477ed-138">Winsock Secure Socket Extensions</span><span class="sxs-lookup"><span data-stu-id="477ed-138">Winsock Secure Socket Extensions</span></span>](winsock-secure-socket-extensions.md)
</dt> </dl>

 

 
