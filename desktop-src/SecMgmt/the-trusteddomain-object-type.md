---
description: Windows-basierten Systemen können mehrere Instanzen des TrustedDomain-Objekttyps haben.
ms.assetid: 13efedb5-ebb6-459b-8c4f-06774226278c
title: Der TrustedDomain-Objekttyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdab860f9192e48433242251578a20a45bf294164c0bffff8b6f00562a1442e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004838"
---
# <a name="the-trusteddomain-object-type"></a>Der TrustedDomain-Objekttyp

Windows-basierten Systemen können mehrere Instanzen [](trusteddomain-object.md) des TrustedDomain-Objekttyps haben. **TrustedDomain-Objekte** verfügen über zwei Felder, die für alle **TrustedDomain-Objekte eindeutig sein** müssen:

-   Der Name der [ **TrustedDomain**](trusteddomain-object.md)
-   Die [*Sicherheits-ID*](/windows/desktop/SecGloss/s-gly) (SID) der [**TrustedDomain.**](trusteddomain-object.md)

Der Versuch, ein neues **TrustedDomain-Objekt** mit einem Namen oder einer SID zu erstellen, das bereits von einem anderen **TrustedDomain-Objekt** verwendet wird, wird abgelehnt.

 

 
