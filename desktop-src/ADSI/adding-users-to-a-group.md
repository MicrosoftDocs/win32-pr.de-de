---
title: Hinzufügen von Benutzern zu einer Gruppe
description: Joe von, der Unternehmens Administrator, fügt Julie Bankert nun der Verwaltungsgruppe hinzu. Zum Hinzufügen eines Objekts zu einer Gruppe verwenden Sie die IADsGroup. Add-Methode.
ms.assetid: 57a9f5b2-2e48-401d-8d3b-eceb711a1df9
ms.tgt_platform: multiple
keywords:
- Hinzufügen von Benutzern zu einer Gruppe ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ea0ac78c0175248cb12e0f47a94ae60e7f1d16c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309271"
---
# <a name="adding-users-to-a-group"></a><span data-ttu-id="6d339-105">Hinzufügen von Benutzern zu einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="6d339-105">Adding Users to a Group</span></span>

<span data-ttu-id="6d339-106">Joe von, der Unternehmens Administrator, fügt Julie Bankert nun der Verwaltungsgruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="6d339-106">Joe Worden, the enterprise administrator, will now add Julie Bankert to the Management group.</span></span> <span data-ttu-id="6d339-107">Zum Hinzufügen eines Objekts zu einer Gruppe verwenden Sie die [**IADsGroup. Add**](/windows/desktop/api/Iads/nf-iads-iadsgroup-add) -Methode.</span><span class="sxs-lookup"><span data-stu-id="6d339-107">To add an object to a group, use the [**IADsGroup.Add**](/windows/desktop/api/Iads/nf-iads-iadsgroup-add) method.</span></span>


```VB
Dim grp as IADsGroup

Set grp = GetObject("LDAP://CN=Management,OU=Sales,DC=Fabrikam,DC=COM") 
grp.Add ("LDAP://CN=Julie Bankert,OU=Sales,DC=Fabrikam,DC=COM")
```



## <a name="related-topics"></a><span data-ttu-id="6d339-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6d339-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d339-109">Erstellen einer neuen Gruppe</span><span class="sxs-lookup"><span data-stu-id="6d339-109">Creating a New Group</span></span>](creating-a-new-group.md)
</dt> </dl>

 

 




