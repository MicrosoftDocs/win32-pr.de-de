---
title: Schnittstelle (com)
description: Ein optionaler Eintrag, der alle von der zugeordneten-Klasse unterstützten Schnittstellen-IDs (IIDs) angibt.
ms.assetid: 212a6500-14ce-4a9b-9e6a-38d83a5630c8
keywords:
- COM-Registrierungsschlüssel com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990c06285d60067c9a26faffabffc70cbdd283d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106340754"
---
# <a name="interface-com"></a><span data-ttu-id="1a4a5-104">Schnittstelle (com)</span><span class="sxs-lookup"><span data-stu-id="1a4a5-104">Interface (COM)</span></span>

<span data-ttu-id="1a4a5-105">Ein optionaler Eintrag, der alle von der zugeordneten-Klasse unterstützten Schnittstellen-IDs (IIDs) angibt.</span><span class="sxs-lookup"><span data-stu-id="1a4a5-105">An optional entry that specifies all interface IDs (IIDs) supported by the associated class.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="1a4a5-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="1a4a5-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Interface
         {IID1} = name1
         {IID2} = name2
         ...
```

## <a name="remarks"></a><span data-ttu-id="1a4a5-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1a4a5-107">Remarks</span></span>

<span data-ttu-id="1a4a5-108">Wenn ein Schnittstellen Name nicht in dieser Liste vorhanden ist, kann die Schnittstelle nie von einer Instanz dieser Klasse unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="1a4a5-108">If an interface name is not present in this list, the interface can never be supported by an instance of this class.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a4a5-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1a4a5-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a4a5-110">Schnittstellenschlüssel</span><span class="sxs-lookup"><span data-stu-id="1a4a5-110">Interface Key</span></span>](interface-key.md)
</dt> </dl>

 

 




