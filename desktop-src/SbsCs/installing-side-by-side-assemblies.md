---
description: Sie können assemblys nebeneinander als freigegebene Assemblys oder als private Assemblys installieren. Weitere Informationen finden Sie unter Installing Side-by-Side Assemblies as Private Assemblies (Installieren von nebenseitigen Assemblys als private Assemblys) und Installing Side-by-Side Assemblies as Shared Assemblies (Installieren von nebenseitigen Assemblys als freigegebene Assemblys).
ms.assetid: 36f271ff-be0c-4162-8e1c-86088ebddbcc
title: Installieren von nebenseitigen Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2124b490d64427e80b5beee53d1221cba4d5e59a23dc2d72c2da6833e14a98cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142133"
---
# <a name="installing-side-by-side-assemblies"></a>Installieren von nebenseitigen Assemblys

Sie können assemblys nebeneinander als [freigegebene Assemblys](/windows/desktop/Msi/shared-assemblies) oder als [private Assemblys](/windows/desktop/Msi/private-assemblies)installieren. Weitere Informationen finden Sie unter [Installing Side-by-Side Assemblies as Private Assemblies (Installieren von nebenseitigen Assemblys als private Assemblys)](installing-side-by-side-assemblies-as-private-assemblies.md) und [Installing Side-by-side Assemblies as Shared Assemblies (Installieren von nebenseitigen Assemblys als freigegebene Assemblys).](installing-side-by-side-assemblies-as-shared-assemblies.md)

Beachten Sie dabei Folgendes:

-   Assemblys, die mithilfe des [Benutzerinstallationskontexts](/windows/desktop/Msi/installation-context) im globalen Assemblycache installiert werden, werden nicht durch Windows Dateischutz geschützt.
-   Assemblys, die mithilfe des [Installationskontexts](/windows/desktop/Msi/installation-context) pro Computer im globalen Assemblycache installiert werden, werden durch Windows Dateischutz geschützt.

 

 
