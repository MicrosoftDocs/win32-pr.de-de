---
description: Erläutert, wie Kontoobjekte geschützt werden.
ms.assetid: a07ef46e-f4b6-4e21-bdd7-72d03e1c88b3
title: Kontoobjektschutz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c49610827c8f27b2ad1dd645faca1374534b9d4acb8353421fc55901da724dd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117969759"
---
# <a name="account-object-protection"></a>Kontoobjektschutz

[**Kontoobjekte**](account-object.md) werden auf folgende Weise geschützt:

-   Die Gruppe **WORLD verfügt** über GENERIC \_ EXECUTE.
-   Die Gruppe **LOCAL \_ ADMIN** verfügt über DELETE-, GENERIC \_ READ-, GENERIC \_ WRITE-, GENERIC \_ EXECUTE- und \_ WRITE-DACL-Zugriff.
-   Die Gruppe **LOCAL \_ ADMIN** wird als Besitzer und primäre Gruppe von Kontoobjekten zugewiesen.

 

 



