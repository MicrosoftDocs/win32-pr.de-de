---
description: Windows-basierte Systeme können über mehrere Instanzen des Objekttyp "Treuhänder" verfügen.
ms.assetid: 13efedb5-ebb6-459b-8c4f-06774226278c
title: Der "Treuhänder Domain"-Objekttyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f0a4e6eca0790d877a9a23e4d83725d4e80798
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750857"
---
# <a name="the-trusteddomain-object-type"></a><span data-ttu-id="0ea13-103">Der "Treuhänder Domain"-Objekttyp</span><span class="sxs-lookup"><span data-stu-id="0ea13-103">The TrustedDomain Object Type</span></span>

<span data-ttu-id="0ea13-104">Windows-basierte Systeme können über mehrere Instanzen des Objekttyp " [**Treuhänder**](trusteddomain-object.md) " verfügen.</span><span class="sxs-lookup"><span data-stu-id="0ea13-104">Windows-based systems can have multiple instances of the [**TrustedDomain**](trusteddomain-object.md) object type.</span></span> <span data-ttu-id="0ea13-105">Die Objekte für die **Treuhänder Domäne** verfügen über zwei Felder, die in allen " **Treuhänder Domain** "-Objekten eindeutig sein müssen:</span><span class="sxs-lookup"><span data-stu-id="0ea13-105">**TrustedDomain** objects have two fields that must be unique among all **TrustedDomain** objects:</span></span>

-   <span data-ttu-id="0ea13-106">Der Name der [ **Treuhänder Domäne**](trusteddomain-object.md)</span><span class="sxs-lookup"><span data-stu-id="0ea13-106">The name of the [**TrustedDomain**](trusteddomain-object.md)</span></span>
-   <span data-ttu-id="0ea13-107">Die [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -ID (SID) der [**Treuhänder Domäne**](trusteddomain-object.md).</span><span class="sxs-lookup"><span data-stu-id="0ea13-107">The [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) of the [**TrustedDomain**](trusteddomain-object.md).</span></span>

<span data-ttu-id="0ea13-108">Der Versuch, ein neues " **Treuhänder Domain** "-Objekt mit einem Namen oder einer SID zu erstellen, die bereits von einem anderen " **Treuhänder Domain** "-Objekt verwendet wird, wird zurückgewiesen.</span><span class="sxs-lookup"><span data-stu-id="0ea13-108">An attempt to create a new **TrustedDomain** object with either a name or SID that is already in use by another **TrustedDomain** object will be rejected.</span></span>

 

 
