---
title: User-Selected-Kompressoren
description: User-Selected-Kompressoren
ms.assetid: 38569f9c-2df3-4959-990b-5c33203ff916
keywords:
- Videokomprimierungs-Manager (VCM), vom Benutzer ausgewählte Kompressoren
- VCM (Videokomprimierungs-Manager), vom Benutzer ausgewählte Kompressoren
- Iccompressorchoose-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbbba48b919265ea6e0bab2c3d891f628c4e660a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947879"
---
# <a name="user-selected-compressors"></a>User-Selected-Kompressoren

Wenn Sie Daten komprimieren, kann die Anwendung die [**iccompressorchoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) -Funktion verwenden, um ein Dialogfeld zu erstellen, in dem der Benutzer den Kompressor auswählen kann. Sie können Flags für diese Funktion angeben, um dem Benutzer die Angabe der Keyframe-Frequenz und der Movie-Data-Rate oder das Anzeigen eines Vorschau Fensters zu ermöglichen.

Der vom Benutzer ausgewählte Kompressor wird automatisch geöffnet, und das zugehörige Handle wird im hussiemember der in **iccompressorchoose** angegebenen [**compvars**](/windows/desktop/api/Vfw/ns-vfw-compvars) -Struktur zurückgegeben.

Wenn Sie **iccompressorchoose** verwenden, verwenden Sie die [**iccompressorfree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) -Funktion, um den-Kompressor zu schließen und alle Ressourcen freizugeben, die der **compvars** -Struktur zugeordnet sind.

 

 




