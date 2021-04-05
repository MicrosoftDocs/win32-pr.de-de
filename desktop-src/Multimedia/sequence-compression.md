---
title: Sequenz Komprimierung
description: Sequenz Komprimierung
ms.assetid: ea24088d-6a52-4d4e-8496-5b6a6616f684
keywords:
- Videokomprimierungs-Manager (VCM), Sequenz Komprimierung
- VCM (Videokomprimierungs-Manager), Sequenz Komprimierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8485c31361540ae0e0e9569453bc610d10d88d3d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947664"
---
# <a name="sequence-compression"></a>Sequenz Komprimierung

Die Anwendung kann die Funktionen " [**icseqcompressframe**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe)", " [**icseqcompressframestart**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart)" und " [**icseqcompressframeend**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend) " verwenden, um eine Sequenz von Frames zu komprimieren. Diese Funktionen verwenden die in der [**compvars**](/windows/desktop/api/Vfw/ns-vfw-compvars) -Struktur gespeicherten Daten. Anwendungen verwenden die Funktion [**iccompressorchoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) , um dem Benutzer zu ermöglichen, einen Kompressor auszuwählen, zu öffnen und die Komprimierungs Parameter in der **compvars** -Struktur festzulegen. Anwendungen können die Parameter in der Struktur jedoch manuell festlegen.

Bevor eine Anwendung damit beginnen kann, eine Sequenz von Frames zu komprimieren, muss Sie **icseqcompressframestart** verwenden, um die erforderlichen Ressourcen zuzuordnen. Nachdem die Ressourcen zugewiesen wurden, kann die Anwendung **icseqcompressframe** verwenden, um jeden Frame einzeln zu komprimieren. Die bei der Komprimierung der Sequenz verwendete Framerate und die Keyframe-Frequenz werden in Elementen der **compvars** -Struktur angegeben. Der Rückgabewert für **iccqcompressframe** verweist auf die komprimierten Daten.

Wenn eine Anwendung das Komprimieren einer Sequenz abgeschlossen hat, kann **icseqcompressframeend** verwendet werden, um Systemressourcen freizugeben, die für **icseqcompressframestart** reserviert wurden. Um die Ressourcen freizugeben, die für die **compvars** -Struktur reserviert werden, kann die Anwendung die [**iccompressorfree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) -Funktion verwenden.

 

 




