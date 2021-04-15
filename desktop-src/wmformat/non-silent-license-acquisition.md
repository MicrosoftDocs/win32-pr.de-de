---
title: Nicht automatische Lizenz Beschaffung
description: Nicht automatische Lizenz Beschaffung
ms.assetid: 3b3fce53-9202-4e55-82d5-7c70ea833087
keywords:
- Windows Media-Format-SDK, nicht automatischer Lizenzerwerb
- Windows Media-Format-SDK, Lizenzen
- Digital Rights Management (DRM), nicht automatische Lizenz Beschaffung
- DRM (Digital Rights Management), nicht automatische Lizenz Beschaffung
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Erweiterte APIs für den DRM-Client, nicht automatische Lizenz Beschaffung
- Erweiterte Client-APIs, nicht automatische Lizenz Beschaffung
- nicht automatische Lizenz Beschaffung
- Lizenzen, nicht automatische Lizenz Beschaffung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb8d7c4865e74fd5ce383cff8317de905828afe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516058"
---
# <a name="non-silent-license-acquisition"></a>Nicht automatische Lizenz Beschaffung

Der nicht automatische Lizenz Abruf ermöglicht dem Lizenz Anbieter die Interaktion mit dem Endbenutzer über eine Webseite als Zwischenschritt im Lizenz Erwerbs Vorgang. Der nicht automatische Lizenzerwerb wird als Reaktion auf einen Benutzer initiiert, der versucht, auf geschützte Inhalte zuzugreifen.

Führen Sie die folgenden Schritte aus, um einen nicht automatischen Lizenzerwerb durchzuführen:

1.  Nennen Sie die [**iwmdrmlicenabmanagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) -Methode. Übergeben Sie den DRM-Header aus der geschützten Datei als *bstrinheaderdata* -Parameter. Geben Sie an, welche Rechte von der Lizenz im *bstractions* -Parameter erteilt werden sollen. Legen Sie abschließend den *dwFlags* -Parameter auf "WMDRM-Lizenz abrufen" nicht automatisch fest \_ \_ \_ .
2.  Trap Ereignisse für die **iwmdrmlicentsmanagement** -Schnittstelle. Wenn Sie das **mewmdrmlicenabacquisitionabgeschlossene** -Ereignis empfangen, rufen Sie den zugehörigen Wert durch Aufrufen von **imfmediaevent:: GetValue** ab. Der Wert muss vom Typ "VT \_ unknown" sein, einem Zeiger auf eine **IUnknown** -Schnittstelle.
3.  Nennen Sie die **QueryInterface** -Methode der **IUnknown** -Schnittstelle, die Sie in Schritt 2 abgerufen haben, um die [**iwmdrmnonsilentlicenseaquisition**](iwmdrmnonsilentlicenseaquisition.md) -Schnittstelle abzurufen.
4.  Rufen Sie [**iwmdrmnonsilentlicenseaquisition:: getchallenge**](iwmdrmnonsilentlicenseaquisition-getchallenge.md) auf, um die Lizenz Herausforderung abzurufen. Nennen Sie auch [**iwmdrmnonsilentlicenseaquisition:: getURL**](iwmdrmnonsilentlicenseaquisition-geturl.md) , wenn Sie nicht bereits über die URL des Lizenzservers verfügen.
5.  Sendet die Abfrage an die durch die URL angegebene Webseite.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erwerben von Lizenzen**](acquiring-licenses.md)
</dt> <dt>

[**Verwenden des Media Foundation-Ereignis Modells**](using-the-media-foundation-model.md)
</dt> </dl>

 

 




