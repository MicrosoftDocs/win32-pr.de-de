---
description: Beschreibt, wie das Policy-Objekt standardmäßig geschützt wird.
ms.assetid: e2d65ebf-5fbd-4e25-9862-a8188abb5492
title: Richtlinienobjektschutz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3317d9cef2a6ff1dfa29753f9a807286d62f31abb0e8c0c9d0150ee10535a1fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894060"
---
# <a name="policy-object-protection"></a>Richtlinienobjektschutz

Das [**Richtlinienobjekt**](policy-object.md) ist standardmäßig mit den folgenden Einstellungen geschützt:

-   Die lokale Gruppe WORLD verfügt über GENERIC \_ EXECUTE-Zugriff.
-   Dem bekannten ID-System wird POLICY \_ ALL \_ ACCESS gewährt.
-   Die lokale Gruppe LOCAL \_ ADMIN verfügt \_ über \_ GENERISCHEN LESE-, GENERISCHEN SCHREIB- und GENERISCHEN \_ EXECUTE-Zugriff.
-   Die Gruppe LOCAL \_ ADMIN wird als Besitzer und primäre Gruppe dieses Objekts zugewiesen.

Das [**Richtlinienobjekt**](policy-object.md) kann nicht erstellt oder zerstört werden.

 

 



