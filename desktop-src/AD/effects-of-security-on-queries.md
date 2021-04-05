---
title: Auswirkungen der Sicherheit bei der Suche
description: Sicherheit ist ein impliziter Filter beim Durchführen von Such Vorgängen, beim Auflisten von Containern oder beim Lesen von Eigenschaften.
ms.assetid: 4a027069-8c3d-4a95-a04b-c9c59200a9ed
ms.tgt_platform: multiple
keywords:
- Auswirkungen der Sicherheit beim Suchen Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26feee840c0668b2ea9412932a27927bb1c00012
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707698"
---
# <a name="effects-of-security-on-searching"></a><span data-ttu-id="8dd69-104">Auswirkungen der Sicherheit bei der Suche</span><span class="sxs-lookup"><span data-stu-id="8dd69-104">Effects of Security on Searching</span></span>

<span data-ttu-id="8dd69-105">Sicherheit ist ein impliziter Filter beim Durchführen von Such Vorgängen, beim Auflisten von Containern oder beim Lesen von Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8dd69-105">Security is an implicit filter when performing searches, enumerating containers, or reading properties.</span></span>

<span data-ttu-id="8dd69-106">ADSI kann keine \_ solche \_ Eigenschaft oder keine \_ derartigen \_ Objekt Fehler zurückgeben, auch wenn das Objekt vorhanden ist, wenn Sie keinen Zugriff auf die Lese Attribute für das Objekt haben.</span><span class="sxs-lookup"><span data-stu-id="8dd69-106">ADSI can return NO\_SUCH\_PROPERTY or NO\_SUCH\_OBJECT errors even when the object exists if you do not have access to read attributes on the object.</span></span>

<span data-ttu-id="8dd69-107">Beispielsweise kann ein Aufrufer in der Lage sein, die untergeordneten Objekte in einem Container aufzulisten, da der Aufrufer \_ überlisten Inhalts Rechte für den Container verfügt.</span><span class="sxs-lookup"><span data-stu-id="8dd69-107">For example, a caller may be able to enumerate the child objects in a container because the caller has LIST\_CONTENTS rights on the container.</span></span> <span data-ttu-id="8dd69-108">Der gleiche Aufrufer ist jedoch möglicherweise nicht in der Lage, auf die aufgelisteten Objekte zuzugreifen, wenn der Aufrufer keinen Lesezugriff auf die untergeordneten Objekte hat.</span><span class="sxs-lookup"><span data-stu-id="8dd69-108">But the same caller may not be able to access the enumerated objects if the caller does not have read access to the child objects.</span></span> <span data-ttu-id="8dd69-109">In diesem Fall gibt eine Abfrage für ein untergeordnetes Objekt möglicherweise kein \_ solches Objekt zurück, \_ auch wenn der Aufrufer das Objekt erfolgreich aufzählt.</span><span class="sxs-lookup"><span data-stu-id="8dd69-109">In this case, a query for a child object may return NO\_SUCH\_OBJECT even though the caller successfully enumerated the object.</span></span>

<span data-ttu-id="8dd69-110">Wenn der Aufrufer nicht über ausreichende Rechte verfügt, können die folgenden Rückgabecodes zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="8dd69-110">If the caller does not have sufficient rights, the following return codes may be returned:</span></span>

<span data-ttu-id="8dd69-111">E \_ ADS \_ ungültiges \_ Domänen \_ Objekt</span><span class="sxs-lookup"><span data-stu-id="8dd69-111">E\_ADS\_INVALID\_DOMAIN\_OBJECT</span></span>

<span data-ttu-id="8dd69-112">E \_ ADS- \_ Eigenschaft \_ nicht \_ unterstützt</span><span class="sxs-lookup"><span data-stu-id="8dd69-112">E\_ADS\_PROPERTY\_NOT\_SUPPORTED</span></span>

<span data-ttu-id="8dd69-113">E \_ ADS- \_ Eigenschaft \_ nicht \_ gefunden</span><span class="sxs-lookup"><span data-stu-id="8dd69-113">E\_ADS\_PROPERTY\_NOT\_FOUND</span></span>

 

 




