---
title: Benennen von Kontexten und Verzeichnispartitionen
description: Jeder Domänencontroller in einer von einer Domäne gesteuerten Gesamtstruktur Active Directory Domain Services Verzeichnispartitionen.
ms.assetid: 77ac171c-2031-46d7-b81e-dd9ae0c70ccb
ms.tgt_platform: multiple
keywords:
- Benennen von Kontexten und Verzeichnispartitionen AD
- Naming Contexts AD , About
- Verzeichnispartitionen AD , Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d309b76b50270f093b3a4930680b343d517976e269e731082696b89bf6a58c46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025708"
---
# <a name="naming-contexts-and-directory-partitions"></a>Benennen von Kontexten und Verzeichnispartitionen

Jeder Domänencontroller in einer domänenstruktur, die von einem Active Directory Domain Services enthält [*Verzeichnispartitionen.*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)) Verzeichnispartitionen werden auch als [*Namenskontexte bezeichnet.*](/previous-versions/windows/desktop/legacy/ms681918(v=vs.85)) Eine Verzeichnispartition ist ein zusammenhängender Teil des gesamten Verzeichnisses mit unabhängigem Replikationsbereich und Zeitplanungsdaten. Standardmäßig enthält der Active Directory-Domäne-Dienst für ein Unternehmen die folgenden Partitionen:

-   [*Schemapartition:*](/previous-versions/windows/desktop/legacy/ms681936(v=vs.85))Die Schemapartition enthält **die Objekte classSchema** und **attributeSchema,** die die Typen von Objekten definieren, die in der Gesamtstruktur vorhanden sein können. Jeder Domänencontroller in der Gesamtstruktur verfügt über ein Replikat derselben Schemapartition.
-   [*Konfigurationspartition:*](/previous-versions/windows/desktop/legacy/ms681898(v=vs.85))Die Konfigurationspartition enthält die Replikationstopologie und andere Konfigurationsdaten, die in der gesamten Gesamtstruktur repliziert werden müssen. Jeder Domänencontroller in der Gesamtstruktur verfügt über ein Replikat derselben Konfigurationspartition.
-   [*Domänenpartition:*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85))Die Domänenpartition enthält die Verzeichnisobjekte, z. B. Benutzer und Computer, die der lokalen Domäne zugeordnet sind. Eine Domäne kann über mehrere Domänencontroller und eine Gesamtstruktur über mehrere Domänen verfügen. Jeder Domänencontroller speichert ein vollständiges Replikat der Domänenpartition für seine lokale Domäne, aber keine Replikate der Domänenpartitionen für andere Domänen.

Windows Server 2003 führt die Anwendungsverzeichnispartition ein, die die Möglichkeit bietet, den Replikationsbereich zu steuern und die Platzierung von Replikaten auf eine Weise zu ermöglichen, die für dynamische Daten besser geeignet ist. Weitere Informationen zu Anwendungsverzeichnispartitionen finden Sie unter [Informationen zu Anwendungsverzeichnispartitionen.](about-application-directory-partitions.md)

Weitere Informationen dazu, wie Active Directory Domain Services konsistenz zwischen den verschiedenen Replikaten einer Verzeichnispartition erhalten, finden Sie unter [Replikation und Datenintegrität.](replication-and-data-integrity.md)

 

 