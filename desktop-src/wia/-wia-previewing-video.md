---
description: Die iwiavideo-Schnittstelle ermöglicht einer Anwendung, Videos anzuzeigen und Bilder daraus zu erfassen.
ms.assetid: 59eddbdc-4957-44be-a602-0763f3385e89
title: Anzeigen einer Vorschau für Videos (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 935625c1c16ceea66326963185dd75d96d98ed02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526429"
---
# <a name="previewing-video-wia"></a>Anzeigen einer Vorschau für Videos (WIA)

Die [**iwiavideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) -Schnittstelle ermöglicht einer Anwendung, Videos anzuzeigen und Bilder daraus zu erfassen. Führen Sie die folgenden Schritte aus, um das streamingvideogerät auszuwählen und einen Videostream in einem Fenster anzuzeigen.

-   Rufen Sie [cokreateinstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um einen Zeiger auf die [**iwiadevmgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) -Schnittstelle abzurufen.
-   Verwenden Sie die [**iwiadevmgr:: enumdeviceinfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) -Methode der [**iwiadevmgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) -Schnittstelle, um einen Zeiger auf die [**ienumwia \_ dev \_ Info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) -Schnittstelle zu erhalten. Anweisungen zum Auflisten von Geräten finden Sie unter Auflisten von System Geräten.
-   Verwenden Sie die [**ienumwia \_ dev \_ Info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) -Schnittstelle zum Abrufen eines [**iwiapropertystorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) -Schnittstellen Zeigers für jedes gefundene Windows-Abbild Erfassungsgerät (WIA).
-   Verwenden Sie die [**iwiapropertystorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) -Schnittstelle, um die Eigenschaft "tviceid" des gewünschten Geräts zu erhalten. Ein streamingvideogerät verfügt über das Flag stidevicetyetstreamingvideo der Eigenschaft WIA \_ DIP \_ dev \_ Type.
-   Verwenden Sie die [**iwiapropertystorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) -Schnittstelle zum Aufrufen des \_ \_ \_ Verzeichnis Eigenschafts Werts WIA DPV Images.
-   Rufen Sie [cokreateinstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um einen Zeiger auf die [**iwiavideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) -Schnittstelle abzurufen.
-   Legen Sie die [**iwiavideo:: imagesdirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) -Eigenschaft der [**iwiavideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) -Schnittstelle auf den Wert fest, der vom \_ Wert des \_ \_ Verzeichnis Eigenschafts Werts WIA-DPV-Images empfangen wird.
-   Nennen Sie [**iwiavideo:: kreatevideobywiadevid**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-createvideobywiadevid) auf der [**iwiavideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) -Schnittstelle, und übergeben Sie dabei die Geräte-ID des streamingbildgeräts und den Handle des Fensters, in dem das Video angezeigt werden soll.

> [!Note]  
> WIA unterstützt keine Videogeräte in Windows Server 2003, Windows Vista oder höher. Verwenden Sie für diese Versionen von Windows [DirectShow](/previous-versions//ms783323(v=vs.85)) zum Abrufen von Bildern aus Videos.

 

 

 
