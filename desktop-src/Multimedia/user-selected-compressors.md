---
title: User-SelectedUser-Selected
description: User-SelectedUser-Selected
ms.assetid: 38569f9c-2df3-4959-990b-5c33203ff916
keywords:
- Videokomprimierungs-Manager (VCM), vom Benutzer ausgewählte Komprimierungs-Manager
- VCM (Videokomprimierungs-Manager), vom Benutzer ausgewählte Komprimierungen
- ICCompressorChoose-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c855acb1ecd69876009d0cc3eb6a3b3f4129cc252183e40c5b2d00289be82842
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370800"
---
# <a name="user-selected-compressors"></a>User-SelectedUser-Selected

Beim Komprimieren von Daten kann Ihre Anwendung die [**ICCompressorChoose-Funktion**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) verwenden, um ein Dialogfeld zu erstellen, in dem der Benutzer den Eintrag auswählen kann. Sie können Flags für diese Funktion angeben, damit der Benutzer die Keyframehäufigkeit und die Filmdatenrate angeben oder ein Vorschaufenster anzeigen kann.

Das vom Benutzer ausgewählte Element wird automatisch geöffnet, und sein Handle wird im hic-Member der [**COMPVARS-Struktur zurückgegeben,**](/windows/desktop/api/Vfw/ns-vfw-compvars) die in **ICCompressorChoose** angegeben ist.

Wenn Sie **ICCompressorChoose** verwenden, verwenden Sie die [**ICCompressorFree-Funktion,**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) um die Schäden zu schließen und alle Ressourcen frei zu machen, die der **COMPVARS-Struktur** zugeordnet sind.

 

 




