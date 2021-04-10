---
description: Evrpresenter-Beispiel
ms.assetid: 791a9816-4c40-4683-8b32-22f73d7fe84d
title: Evrpresenter-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bde85de152c41f348b1aae74a8c0d67ca746cab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127889"
---
# <a name="evrpresenter-sample"></a>Evrpresenter-Beispiel

Zeigt, wie ein benutzerdefinierter Presenter für den [erweiterten Videorenderer](enhanced-video-renderer.md) (EVR) implementiert wird. Der benutzerdefinierte Presenter kann entweder mit dem DirectShow-EVR-Filter oder der Microsoft Media Foundation EVR-Senke verwendet werden.

## <a name="apis-demonstrated"></a>Gezeigte APIs

In diesem Beispiel werden die folgenden Media Foundation Schnittstellen veranschaulicht:

-   [**IMF-staatink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [**Imfratesupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [**Imftopologyservicelookupclient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient)
-   [**IMF videoabviceid**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)
-   [**IMF videodisplaycontrol**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)
-   [**IMF videopresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)

## <a name="usage"></a>Verbrauch

Das Ereignis evrpresenter erstellt eine DLL, bei der es sich um einen com-Server für den Presenter handelt. Bevor Sie den benutzerdefinierten Presenter verwenden, müssen Sie die dll registrieren.

So verwenden Sie dieses Beispiel in Media Foundation:

1.  Erstellen Sie das Beispiel.
2.  Regsvr32-EvrPresenter.dll.
3.  Erstellen Sie das [MF Player-Beispiel](/previous-versions//bb970516(v=vs.85))und führen Sie es aus.
4.  Wählen Sie im Menü **Datei** die Option Datei **Öffnen** aus.
5.  Wählen Sie im Dialogfeld **Datei öffnen** die Option **Custom EVR Presenter aus.**
6.  Wählen Sie eine Datei für die Wiedergabe aus.

So verwenden Sie dieses Beispiel in DirectShow:

1.  Erstellen Sie das Beispiel.
2.  Registrieren Sie EvrPresenter.dll.
3.  Erstellen Sie das Beispiel evrplayer, und führen Sie es aus. Dieses Beispiel ist in den DirectShow-Beispielen in der Windows SDK enthalten.
4.  Wählen Sie im Menü **Datei** die Option **EVR Presenter** aus.
5.  Wählen Sie eine Datei für die Wiedergabe aus.

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist im [GitHub-Repository für klassische Windows-Beispiele](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip)verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterter Videorenderer](enhanced-video-renderer.md)
</dt> <dt>

[Schreiben von EVR Presenter](how-to-write-an-evr-presenter.md)
</dt> <dt>

[Media Foundation-SDK-Beispiele](media-foundation-sdk-samples.md)
</dt> </dl>

 

 
