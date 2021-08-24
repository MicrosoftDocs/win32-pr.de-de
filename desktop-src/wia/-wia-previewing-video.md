---
description: Mit der IWiaVideo-Schnittstelle kann eine Anwendung Videos anzeigen und stille Bilder daraus erfassen.
ms.assetid: 59eddbdc-4957-44be-a602-0763f3385e89
title: Videovorschau (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca270adf4e6461beac409315c782101744e8afeb72c33f07aa7bbc999e24751
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813720"
---
# <a name="previewing-video-wia"></a>Videovorschau (WIA)

Mit [**der IWiaVideo-Schnittstelle**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) kann eine Anwendung Videos anzeigen und stille Bilder daraus erfassen. Führen Sie die folgenden Schritte aus, um das Streamingvideogerät auszuwählen und einen Videostream in einem Fenster anzuzeigen.

-   Rufen [Sie CoCreateInstance auf,](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) um einen Zeiger auf die [**IWiaDevMgr-Schnittstelle**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) abzurufen.
-   Verwenden Sie die [**IWiaDevMgr::EnumDeviceInfo-Methode**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) der [**IWiaDevMgr-Schnittstelle,**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) um einen Zeiger auf die [**IEnumWIA \_ DEV \_ INFO-Schnittstelle**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) zu erhalten. Anweisungen zum Aufzählen von Geräten finden Sie unter Aufzählen von Systemgeräten.
-   Verwenden Sie die [**IEnumWIA \_ DEV \_ INFO-Schnittstelle,**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) um einen [**IWiaPropertyStorage-Schnittstellenzeiger**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) für jedes gefundene WIA-Gerät (Windows Image Acquisition) zu erhalten.
-   Verwenden Sie [**die IWiaPropertyStorage-Schnittstelle,**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) um die DeviceID-Eigenschaft des gewünschten Geräts zu erhalten. Ein Streamingvideogerät verfügt über das Flag StiDeviceTypeStreamingVideo der WIA \_ DIP \_ DEV \_ TYPE-Eigenschaft.
-   Verwenden Sie [**die IWiaPropertyStorage-Schnittstelle,**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) um den WIA \_ DPV \_ IMAGES \_ DIRECTORY-Eigenschaftswert zu erhalten.
-   Rufen [Sie CoCreateInstance auf,](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) um einen Zeiger auf die [**IWiaVideo-Schnittstelle**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) abzurufen.
-   Legen Sie [**die IWiaVideo::ImagesDirectory-Eigenschaft**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) der [**IWiaVideo-Schnittstelle**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) auf den Wert fest, der vom WIA \_ DPV \_ IMAGES \_ DIRECTORY-Eigenschaftswert empfangen wird.
-   Rufen [**Sie IWiaVideo::CreateVideoByWiaDevID**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-createvideobywiadevid) auf der [**IWiaVideo-Schnittstelle**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) auf, und übergeben Sie dabei die Geräte-ID des Streamingbildgeräts und das Handle des Fensters, in dem das Video angezeigt werden soll.

> [!Note]  
> WIA unterstützt keine Videogeräte in Windows Server 2003, Windows Vista oder höher. Verwenden Sie für diese Versionen Windows [DirectShow,](/previous-versions//ms783323(v=vs.85)) um Bilder aus Videos zu erhalten.

 

 

 
