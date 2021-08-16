---
title: Kategorisieren von DCOM-Proxys und Stubs
description: Kategorisieren von DCOM-Proxys und Stubs
ms.assetid: f5d117d6-6c2c-4beb-8869-1581a5b1846f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f45f61d89e31316975685d3e603a93d30559546c86abc3b63e8e7e8a0c83ff1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310867"
---
# <a name="categorizing-dcom-proxies-and-stubs"></a>Kategorisieren von DCOM-Proxys und Stubs

DCOM marshallt Verweise auf -Objekte, indem OBJREFs erstellt werden, die CLSIDs enthalten. Diese CLSIDs sind anfällig für Sicherheitsangriffe, da während des Marshallings beliebige DLLs geladen werden können. Das EOAC \_ NO \_ CUSTOM \_ MARSHAL-Flag kann jedoch beim Aufrufen von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) angegeben werden (siehe [**EOLE AUTHENTICATION \_ \_ CAPABILITIES**](/windows/win32/api/objidlbase/ne-objidlbase-eole_authentication_capabilities)). Das Festlegen dieses Flags trägt zum Schutz der Serversicherheit bei der Verwendung von DCOM bei, da es die Wahrscheinlichkeit verringert, dass beliebige DLLs ausgeführt werden. Wenn dieses Flag festgelegt ist, lässt der Server das Marshalling nur von CLSIDs zu, die in ole32.dll, comadmin.dll, comsvcs.dll oder es.dll implementiert sind oder die die KATEGORIE-ID CATID \_ MARSHALER implementieren.

CATID \_ MARSHALER ist eine Komponentenkategorie-GUID, die einer CLSID zugeordnet werden kann, die benutzerdefiniertes Marshalling vorliegt. Die Schnittstellen, die mit dieser CLSID gemarshallt werden, sind zulässig, wenn die EOAC \_ NO \_ CUSTOM \_ MARSHAL über [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)festgelegt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Komponentenkategorien](component-categories.md)
</dt> </dl>

 

 