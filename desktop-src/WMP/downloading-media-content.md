---
title: Herunterladen von Medieninhalten
description: Herunterladen von Medieninhalten
ms.assetid: 0a057e13-6e0c-4a8f-9cab-051183e6b222
keywords:
- Windows Media Player Online Stores, Herunterladen von Medieninhalten
- Online Stores, Herunterladen von Medieninhalten
- Typ 1 Online Stores, Herunterladen von Medieninhalten
- Windows Media Player Online Stores, Herunterladen von Medieninhalten
- Online Stores, Herunterladen von Medieninhalten
- Typ 1 Online Stores, Herunterladen von Medieninhalten
- Medieninhalt, herunterladen
- Herunterladen von Medieninhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00efe44f2bac25a9eeda86f6adcc78b34beea7cd
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "104390044"
---
# <a name="downloading-media-content"></a>Herunterladen von Medieninhalten

Windows Media Player verarbeitet Musikdateien für den Online Shop. Ein Download kann initiiert werden, wenn auf der Ermittlungs Seite " [extern. Download](external-download.md) " aufgerufen wird oder wenn der Benutzer im Player eine Gruppe von Spuren herunterlädt. In beiden Fällen ruft Windows Media Player [iwmpcontentpartner::D ownload](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download)auf und übergibt eine Inhalts Container Liste, die den Satz der herunter zuladenden Abrufe beschreibt, und ein Cookie, das die Download Transaktion darstellt. Das Content Partner-Plug-in muss dann [iwmpcontentpartnercallback::D ownloadtrack](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-downloadtrack) für jede Spur im Satz einmal aufruft. Wenn das Plug-in **downloadtrack** aufruft, übergibt es ein **HRESULT** in den *hrdownload* -Parameter. Wenn das Plug-in einen Erfolgs Code in *hrdownload* übergibt, lädt Windows Media Player die Nachverfolgung herunter. Wenn das Plug-in einen Fehlercode in *hrdownload* übergibt, wird der Titel nicht vom Player heruntergeladen. Für jeden **Download Download** muss das Plug-in das Transaktions Cookie und die ID des fraglichen Titels bereitstellen. Bei nachverfolgen, die tatsächlich heruntergeladen werden, muss das Plug-in auch die URL des Titels bereitstellen.

Nachdem eine Datei heruntergeladen wurde, wird die Bibliothek von Windows Media Player automatisch aktualisiert, um die neu erworbene Musik widerzuspiegeln. Der Player stellt dem Plug-in über den Downloadvorgang Statusinformationen zur Verfügung, indem [iwmpcontentpartner::D ownloadtrackcomplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-downloadtrackcomplete)aufgerufen wird. Bei dieser Methode stellt der Player ein **HRESULT** bereit, um den Erfolg oder Misserfolg des Downloads, die Spur-ID und die Zeichenfolge der benutzerdefinierten Parameter anzugeben, die der Online Shop beim Aufrufen von **downloadtrack** bereitgestellt hat.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmier Handbuch für den Typ 1 Online Stores**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




