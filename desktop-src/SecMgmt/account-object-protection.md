---
description: Erläutert, wie Konto Objekte geschützt werden.
ms.assetid: a07ef46e-f4b6-4e21-bdd7-72d03e1c88b3
title: Konto Objektschutz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f495a3dc943ef73eef5074e0edc73247ceb02d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347511"
---
# <a name="account-object-protection"></a>Konto Objektschutz

[**Konto**](account-object.md) Objekte werden wie folgt geschützt:

-   Die Gruppe " **World** " hat eine generische \_ Ausführung.
-   Der **lokale \_ Administrator** der Gruppe verfügt über DELETE \_ -, Generic Read-, generic \_ Write-, generic \_ Execute-und Write- \_ DACL-Zugriff.
-   Der **lokale \_ Administrator** der Gruppe wird als Besitzer und primäre Gruppe von Konto Objekten zugewiesen.

 

 



