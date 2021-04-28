---
description: DEP/NX-Kompatibilität
ms.assetid: 18F74BA7-2729-4EB3-8E6F-4E5A8C17C317
title: DEP/NX-Kompatibilität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb8b46c9143ee96b8599c10d4c70276d36e20a08
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116428"
---
# <a name="depnx-compatibility"></a>DEP/NX-Kompatibilität

In Windows Internet Explorer 7 ist DEP/NX aus Kompatibilitätsgründen standardmäßig deaktiviert. Mehrere beliebte Add-Ons sind nicht mit DEP/NX kompatibel und schlagen fehl, wenn Windows Internet Explorer sie mit aktivierter DEP/NX lädt.

In der Regel werden diese Add-Ons mit einer älteren Version des ATL-Frameworks erstellt. ATL 7.1 und frühere Versionen sind nicht mit dem DEP-Sicherheitsfeature konzipiert. Glücklicherweise verfügen neue Versionen von Microsoft Windows Service Packs über neue DEP-/NX-APIs, mit denen Sie DEP/NX verwenden und die Kompatibilität mit älteren ATL-Versionen beibehalten können. Diese neuen APIs ermöglichen es Internet Explorer, SICH für DEP/NX zu entscheiden, ohne dass Add-Ons, die mit älteren AtL-Versionen erstellt wurden, fehlschlagen.

Wenn ein Add-On nicht DEP-/NX-kompatibel ist und keine veraltete ATL verwendet, können Sie eine Gruppenrichtlinie Option verwenden, um DEP/NX für Internet Explorer zu deaktivieren, bis eine aktualisierte Version des fehlerhaften Steuerelements bereitgestellt wird. Lokale Administratoren können DEP/NX steuern, indem sie Internet Explorer als Administrator ausführen und die Option **Speicherschutz aktivieren** im Bereich **Erweitert** von **Internetoptionen** deaktivieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe von Kompatibilitätsansicht](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
