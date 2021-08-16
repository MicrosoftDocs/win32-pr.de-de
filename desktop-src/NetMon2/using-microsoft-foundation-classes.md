---
description: Aufgrund des Speicherbedarfs statisch verknüpfter DLLs sollten Sie vermeiden, Microsoft Foundation Classes (MFCs) zum Schreiben eines Experten zu verwenden.
ms.assetid: 634852fd-d0e0-42a7-90af-e93cc0e4ac84
title: Verwenden von Microsoft Foundation Classes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bec1b01260d3fd7d1e7058c9fff8aa3cc32390b3f2f6cc715c91563a871fbf20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118362929"
---
# <a name="using-microsoft-foundation-classes"></a>Verwenden von Microsoft Foundation Classes

Aufgrund des Speicherbedarfs statisch verknüpfter DLLs sollten Sie vermeiden, Microsoft Foundation Classes (MFCs) zum Schreiben eines Experten zu verwenden. Wenn Sie jedoch den MFC verwenden, stellen Sie den Zugriff auf eine der MFC-DLL-Ressourcen sicher, indem Sie den folgenden Code sofort nach dem Eintrag einschließen:

``` syntax
#ifdef _AFXDLL
      AFX_MANAGE_STATE(AfxGetStaticModuleState());
#endif
```

 

 



