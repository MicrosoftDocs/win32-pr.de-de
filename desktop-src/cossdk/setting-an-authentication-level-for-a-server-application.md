---
description: Wenn Sie eine Authentifizierungs Ebene für eine Anwendung festlegen, legen Sie fest, welcher Grad an Authentifizierung durchgeführt wird, wenn Clients die Anwendung anrufen.
ms.assetid: a59935de-6b8f-4c0a-8479-e30bc0509698
title: Festlegen einer Authentifizierungs Ebene für eine Server Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83450b3f8d1939d08cc3d16a21f438c8da6f8fc1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345622"
---
# <a name="setting-an-authentication-level-for-a-server-application"></a><span data-ttu-id="4034b-103">Festlegen einer Authentifizierungs Ebene für eine Server Anwendung</span><span class="sxs-lookup"><span data-stu-id="4034b-103">Setting an Authentication Level for a Server Application</span></span>

<span data-ttu-id="4034b-104">Wenn Sie eine Authentifizierungs Ebene für eine Anwendung festlegen, legen Sie fest, welcher Grad an Authentifizierung durchgeführt wird, wenn Clients die Anwendung anrufen.</span><span class="sxs-lookup"><span data-stu-id="4034b-104">When you set an authentication level for an application, you determine what degree of authentication is performed when clients call into the application.</span></span> <span data-ttu-id="4034b-105">Höhere Authentifizierungs Ebenen sorgen für eine höhere Sicherheit und Datenintegrität, auch wenn dies in der Regel zu Leistungseinbußen führen kann.</span><span class="sxs-lookup"><span data-stu-id="4034b-105">Higher authentication levels provide greater security and data integrity, although usually with some performance degradation.</span></span> <span data-ttu-id="4034b-106">Weitere Informationen finden Sie unter [Client Authentifizierung](client-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="4034b-106">For more information, see [Client Authentication](client-authentication.md).</span></span>

<span data-ttu-id="4034b-107">**So wählen Sie eine Authentifizierungs Ebene für eine Serveranwendung aus**</span><span class="sxs-lookup"><span data-stu-id="4034b-107">**To select an authentication level for a server application**</span></span>

1.  <span data-ttu-id="4034b-108">Klicken Sie mit der rechten Maustaste auf die COM+-Anwendung, für die Sie die Authentifizierung festlegen, und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="4034b-108">Right-click the COM+ application for which you are setting authentication, and then click **Properties**.</span></span>

2.  <span data-ttu-id="4034b-109">Klicken Sie im Dialogfeld Anwendungseigenschaften auf die Registerkarte **Sicherheit** .</span><span class="sxs-lookup"><span data-stu-id="4034b-109">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="4034b-110">Wählen Sie im Feld **Authentifizierungs Ebene für Anrufe** die entsprechende Ebene aus.</span><span class="sxs-lookup"><span data-stu-id="4034b-110">In the **Authentication level for calls** box, select the appropriate level.</span></span> <span data-ttu-id="4034b-111">Die folgenden Ebenen sind von der niedrigsten zur höchsten Sicherheit geordnet:</span><span class="sxs-lookup"><span data-stu-id="4034b-111">The levels are as follows, ordered from lowest to highest security:</span></span>

    -   <span data-ttu-id="4034b-112">**Keine**.</span><span class="sxs-lookup"><span data-stu-id="4034b-112">**None**.</span></span> <span data-ttu-id="4034b-113">Es erfolgt keine Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="4034b-113">No authentication occurs.</span></span>
    -   <span data-ttu-id="4034b-114">**Verbinden** Sie sich.</span><span class="sxs-lookup"><span data-stu-id="4034b-114">**Connect**.</span></span> <span data-ttu-id="4034b-115">Authentifiziert Anmeldeinformationen nur dann, wenn die Verbindung hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="4034b-115">Authenticates credentials only when the connection is made.</span></span>
    -   <span data-ttu-id="4034b-116">**Aufgerufen** wird.</span><span class="sxs-lookup"><span data-stu-id="4034b-116">**Call**.</span></span> <span data-ttu-id="4034b-117">Authentifiziert am Anfang jedes Aufrufs die Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="4034b-117">Authenticates credentials at the beginning of every call.</span></span>
    -   <span data-ttu-id="4034b-118">**Paket**.</span><span class="sxs-lookup"><span data-stu-id="4034b-118">**Packet**.</span></span> <span data-ttu-id="4034b-119">Authentifiziert Anmeldeinformationen und überprüft, ob alle Aufrufdaten empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="4034b-119">Authenticates credentials and verifies that all call data is received.</span></span> <span data-ttu-id="4034b-120">Dies ist die Standardeinstellung für com+-Server Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="4034b-120">This is the default setting for COM+ server applications.</span></span>
    -   <span data-ttu-id="4034b-121">**Paketintegrität**.</span><span class="sxs-lookup"><span data-stu-id="4034b-121">**Packet Integrity**.</span></span> <span data-ttu-id="4034b-122">Authentifiziert Anmeldeinformationen und stellt sicher, dass während der Übertragung keine Aufrufdaten geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="4034b-122">Authenticates credentials and verifies that no call data has been modified in transit.</span></span>
    -   <span data-ttu-id="4034b-123">**Paket Datenschutz**.</span><span class="sxs-lookup"><span data-stu-id="4034b-123">**Packet Privacy**.</span></span> <span data-ttu-id="4034b-124">Authentifiziert Anmeldeinformationen und verschlüsselt das Paket, einschließlich der Daten sowie der Identität und Signatur des Absenders.</span><span class="sxs-lookup"><span data-stu-id="4034b-124">Authenticates credentials and encrypts the packet, including the data and the sender's identity and signature.</span></span>

4.  <span data-ttu-id="4034b-125">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4034b-125">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4034b-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4034b-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4034b-127">Aktivieren der Authentifizierung für eine Bibliotheks Anwendung</span><span class="sxs-lookup"><span data-stu-id="4034b-127">Enabling Authentication for a Library Application</span></span>](enabling-authentication-for-a-library-application.md)
</dt> </dl>

 

 



