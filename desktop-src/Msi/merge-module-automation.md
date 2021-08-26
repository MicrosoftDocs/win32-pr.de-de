---
description: Mergemod.dll stellt ein COM-Objekt bereit, das Mergevorgänge und die Quellimagegenerierung für Mergemodule implementiert. Das Hauptobjekt implementiert Schnittstellen für C/C++-Programme und Automatisierungsclients, einschließlich Visual Basic und VBScript.
ms.assetid: 877d3691-948f-4aea-89d8-0ff008126ccc
title: Modulautomatisierung zusammenführen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e592429b77671e154b932f3d79f6f57bb39a65ee2058aafd2164428234458acf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043050"
---
# <a name="merge-module-automation"></a>Modulautomatisierung zusammenführen

Mergemod.dll stellt ein COM-Objekt bereit, das Mergevorgänge und die Quellimagegenerierung für Mergemodule implementiert. Das Hauptobjekt implementiert Schnittstellen für C/C++-Programme und Automatisierungsclients, einschließlich Visual Basic und VBScript.

Die bevorzugte Methode zum Installieren von Mergemod.dll ist die Verwendung des Windows Installers. Die Komponenten-ID für die Komponente, die die Mergemod.dll COM-Schnittstelle enthält, lautet {FD153241-37EC-11D2-8892-00A0C981B015}. Die gleiche Binärdatei kann auf allen Windows Systemen verwendet werden, und die DLL registriert sich selbst über regsvr32 auf älteren Systemen.

Beachten Sie, dass Mergemod.dll erfordert, dass die Msvcrt.dll auf dem System installiert werden.

Beachten Sie, dass Mergemod.dll 2.0 erforderlich ist, um [konfigurierbare Mergemodule](configurable-merge-modules.md)zu erstellen. Mergemod.dll Version 2.0 bietet erweiterte Funktionen zur Buildzeit über die [**IMsmMerge2-Schnittstelle.**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) Diese CLSID unterstützt alle vorhandenen Funktionen der [**IMsmMerge-Schnittstelle,**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) die von Mergemod.dll Version 1.0 bereitgestellt wird. Die Standardschnittstelle für das [**Merge-Objekt**](merge-object.md) von Mergemod.dll 2.0 ist die **IMsmMerge2-Schnittstelle** anstelle der **IMsmMerge-Schnittstelle.**

[Objektmodell für Mergemod.dll Version 1.0](object-model-for-mergemod-dll-version-1-0.md)

[Objektmodell für Mergemod.dll Version 2.0](object-model-for-mergemod-dll-version-2-0.md)

 

 
