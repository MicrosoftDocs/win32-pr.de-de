---
title: Still-Image Erfassung
description: Still-Image Erfassung
ms.assetid: 9e84b385-aedb-4132-8a2d-72c32594083a
keywords:
- WM_CAP_GRAB_FRAME_NOSTOP Meldung
- WM_CAP_GRAB_FRAME Meldung
- capgrabframenostop-Makro
- capgrabframe-Makro
- WM_CAP_EDIT_COPY Meldung
- capeditcopy-Makro
- WM_CAP_FILE_SAVEDIB Meldung
- capfilesavedib-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cb80d320f2bd90cfd62fef83d7b3066762b6ebe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100670"
---
# <a name="still-image-capture"></a>Still-Image Erfassung

Wenn Sie einen einzelnen Frame als noch Bild erfassen möchten, können Sie die Sende [**\_ \_ \_ Rahmen**](wm-cap-grab-frame.md) Nachricht "WM-Abdeckung zum Abrufen von [**\_ \_ \_ Rahmen \_**](wm-cap-grab-frame-nostop.md) " oder "WM-Abdeckung" (oder das Makro " [**capgrabframenostop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) " oder " [**capgrabframe**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) ") verwenden, um das digitalisierte Bild in einem internen Frame Puffer zu erfassen. Sie können die Anzeige für das erfasste Abbild mithilfe des WM- \_ Abdeckungs \_ \_ Rahmens fixieren. Verwenden Sie andernfalls den WM- \_ Abdeckungs \_ \_ Rahmen \_ nostoppt.

Nach der Erfassung können Sie das Abbild für die Verwendung durch andere Anwendungen kopieren. Sie können ein Bild aus dem Frame Puffer in die Zwischenablage kopieren, indem Sie die Meldung zum [**\_ \_ Bearbeiten \_ der WM**](wm-cap-edit-copy.md) -Abdeckung (oder das [**capeditcopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) -Makro) verwenden. Sie können das Bild auch aus dem Frame Puffer in eine geräteunabhängige Bitmap (DIB) kopieren, indem Sie die [**\_ Datei " \_ \_ savedib**](wm-cap-file-savedib.md) " der WM-Cap-Datei (oder das Makro [**capfilesavedib**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) ) verwenden.

Die Anwendung kann auch die zwei einzelnen Frame Erfassungs Nachrichten verwenden, um einen Sequenz Rahmen nach Frame zu bearbeiten oder um eine Zeitverlaufs-Fotosequenz zu erstellen.

 

 




