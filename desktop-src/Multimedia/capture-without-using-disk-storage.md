---
title: Erfassen ohne Datenträger-Storage
description: Erfassen ohne Datenträger-Storage
ms.assetid: 2e2f1b67-69be-424c-8a6f-d9db5eeb6088
keywords:
- WM_CAP_SEQUENCE_NOFILE Meldung
- capCaptureSequenceNoFile-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ea708bd99cc2c325623eb53d734fadb2acdd0112e3a727fae9bfa741b8d301e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691620"
---
# <a name="capture-without-using-disk-storage"></a>Erfassen ohne Datenträger-Storage

Sie können Erfassungsdienste verwenden, ohne die Daten in eine Datenträgerdatei zu schreiben, indem Sie die [**WM \_ CAP SEQUENCE \_ \_ NOFILE-Meldung**](wm-cap-sequence-nofile.md) (oder das [**CapCaptureSequenceNoFile-Makro)**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) verwenden. Diese Meldung ist nur in Verbindung mit Rückruffunktionen nützlich, die es Ihrer Anwendung ermöglichen, die Video- und Audiodaten direkt zu verwenden. Beispielsweise können Videoconferencing-Anwendungen diese Nachricht verwenden, um Streamingvideoframes abzurufen. Die Rückruffunktionen übertragen die erfassten Bilder auf den Remotecomputer.

 

 




