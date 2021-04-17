---
title: Einschränkungen der gegenseitigen Authentifizierung mit Kerberos
description: Sowohl das Konto des Clients als auch das Konto des Diensts müssen sich in Domänen mit Windows 2000-oder gemischtem Modus befinden, da Kerberos-Dienste nicht in Domänen mit unterer Ebene verfügbar sind.
ms.assetid: 54685e88-b289-4db9-b4cb-f5c22a216a0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 290bd93050c9cb4c89052ce644b4c588f638f312
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470860"
---
# <a name="limitations-of-mutual-authentication-with-kerberos"></a><span data-ttu-id="b02ea-103">Einschränkungen der gegenseitigen Authentifizierung mit Kerberos</span><span class="sxs-lookup"><span data-stu-id="b02ea-103">Limitations of Mutual Authentication with Kerberos</span></span>

<span data-ttu-id="b02ea-104">Sowohl das Konto des Clients als auch das Konto des Diensts müssen sich in Domänen mit Windows 2000-oder gemischtem Modus befinden, da Kerberos-Dienste nicht in Domänen mit unterer Ebene verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="b02ea-104">Both the client's account and the service's account must be in Windows 2000 native or mixed-mode domains because Kerberos services are not available in downlevel domains.</span></span> <span data-ttu-id="b02ea-105">Außerdem müssen sich sowohl Client-als auch Dienst Konten in derselben Gesamtstruktur befinden, weil der Client-KDC den globalen Katalog verwendet, um nach dem Dienst Prinzipal Namen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="b02ea-105">In addition, both client and service accounts must be in the same forest because the client's KDC uses the global catalog to search for the service principal name.</span></span>

<span data-ttu-id="b02ea-106">Sowohl der Dienst als auch der Client müssen unter Windows 2000 ausgeführt werden. andernfalls schlägt die gegenseitige Authentifizierung mit Kerberos fehl, da frühere Versionen von Windows Kerberos nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b02ea-106">Both service and client must be running on Windows 2000, otherwise mutual authentication with Kerberos will fail because earlier versions of Windows do not support Kerberos.</span></span>

<span data-ttu-id="b02ea-107">Dienst Prinzipal Namen müssen den DNS-Namen des Host Servers enthalten, auf dem der Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b02ea-107">Service principal names must include the DNS name of the host server on which the service is running.</span></span> <span data-ttu-id="b02ea-108">Sie müssen den DNS-Namen verwenden.</span><span class="sxs-lookup"><span data-stu-id="b02ea-108">You must use the DNS name.</span></span>

 

 




