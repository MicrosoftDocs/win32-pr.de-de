---
description: PMP-Mediensitzung
ms.assetid: CF3A427D-31D2-45FF-BE87-F192B758204E
title: PMP-Mediensitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 683bc6d3dcc78bfb18daedabab614c95c33492fb7e17d48cbe7f6f08bdc766ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118239207"
---
# <a name="pmp-media-session"></a>PMP-Mediensitzung

Eine Anwendung kann die [Mediensitzung](media-session.md) in einem separaten Prozess erstellen, der als PMP-Prozess [(Protected Media Path)](protected-media-path.md) bezeichnet wird. Der Hauptzweck des PMP-Prozesses besteht darin, die Wiedergabe geschützter Inhalte mithilfe von DRM (Digital Rights Management) zu ermöglichen. Standardmäßig wird der PMP-Prozess in einer geschützten Umgebung (Protected Environment, PE) erstellt. Nur vertrauenswürdige, signierte Komponenten können innerhalb eines PE geladen werden. Ein sekundärer Vorteil des PMP-Prozesses besteht darin, dass der Anwendungsprozess von der Medienpipeline isoliert wird. Weitere Informationen zum PMP-Prozess finden Sie unter [Protected Media Path](protected-media-path.md).

Um die Mediensitzung innerhalb des PMP-Prozesses zu erstellen, rufen Sie die [**MFCreatePMPMediaSession-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) auf. Optional können Sie das **MFPMPSESSION \_ UNPROTECTED \_ PROCESS-Flag** übergeben. Wenn dieses Flag festgelegt ist, wird der PMP-Prozess in einem nicht geschützten Prozess und nicht in einem PE-Prozess erstellt. Der ungeschützte Prozess kann nicht für die DRM-Wiedergabe verwendet werden, bietet ihnen jedoch die Vorteile der Prozessisolation.

Die [**MFCreatePMPMediaSession-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) gibt einen Zeiger auf ein Proxyobjekt für die Mediensitzung zurück. Die Anwendung kommuniziert über den Proxy mit der Mediensitzung.

![Abbildung der Mediensitzung im pmp-Prozess](images/pmp01.png)

Wenn die Anwendung eine Topologie erstellt, wird standardmäßig die Medienquelle im Anwendungsprozess erstellt. Im PMP-Prozess wird ein Proxy für die Medienquelle erstellt. Die Medienquelle kann Objekte innerhalb des PMP-Prozesses mithilfe der [**IMFPMPHost-Schnittstelle**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) erstellen. Um beispielsweise DRM zu unterstützen, erstellt eine Medienquelle ein Objekt, das als *Eingabevertrauensstellungsstelle (Input Trust Authority,* ITA) bezeichnet wird. Der ITA muss innerhalb des PMP-Prozesses erstellt werden. (Weitere Informationen zu ITAs finden Sie unter [Pfad zu geschützten Medien.)](protected-media-path.md) Gehen Sie wie folgt vor, um die [**IMFPMPHost-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) zu verwenden:

1.  Die Medienquelle muss die [**IMFPMPClient-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpclient) implementieren.
2.  Während der Topologieauflösung ruft der Mediensitzungsproxy die [**IMFPMPClient::SetPMPHost-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfpmpclient-setpmphost) für die Medienquelle auf.
3.  Die Medienquelle ruft [**IMFPMPHost::CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) auf, um das Objekt innerhalb des PMP-Prozesses zu erstellen. Das -Objekt muss über eine registrierte CLSID verfügen. Darüber hinaus muss das Objekt vertrauenswürdig und digital signiert sein, um es innerhalb des PE zu laden. Informationen zum Signieren geschützter Medienkomponenten finden Sie im Whitepaper [Codesignierung für Komponenten geschützter Medien in Windows Vista.](/windows-hardware/test/hlk/)

Die folgende Abbildung zeigt die im Anwendungsprozess erstellte Medienquelle.

![Abbildung einer Medienquelle im Anwendungsprozess.](images/pmp02.png)

Eine weitere Alternative besteht darin, die Medienquelle innerhalb der PMP-Sitzung zu erstellen.

1.  Legen Sie das [**MF SESSION REMOTE SOURCE \_ \_ \_ \_ MODE-Attribut**](mf-session-remote-source-mode-attribute.md) fest, wenn Sie die Mediensitzung erstellen. Konfigurationsattribute werden im *pConfiguration-Parameter* der [**MFCreatePMPMediaSession-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) angegeben.
2.  Rufen Sie [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) in der Mediensitzung auf, um einen Zeiger auf die [**IMFPMPHost-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) abzurufen. Der Dienstbezeichner ist **MF \_ PMP \_ SERVICE.**
3.  Rufen Sie [**IMFPMPHost::CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) mit dem Klassenbezeichner **CLSID \_ MFSourceResolver** auf, um den Quellresolver innerhalb des PMP-Prozesses zu erstellen. Die -Methode gibt einen Zeiger auf einen Proxy für den Quell resolver zurück.
4.  Rufen Sie ZUM Erstellen der Medienquelle [**DIE DATEI AUFSOURCEResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) oder [**EINENSOURCEResolver::BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) auf.
    > [!Note]  
    > In diesem Fall müssen Sie die asynchronen Versionen dieser Methoden verwenden, da die synchronen Versionen nicht remotable sind.

     

Die folgende Abbildung zeigt die im PMP-Prozess erstellte Medienquelle.

![Abbildung einer Medienquelle im pmp-Prozess.](images/pmp03.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Wiedergeben geschützter Mediendateien](how-to-play-protected-media-files.md)
</dt> <dt>

[Mediensitzung](media-session.md)
</dt> <dt>

[Pfad zu geschützten Medien](protected-media-path.md)
</dt> </dl>

 

 
