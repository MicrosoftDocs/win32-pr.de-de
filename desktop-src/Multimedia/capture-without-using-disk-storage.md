---
title: Erfassung ohne Verwendung Disk Storage
description: Erfassung ohne Verwendung Disk Storage
ms.assetid: 2e2f1b67-69be-424c-8a6f-d9db5eeb6088
keywords:
- WM_CAP_SEQUENCE_NOFILE Meldung
- capcapturesequencenofile-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76fa69fa8a827117dbc110a410cb40084614559
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337358"
---
# <a name="capture-without-using-disk-storage"></a>Erfassung ohne Verwendung Disk Storage

Sie können Aufzeichnungs Dienste verwenden, ohne die Daten in eine Datenträger Datei zu schreiben, indem Sie die " [**WM \_ Cap \_ Sequence \_ NoFile**](wm-cap-sequence-nofile.md) "-Nachricht (oder das [**capcapturesequencenofile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) -Makro) verwenden. Diese Meldung ist nur in Verbindung mit Rückruf Funktionen hilfreich, mit denen Ihre Anwendung die Video-und Audiodaten direkt verwenden kann. Beispielsweise können Videokonferenz-Anwendungen diese Nachricht zum Abrufen von streamingvideoframes verwenden. Die Rückruf Funktionen würden die erfassten Images auf den Remote Computer übertragen.

 

 




