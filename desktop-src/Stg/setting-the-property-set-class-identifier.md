---
title: Festlegen des Eigenschafts Satz-Klassen Bezeichners
description: Die IPropertyStorage-setClass-Methode legt sowohl die CLSID des Speicher Objekts als auch den Wert des Klassentags fest, der im com-Eigenschaften Satz gespeichert ist. Dies tritt auf, wenn für einen nicht einfachen Eigenschafts Speicher aufgerufen wird, der in einem strukturierten Speicher Objekt gespeichert ist.
ms.assetid: 3f542a66-5e04-43c1-a386-7d709c615972
keywords:
- Festlegen des Eigenschafts Satz-Klassen Bezeichners
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9ec6e038ef6bc5f4f12228581946a4051c532b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037403"
---
# <a name="setting-the-property-set-class-identifier"></a><span data-ttu-id="40fbd-105">Festlegen des Eigenschafts Satz-Klassen Bezeichners</span><span class="sxs-lookup"><span data-stu-id="40fbd-105">Setting the Property Set Class Identifier</span></span>

<span data-ttu-id="40fbd-106">Die [**IPropertyStorage:: setClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass) -Methode legt sowohl die CLSID des Speicher Objekts als auch den Wert des Klassentags fest, der im com-Eigenschaften Satz gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="40fbd-106">The [**IPropertyStorage::SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass) method sets both the CLSID of the storage object and the class tag value stored in the COM property set.</span></span> <span data-ttu-id="40fbd-107">Dies tritt auf, wenn für einen nicht einfachen Eigenschafts Speicher aufgerufen wird, der in einem strukturierten Speicher Objekt gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="40fbd-107">This occurs when invoked on a nonsimple property storage stored in a structured storage object.</span></span>

<span data-ttu-id="40fbd-108">Dies bietet Konsistenz und Einheitlichkeit, wodurch eine bessere Interaktion mit einigen Tools erzielt wird.</span><span class="sxs-lookup"><span data-stu-id="40fbd-108">This provides consistency and uniformity which creates better interaction with some tools.</span></span> <span data-ttu-id="40fbd-109">Ein Eigenschaften Speicher Objekt ist nicht einfach, wenn es durch Aufrufen von [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) mit dem **\_ nicht einfachen Flag propsetflag** erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="40fbd-109">A property storage object is nonsimple if it is created by calling [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) with the **PROPSETFLAG\_NONSIMPLE** flag set.</span></span>

<span data-ttu-id="40fbd-110">Die CLSID des Speicher Objekts wird mit einem Aufrufen von [**IStorage:: setClass**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass)festgelegt.</span><span class="sxs-lookup"><span data-stu-id="40fbd-110">The CLSID of the storage object is set with a call to [**IStorage::SetClass**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass).</span></span>

 

 




