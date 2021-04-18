---
title: Active Directory von Betriebs Attributen
description: Betriebs Attribute sind Eigenschaften, die in gespeichert und für administrative Zwecke vom Verzeichnis verwendet werden.
ms.assetid: 07453dc0-747e-4b34-946e-1adb90ea532c
ms.tgt_platform: multiple
keywords:
- Attribute ADSI, Operational Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac95536564f735e8e1bd8c5c28a49ce71a2640a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104387974"
---
# <a name="active-directory-operational-attributes"></a><span data-ttu-id="7acde-104">Active Directory von Betriebs Attributen</span><span class="sxs-lookup"><span data-stu-id="7acde-104">Active Directory Operational Attributes</span></span>

<span data-ttu-id="7acde-105">Betriebs Attribute sind Eigenschaften, die in gespeichert und für administrative Zwecke vom Verzeichnis verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7acde-105">Operational attributes are properties that are stored in and used by the directory for administrative purposes.</span></span> <span data-ttu-id="7acde-106">Beispielsweise können Sie ein Betriebs Attribut verwalten, um das Datum und die Uhrzeit der Änderung eines anderen Attributs zu protokollieren.</span><span class="sxs-lookup"><span data-stu-id="7acde-106">For example, you might maintain an operational attribute to log the date and time when another attribute is modified.</span></span> <span data-ttu-id="7acde-107">Betriebs Attribute müssen explizit mit einem Aufrufen von [**GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7acde-107">Operational Attributes must be explicitly retrieved with a call to [**GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex).</span></span>

 

 




