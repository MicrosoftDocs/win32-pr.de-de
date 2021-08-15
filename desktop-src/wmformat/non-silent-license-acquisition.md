---
title: Nicht automatischer Lizenzerwerb
description: Nicht automatischer Lizenzerwerb
ms.assetid: 3b3fce53-9202-4e55-82d5-7c70ea833087
keywords:
- Windows Media Format SDK, nicht automatischer Lizenzerwerb
- Windows Medienformat-SDK, Lizenzen
- Digital Rights Management (DRM), nicht automatischer Lizenzerwerb
- DRM (Digital Rights Management), nicht automatischer Lizenzerwerb
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Erweiterte DRM-Client-APIs, nicht automatischer Lizenzerwerb
- Erweiterte Client-APIs, nicht automatischer Lizenzerwerb
- Nicht automatischer Lizenzerwerb
- Lizenzen,nicht automatischer Lizenzerwerb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92c9350e429a1fe4b6218878d2211b355c1569b39284161f9f3abceac1afc6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846434"
---
# <a name="non-silent-license-acquisition"></a>Nicht automatischer Lizenzerwerb

Der nicht automatische Lizenzerwerb ermöglicht dem Lizenzanbieter die Interaktion mit dem Endbenutzer über eine Webseite als Zwischenschritt im Lizenzerwerbsprozess. Der nicht automatische Lizenzerwerb wird als Reaktion auf einen Benutzer initiiert, der versucht, auf geschützte Inhalte zu zugreifen.

Führen Sie die folgenden Schritte aus, um einen nicht automatischen Lizenzerwerb durchzuführen:

1.  Rufen Sie [**die IWMDRMLicenseManagement::AcquireLicense-Methode**](iwmdrmlicensemanagement-acquirelicense.md) auf. Übergeben Sie den DRM-Header aus der geschützten Datei als *bstrHeaderData-Parameter.* Geben Sie an, welche Rechte die Lizenz im *bstrActions-Parameter gewähren* soll. Legen Sie abschließend den *dwFlags-Parameter* auf WMDRM \_ ACQUIRE LICENSE \_ \_ NONSILENT fest.
2.  Fangen Sie Ereignisse für **die IWMDRMLicenseManagement-Schnittstelle** ab. Wenn Sie das **MeWMDRMLicenseAcquisitionCompleted-Ereignis** erhalten, rufen Sie den zugeordneten Wert ab, indem Sie **DEN WERT FÜR DAS MEDIENEREIGNIS::GetValue aufrufen.** Der Wert sollte vom Typ VT \_ UNKNOWN sein, ein Zeiger auf eine **IUnknown-Schnittstelle.**
3.  Rufen Sie **die QueryInterface-Methode** der **IUnknown-Schnittstelle** auf, die in Schritt 2 abgerufen wurde, um die [**IWMDRMNonSilentLicenseAquisition-Schnittstelle abzurufen.**](iwmdrmnonsilentlicenseaquisition.md)
4.  Rufen [**Sie IWMDRMNonSilentLicenseAquisition::GetCwiedergabege**](iwmdrmnonsilentlicenseaquisition-getchallenge.md) auf, um die Lizenzanforderung abzurufen. Rufen Sie [**auch IWMDRMNonSilentLicenseAquisition::GetURL**](iwmdrmnonsilentlicenseaquisition-geturl.md) auf, wenn Sie noch nicht über die URL des Lizenzservers verfügen.
5.  Senden Sie die Herausforderung an die webseite, die durch die URL angegeben wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erwerben von Lizenzen**](acquiring-licenses.md)
</dt> <dt>

[**Verwenden des Media Foundation-Ereignismodells**](using-the-media-foundation-model.md)
</dt> </dl>

 

 




