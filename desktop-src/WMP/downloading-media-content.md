---
title: Herunterladen von Medieninhalten
description: Herunterladen von Medieninhalten
ms.assetid: 0a057e13-6e0c-4a8f-9cab-051183e6b222
keywords:
- Windows Media Player von Onlineshops,Herunterladen von Medieninhalten
- Onlineshops,Herunterladen von Medieninhalten
- Geben Sie 1 Onlineshops ein, und laden Sie Medieninhalte herunter.
- Windows Media Player online stores,media content downloading (Herunterladen von Medieninhalten)
- Onlineshops,Herunterladen von Medieninhalten
- 'Typ 1: Onlineshops,Herunterladen von Medieninhalten'
- Medieninhalt,Herunterladen
- Herunterladen von Medieninhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a314dc4b59966fd779660a2c1ab26fc2b37d413e4add068f936a6109acd423a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997030"
---
# <a name="downloading-media-content"></a>Herunterladen von Medieninhalten

Windows Media Player verarbeitet Downloads von Musikdatei für den Onlineshop. Ein Download kann initiiert werden, wenn die Ermittlungsseite [External.download](external-download.md) aufruft oder der Benutzer im Player auswählt, um eine Reihe von Spuren herunterzuladen. In beiden Fällen ruft Windows Media Player [IWMPContentPartner::D ownload](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download)auf und überspringt eine Inhaltscontainerliste, die den Satz der herunterzuladenden Spuren beschreibt, und ein Cookie, das die Downloadtransaktion darstellt. Das Inhaltspartner-Plug-In muss dann für jede Spur im Satz [einmal IWMPContentPartnerCallback::D ownloadTrack](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-downloadtrack) aufrufen. Wenn das Plug-In **DownloadTrack aufruft,** übergibt es **ein HRESULT** im *parameter hrDownload.* Wenn das Plug-In in *hrDownload* einen Erfolgscode übergibt, Windows Media Player die Spur herunter. Wenn das Plug-In in *hrDownload* einen Fehlercode übergibt, wird die Spur vom Player nicht heruntergeladen. Für jeden **Downloadaufruf muss** das Plug-In das Transaktionscookie und die ID der jeweiligen Spur liefern. Für Spuren, die tatsächlich heruntergeladen werden, muss das Plug-In auch die URL der Spur angeben.

Nachdem eine Datei heruntergeladen wurde, Windows Media Player die Bibliothek automatisch entsprechend der neu erworbenen Musik aktualisiert. Der Player stellt dem Plug-In Statusinformationen zum Downloadvorgang bereit, indem [er IWMPContentPartner::D ownloadTrackComplete aufruft.](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-downloadtrackcomplete) Bei dieser Methode stellt der Player ein **HRESULT** bereit, um den Erfolg oder Fehler des Downloads, die Track-ID und die benutzerdefinierte Parameterzeichenfolge anzugeben, die der Onlineshop beim Aufrufen von **DownloadTrack bereitgestellt hat.**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierhandbuch für Onlineshops vom Typ 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




