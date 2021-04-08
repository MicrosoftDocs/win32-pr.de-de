---
title: Grundlagen zu Kompressor und Debug
description: Grundlagen zu Kompressor und Debug
ms.assetid: 49a958c1-1798-4c6c-913c-5bf5869f926b
keywords:
- Videokomprimierungs-Manager (VCM), Öffnen von Kompressoren
- VCM (Videokomprimierungs-Manager), Öffnen von Kompressoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b51e0221c495d5e2d0782f4e56e0778c0d2462
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856052"
---
# <a name="compressor-and-decompressor-basics"></a>Grundlagen zu Kompressor und Debug

Zum Öffnen und Suchen eines Kompressors können Sie die [**iclocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) -Funktion und die [**icopen**](/windows/desktop/api/Vfw/nf-vfw-icopen) -Funktion verwenden. Sie können **iclocate** verwenden, um einen Kompressor eines bestimmten Typs zu finden und ein Handle dafür für die Verwendung in anderen VCM-Funktionen zu erhalten. Zum Öffnen eines Kompressors können Sie **icopen** verwenden. Die Anwendung verwendet das Handle, das von dieser Funktion zurückgegeben wird, um den geöffneten Kompressor zu identifizieren, wenn er andere VCM-Funktionen verwendet.

Zum Öffnen und Suchen eines-Debug können Anwendungen die [**ICDE compressopen**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen) -und [**icdrawopen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen) -Makros verwenden. Diese Makros verwenden **iclocate** für den Vorgang.

Wenn Ihre Anwendung die Verwendung eines Kompressors oder einer Debug-Debug abgeschlossen hat, muss Sie Sie schließen, um alle Ressourcen freizugeben, die für die Komprimierung oder die Komprimierung Die Anwendung kann die [**icclose**](/windows/desktop/api/Vfw/nf-vfw-icclose) -Funktion verwenden, um den-Kompressor oder den-Debug zu schließen.

Außerdem kann die Anwendung die Kompressoren oder die Aufzählung auf einem System mithilfe der [**icinfo**](/windows/desktop/api/Vfw/nf-vfw-icinfo) -Funktion auflisten.

> [!Note]  
> Der Stream-Header in einer AVI-Datei enthält Informationen über den Streamtyp und den spezifischen Handler für diesen Stream. Innerhalb des Stream-Headers identifizieren die Member **fcctype** und **fccHandler** den Streamtyp und den für den Stream angegebenen Stream-Handler.

 

 

 




