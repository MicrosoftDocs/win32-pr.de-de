---
title: Erstellen eines externen Verweises
description: Wenn ein externes CrossRef-Objekt erstellt wird und ein Domänen Controller es zum Generieren eines Verweises verwendet, stellt das CrossRef-Objekt zwei wichtige Datenelemente in den folgenden Eigenschaften bereit.
ms.assetid: 9805390c-9e8d-4afd-bffc-43abf6055413
ms.tgt_platform: multiple
keywords:
- externe Verweise Active Directory
- Active Directory Beispiele Active Directory, Erstellen eines externen Verweises
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801a9306c374a0c22d206e9a0f9dbb8cd240da0c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724592"
---
# <a name="creating-an-external-referral"></a>Erstellen eines externen Verweises

Wenn ein externes [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekt erstellt wird und ein Domänen Controller es zum Generieren eines Verweises verwendet, stellt das **CrossRef** -Objekt zwei wichtige Datenelemente in den folgenden Eigenschaften bereit. Weitere Informationen zu Situationen, in denen dies auftreten kann, finden Sie im vorherigen Abschnitt.



| Eigenschaft                           | BESCHREIBUNG                                                                                                                                                         |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) | Gibt den Server oder die Domäne an, der Daten aus dem namens Kontext bereitstellen kann, der in [**NCName**](/windows/desktop/ADSchema/a-ncname)angegeben ist.                                           |
| [**NCName**](/windows/desktop/ADSchema/a-ncname)   | Gibt den Distinguished Name für die Domäne, das Schema oder den Konfigurations Container an, die auf dem durch [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot)angegebenen Server oder in der Domäne verankert ist. |



 

Wenn z. b. der Server mit der DNS-Adresse serv1.Northwest.fabrikam.com den namens Kontext für CN = MyContainer, ou = mydom, O = Fabrikam verwendet, legen [**Sie die DNS-Adresse des Servers**](/windows/desktop/ADSchema/a-dnsroot) auf die DNS-Adresse des Servers und [**NCName**](/windows/desktop/ADSchema/a-ncname) auf den Distinguished Name der Domäne, des Schemas oder des Konfigurations Containers fest.

Weitere Informationen und ein Codebeispiel, das zeigt, wie Sie einen externen Verweis erstellen, finden Sie unter [Beispielcode zum Erstellen eines externen CrossRef-Objekts](example-code-for-creating-an-external-crossref-object.md).

 

 