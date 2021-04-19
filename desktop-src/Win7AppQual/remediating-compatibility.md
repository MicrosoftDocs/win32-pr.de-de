---
description: .
ms.assetid: 18F74BA7-2729-4EB3-8E6F-4E5A8C17C317
title: DEP/NX-Kompatibilität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb542331d218ed4c493efde091be3e5efae6aee
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106364287"
---
# <a name="depnx-compatibility"></a>DEP/NX-Kompatibilität

In Windows Internet Explorer 7 wird DEP/NX standardmäßig aus Kompatibilitätsgründen deaktiviert. Mehrere beliebte Add-ons sind nicht mit DEP/NX kompatibel und schlagen fehl, wenn Sie von Windows Internet Explorer mit aktiviertem DEP/NX geladen werden.

In der Regel werden diese Add-ons mithilfe einer älteren Version des ATL-Frameworks erstellt. ATL 7,1 und frühere Versionen sind nicht mit dem DEP-Sicherheits Feature konzipiert. Glücklicherweise verfügen neue Versionen von Microsoft Windows Service Packs über neue DEP/NX-APIs, die es Ihnen ermöglichen, DEP/NX zu verwenden und die Kompatibilität mit älteren ATL-Versionen beizubehalten. Diese neuen APIs ermöglichen es Internet Explorer, DEP/NX zu abonnieren, ohne dass Add-ons, die mit älteren Versionen von ATL erstellt wurden, fehlschlagen.

Wenn ein Add-on nicht mit DEP/NX kompatibel ist und keinen veralteten ATL-Code verwendet, können Sie eine Gruppenrichtlinie Option verwenden, um DEP/NX für Internet Explorer zu abonnieren, bis eine aktualisierte Version des unterbrochenen Steuer Elements bereitgestellt wird. Lokale Administratoren können DEP/NX steuern, indem Sie Internet Explorer als Administrator ausführen und die Option **Speicherschutz aktivieren** im **erweiterten** Bereich der **Internet Optionen** löschen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe der Kompatibilitäts Ansicht](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
