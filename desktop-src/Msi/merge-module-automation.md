---
description: Mergemod.dll stellt ein COM-Objekt bereit, das Mergevorgänge und Quell Abbild Generierung für Mergemodule implementiert. Das Hauptobjekt implementiert Schnittstellen für C/C++-Programme und Automatisierungs Clients, einschließlich Visual Basic und VBScript.
ms.assetid: 877d3691-948f-4aea-89d8-0ff008126ccc
title: Modul Automatisierung zusammenführen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ae27370b2ad898cf9413567285afc41d117815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366219"
---
# <a name="merge-module-automation"></a>Modul Automatisierung zusammenführen

Mergemod.dll stellt ein COM-Objekt bereit, das Mergevorgänge und Quell Abbild Generierung für Mergemodule implementiert. Das Hauptobjekt implementiert Schnittstellen für C/C++-Programme und Automatisierungs Clients, einschließlich Visual Basic und VBScript.

Die bevorzugte Methode zum Installieren von Mergemod.dll ist die Verwendung der Windows Installer. Die Komponenten-ID der Komponente, die die Mergemod.dll com-Schnittstelle enthält, ist {FD153241-37EC-11d2-8892-00A0C981B015}. Die gleiche Binärdatei kann auf allen Windows-Systemen verwendet werden, und die dll wird über regsvr32 auf älteren Systemen selbst registriert.

Beachten Sie, dass Mergemod.dll erfordert, dass die Msvcrt.dll auf dem System installiert ist.

Beachten Sie, dass Mergemod.dll 2,0 erforderlich ist, um [konfigurierbare Mergemodule](configurable-merge-modules.md)zu erstellen. Mergemod.dll Version 2,0 bietet erweiterte Funktionalität zur Buildzeit über die [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) -Schnittstelle. Diese CLSID unterstützt alle vorhandenen Funktionen der [**imsmmerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) -Schnittstelle, die von Mergemod.dll Version 1,0 bereitgestellt wird. Die Standardschnittstelle für das [**Merge**](merge-object.md) -Objekt von Mergemod.dll 2,0 ist die **IMsmMerge2** -Schnittstelle anstelle der **imsmmerge** -Schnittstelle.

[Objektmodell für Mergemod.dll Version 1,0](object-model-for-mergemod-dll-version-1-0.md)

[Objektmodell für Mergemod.dll Version 2,0](object-model-for-mergemod-dll-version-2-0.md)

 

 
