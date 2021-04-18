---
title: Multimedia-Aufzeichnung
description: Multimedia-Aufzeichnung
ms.assetid: e37aaac2-be89-4907-b1a8-f2c64ab2f39e
keywords:
- Mciwndcreate-Funktion
- Mciwndnew-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6b1793ff7653e87a631ce1a4599345ec78f4015
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388276"
---
# <a name="multimedia-recording"></a>Multimedia-Aufzeichnung

Sie können Aufzeichnungsfunktionen in Ihrer Anwendung implementieren, indem Sie die in mciwnd integrierte Benutzeroberfläche verwenden. Sie können die [**mciwndcreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) -Funktion und das [**mciwndnew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) -Makro verwenden, um Steuerelemente zum Starten und Beenden der Aufzeichnung und zum Speichern der aufgezeichneten Informationen bereitzustellen. Mithilfe von " **mciwndcreate**" können Sie Fenster Stile zum Anzeigen eines mciwnd-Fensters und zum Einschließen der Schaltfläche **Datensatz** auf der Symbolleiste angeben. Mit **mciwndnew** können Sie den Gerätetyp angeben, der aufgezeichnet wird, und angeben, dass die Informationen in einer neuen Datei erfasst werden sollen.

Wenn Ihre Anwendung eine höhere Komplexität erfordert, können Sie die Aufzeichnung automatisieren und anpassen, indem Sie das [**mciwndrecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord) -Makro verwenden. Weitere Informationen finden Sie unter [Anpassen des Aufzeichnungsprozesses](customizing-the-recording-process.md).

> [!Note]  
> Einige Geräte, z. b. CD-Audiodaten und MCIAVI, werden nur für die Wiedergabe verwendet. Andere Geräte, z. b. Waveform-Audiogeräte, können für die Aufzeichnung verwendet werden. Wenn Sie ein Gerät angeben, das nicht aufzeichnen kann, lässt mciwnd die Schaltfläche **Datensatz** von der Symbolleiste aus.

 

 

 




