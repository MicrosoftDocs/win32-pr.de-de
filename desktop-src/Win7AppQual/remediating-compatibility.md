---
description: DEP/NX-Kompatibilität
ms.assetid: 18F74BA7-2729-4EB3-8E6F-4E5A8C17C317
title: DEP/NX-Kompatibilität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65af83e43defb5216b176755dbc8f32067f907620bc120a16aff8b6db3392c9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118329625"
---
# <a name="depnx-compatibility"></a>DEP/NX-Kompatibilität

In der Standardeinstellung Windows Internet Explorer 7 DEP/NX aus Kompatibilitätsgründen deaktiviert. Mehrere beliebte Add-Ons sind nicht mit DEP/NX kompatibel und führen zu einem Fehler, wenn Windows Internet Explorer mit aktivierter DEP/NX geladen werden.

In der Regel werden diese Add-Ons mit einer älteren Version des ATL-Frameworks erstellt. ATL 7.1 und frühere Versionen wurden nicht mit dem DEP-Sicherheitsfeature entworfen. Glücklicherweise verfügen neue Versionen von Microsoft Windows Service Packs über neue DEP/NX-APIs, mit denen Sie DEP/NX verwenden und die Kompatibilität mit älteren ATL-Versionen beibehalten können. Diese neuen APIs ermöglichen es Internet Explorer, SICH für DEP/NX zu entscheiden, ohne dass Add-Ons, die mit älteren Versionen von ATL erstellt werden, fehlschlagen.

Wenn ein Add-On nicht DEP-/NX-kompatibel ist und kein veraltetes ATL verwendet, können Sie eine Gruppenrichtlinie-Option verwenden, um DEP/NX für Internet Explorer zu deaktivieren, bis eine aktualisierte Version des fehlerhaften Steuerelements bereitgestellt wird. Lokale Administratoren können DEP/NX steuern, indem sie Internet Explorer  als Administrator ausführen  und die Option Speicherschutz aktivieren im Bereich Erweitert von **Internetoptionen deaktivieren.**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beheben von Kompatibilitätsproblemen in Webanwendungen mit Kompatibilitätsansicht](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
