---
title: Sequenzkomprimierung
description: Sequenzkomprimierung
ms.assetid: ea24088d-6a52-4d4e-8496-5b6a6616f684
keywords:
- Videokomprimierungs-Manager (VCM), Sequenzkomprimierung
- VCM (Videokomprimierungs-Manager), Sequenzkomprimierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c930c1f2a3e73e21e63195129221aaa28017e5a8d59122be9d8cbf956b828bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688870"
---
# <a name="sequence-compression"></a>Sequenzkomprimierung

Ihre Anwendung kann die [**Funktionen ICSeqCompressFrame,**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe) [**ICSeqCompressFrameStart**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart)und [**ICSeqCompressFrameEnd**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend) verwenden, um eine Sequenz von Frames zu komprimieren. Diese Funktionen verwenden die in der [**COMPVARS-Struktur gespeicherten**](/windows/desktop/api/Vfw/ns-vfw-compvars) Daten. Anwendungen verwenden die [**ICCompressorChoose-Funktion,**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) um dem Benutzer das Auswählen eines Gerüsts, das Öffnen und das Festlegen der Komprimierungsparameter in der **COMPVARS-Struktur zu** ermöglichen. Anwendungen können die Parameter jedoch manuell in der Struktur festlegen.

Bevor eine Anwendung mit dem Komprimieren einer Sequenz von Frames beginnen kann, muss sie **ICSeqCompressFrameStart** verwenden, um die erforderlichen Ressourcen zu reservieren. Nachdem die Ressourcen zugeordnet wurden, kann die Anwendung **ICSeqCompressFrame** verwenden, um jeden Frame einzeln zu komprimieren. Die Framerate und die Keyframefrequenz, die beim Komprimieren der Sequenz verwendet werden, werden in Membern der **COMPVARS-Struktur** angegeben. Der Rückgabewert für **ICSeqCompressFrame** verweist auf die komprimierten Daten.

Wenn eine Anwendung die Komprimierung einer Sequenz abgeschlossen hat, kann sie **ICSeqCompressFrameEnd** verwenden, um Systemressourcen frei zu geben, die **für ICSeqCompressFrameStart zugeordnet sind.** Um die für die **COMPVARS-Struktur** zugeordneten Ressourcen frei zu geben, kann die Anwendung die [**ICCompressorFree-Funktion**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) verwenden.

 

 




