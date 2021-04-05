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
# <a name="the-trusteddomain-object-type"></a>Der "Treuhänder Domain"-Objekttyp

Windows-basierte Systeme können über mehrere Instanzen des Objekttyp " [**Treuhänder**](trusteddomain-object.md) " verfügen. Die Objekte für die **Treuhänder Domäne** verfügen über zwei Felder, die in allen " **Treuhänder Domain** "-Objekten eindeutig sein müssen:

-   Der Name der [ **Treuhänder Domäne**](trusteddomain-object.md)
-   Die [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -ID (SID) der [**Treuhänder Domäne**](trusteddomain-object.md).

Der Versuch, ein neues " **Treuhänder Domain** "-Objekt mit einem Namen oder einer SID zu erstellen, die bereits von einem anderen " **Treuhänder Domain** "-Objekt verwendet wird, wird zurückgewiesen.

 

 
