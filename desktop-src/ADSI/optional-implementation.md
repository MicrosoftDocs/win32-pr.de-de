---
title: Optionale Implementierung
description: Die folgenden Features sind optional, werden jedoch empfohlen.
ms.assetid: 6123bdda-06cf-4b8b-b2a8-89882b6341b4
ms.tgt_platform: multiple
keywords:
- Optionale Implementierung ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3074f3ef6b4d36713d483937ad0f6ef10167777a7c36f8d21427d7df2b0485a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838950"
---
# <a name="optional-implementation"></a>Optionale Implementierung

Die folgenden Features sind optional, werden jedoch empfohlen:

-   Die [**IDirectorySearch-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) für Nicht-Automatisierungsclients. Da der ADSI-OLE DB-Anbieter **IDirectorySearch** verwendet, um Abfragen darzustellen und Ergebnisse aus dem zugrunde liegenden Verzeichnisdienst zu sammeln, bieten Anbieter, die diese Schnittstelle implementieren, automatisch Zugriff auf OLE DB Datenbanken im Stil, ohne zusätzliche Schnittstellen implementieren zu müssen.
-   Die Schnittstellen [**IADsSecurityDescriptor,**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)und [**IADsAccessControlEntry.**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) Anbietern für Verzeichnisdienste, die ACL-basierte Objektsicherheit unterstützen, wird empfohlen, diese zusätzlichen Features zu implementieren.

 

 




