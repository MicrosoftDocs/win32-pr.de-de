---
description: Festlegen von Administratorrechten für eine Partition
ms.assetid: d38e4a63-9ff9-4acb-bb7e-d6c96644bd32
title: Festlegen von Administratorrechten für eine Partition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33431c5beff76e015d28b6a7e886823620126f2ed9b84db68af9a8f3b8ac1d28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117915823"
---
# <a name="setting-administrative-rights-for-a-partition"></a>Festlegen von Administratorrechten für eine Partition

Benutzer, die der Rolle Administrator der COM+-Systemanwendung zugewiesen sind, dürfen COM+-Partitionen erstellen, ändern und löschen. Im Verwaltungstool komponentendienste können Benutzern Administratorrollen zugewiesen werden, indem Sie den Ordner **Rollen** der COM+-Systemanwendung erweitern.

Ab Windows Server 2003 enthält die Authentifizierungsfunktion für die COM+-Systemanwendung den Wert EOAC \_ DISABLE \_ AAA. Dieser Wert, der aktivierungsbasierte Aktivierungen (Activate-as-Activator, AAA) deaktiviert, wird beim Starten der Systemanwendung im [**CoInitializeSecurity-Aufruf**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) verwendet. Wenn Sie die Authentifizierungsfunktion auf EOAC DISABLE AAA festlegen, kann eine Anwendung, die unter einem privilegierten Konto (z. B. LocalSystem) ausgeführt wird, verhindern, dass ihre Identität zum Starten nicht vertrauenswürdiger Komponenten verwendet \_ \_ wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sammeln von Partitionsmetriken](collecting-partition-metrics.md)
</dt> <dt>

[Konfigurieren des Partitionscaches](configuring-the-partition-cache.md)
</dt> <dt>

[Gruppieren von Anwendungen in Partitionen](grouping-applications-into-partitions.md)
</dt> <dt>

[Verwalten von lokalen Partitionen](managing-local-partitions.md)
</dt> <dt>

[Verwalten von Partitionen in Active Directory](managing-partitions-within-active-directory.md)
</dt> </dl>

 

 
