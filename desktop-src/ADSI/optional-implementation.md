---
title: Optionale Implementierung
description: Die folgenden Funktionen sind optional, werden jedoch empfohlen.
ms.assetid: 6123bdda-06cf-4b8b-b2a8-89882b6341b4
ms.tgt_platform: multiple
keywords:
- Optionaler Implementierungs-ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 043b07f3a9bcfaef4bde8e95458d64828d4e46be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515458"
---
# <a name="optional-implementation"></a>Optionale Implementierung

Die folgenden Funktionen sind optional, werden jedoch empfohlen:

-   Die [**idirector ysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle für nicht-Automatisierungs Clients. Da der ADSI OLE DB-Anbieter **IDirectorySearch** verwendet, um Abfragen zu präsentieren und Ergebnisse aus dem zugrunde liegenden Verzeichnisdienst zu erfassen, ermöglichen Anbieter, die diese Schnittstelle implementieren, automatisch den Zugriff auf OLE DB Format Datenbanken, ohne dass zusätzliche Schnittstellen implementiert werden müssen.
-   Die Schnittstellen [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)und [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) . Anbieter für Verzeichnisdienste, die die ACL-basierte Objektsicherheit unterstützen, werden empfohlen, diese zusätzlichen Features zu implementieren.

 

 




