---
description: Beim Erstellen eines Security Support Provider SSP-Sicherheitspakets sollten Sie dem in die Domäne eingebundener Client nicht gestatten, sich mit einem zwei teiligen Dienstanbieter Namen (Service Provider Name, SPN) in der folgenden Form bei einem Domänen Controller zu authentifizieren.
ms.assetid: 6CD3BC5E-F9B2-4E8E-9DEE-064AE8837DFB
title: Verwenden von dreiteiligen Prinzipal Namen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8760ba740843c62c39a98e7e4683d25410a94ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346924"
---
# <a name="using-three-part-principal-names"></a>Verwenden von dreiteiligen Prinzipal Namen

Beim Erstellen eines Security Support Provider SSP-Sicherheitspakets sollten Sie dem in die Domäne eingebundener Client nicht gestatten, sich mit einem zwei teiligen Dienstanbieter Namen (Service Provider Name, SPN) in der folgenden Form bei einem Domänen Controller zu authentifizieren.

-   <*Protokoll* >/< *Hostname*>

Ein Client sollte sich stets authentifizieren, indem er die Domäne angibt.

-   <*Protokoll* >/< *Hostname* >/< *Domänen Name*>

Ein in eine Domäne eingebundener Client, der sich mit einem zwei teiligen SPN anmeldet, kann möglicherweise die Identität des Domänen Controllers annehmen. Wenn Sie zwei teilige SPNs zulassen, sollten Sie einen Protokolleintrag erstellen, der genügend Informationen enthält, um dem Administrator die Identifizierung des Aufrufers zu ermöglichen.

 

 



