---
title: Kategorisierung von DCOM-Proxys und Stub
description: Kategorisierung von DCOM-Proxys und Stub
ms.assetid: f5d117d6-6c2c-4beb-8869-1581a5b1846f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31685cd1318856b9e305246cfebc2cebb3a7874e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106341333"
---
# <a name="categorizing-dcom-proxies-and-stubs"></a>Kategorisierung von DCOM-Proxys und Stub

DCOM Marshalls Verweise auf Objekte durch das Erstellen von objrefs, die CLSIDs enthalten. Diese CLSIDs sind anfällig für Sicherheitsangriffe, da beliebige DLLs während des Marshalling geladen werden können. Allerdings \_ \_ \_ kann beim Aufrufen von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) das eoac-Flag No Custom Marshal angegeben werden (siehe [**Eole- \_ Authentifizierungs \_ Funktionen**](/windows/win32/api/objidlbase/ne-objidlbase-eole_authentication_capabilities)). Das Festlegen dieses Flags trägt zum Schutz der Serversicherheit bei der Verwendung von DCOM bei, da es die Wahrscheinlichkeit verringert, dass beliebige DLLs ausgeführt werden Wenn dieses Flag festgelegt ist, lässt der Server nur das Marshalling von CLSIDs zu, die in ole32.dll, comadmin.dll, comsvcs.dll oder es.dll implementiert sind oder die die CATID- \_ Marshaler-Kategorie-ID implementieren.

Der CATID- \_ Mars Haller ist eine Komponenten Kategorie-GUID, die einer CLSID zugeordnet werden kann, die Benutzer definiert gemarshallt wird. Die Schnittstellen, die mit dieser CLSID als Benutzer definiert gemarshallt werden, sind zulässig, wenn der eoac \_ keinen \_ benutzerdefinierten \_ Marshal über [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)festgelegt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Komponentenkategorien](component-categories.md)
</dt> </dl>

 

 