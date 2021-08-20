---
title: Multimediadatei-E/A-Referenz
description: Multimediadatei-E/A-Referenz
ms.assetid: 1f24432e-7407-4b97-80ab-0a0c40c09253
keywords:
- Windows Multimedia,Datei-E/A-Referenz
- Multimedia,Datei-E/A-Referenz
- Multimediaeingabe, Datei-E/A-Referenz
- Multimediadatei-E/A, Referenz
- Datei-E/A, Referenz
- Eingabe und Ausgabe (E/A), Referenz
- E/A (Eingabe und Ausgabe), Referenz
- Referenz zu Multimediadatei-E/A,About
- Multimediadatei-E/A-Referenz,About
- Datei-E/A-Referenz,About
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06d61b06c16b12a9276adc0d858a3170dae2f7d636cc63a9ac6cc032a65c978c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136901"
---
# <a name="multimedia-file-io-reference"></a>Multimediadatei-E/A-Referenz

In diesem Abschnitt werden die Funktionen, Makros, Meldungen und Strukturen beschrieben, die der Eingabe und Ausgabe von Multimediadateien zugeordnet sind. Diese Elemente sind wie folgt gruppiert.

## <a name="basic-io"></a>Grundlegende E/A

-   [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose)
-   [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)
-   [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread)
-   [**mmioRename**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename)
-   [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek)
-   [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite)

## <a name="buffered-io"></a>Gepufferte E/A

-   [**mmioAdvance**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioadvance)
-   [**mmioFlush**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioflush)
-   [**mmioGetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo)
-   [**MMIOINFO**](/previous-versions//dd757322(v=vs.85))
-   [**mmioSetBuffer**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer)
-   [**mmioSetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo)

## <a name="riff-io"></a>ORGANISATIONS-E/A

-   [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend)
-   [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo)
-   [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk)
-   [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend)
-   [**mmioFOURCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc)
-   [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc)

## <a name="custom-io-procedures"></a>Benutzerdefinierte E/A-Prozeduren

-   [**IOProc**](/previous-versions//dd757098(v=vs.85))
-   [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)
-   [**MMIOM \_ CLOSE**](mmiom-close.md)
-   [**MMIOM \_ OPEN**](mmiom-open.md)
-   [**MMIOM \_ READ**](mmiom-read.md)
-   [**\_MMIOM-UMBENENNUNG**](mmiom-rename.md)
-   [**MMIOM \_ SEEK**](mmiom-seek.md)
-   [**MMIOM \_ WRITE**](mmiom-write.md)
-   [**MMIOM \_ WRITEFLUSH**](mmiom-writeflush.md)
-   [**mmioSendMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Multimediadatei-E/A](multimedia-file-i-o.md)
</dt> </dl>

 

 