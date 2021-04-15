---
description: In diesem Thema wird beschrieben, wie eine Direct3D-fähige Media Foundation Transformation (MFT) für Video implementiert wird.
ms.assetid: 8ec7e678-8477-41fa-9726-54df5ed187cd
title: Direct3D-Aware-MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad50438250c0ee1627cc20aebb49262ec8eec9ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524560"
---
# <a name="direct3d-aware-mfts"></a>Direct3D-Aware-MFTs

In diesem Thema wird beschrieben, wie eine *Direct3D-fähige* Media Foundation Transformation (MFT) für Video implementiert wird.

Ein Video-MFT wird als *Direct3D* angesehen, wenn er Beispiele verarbeiten kann, die Direct3D-Oberflächen enthalten. Der typische Grund für die Unterstützung von Direct3D in einer Video-MFT besteht darin, die hardwarebeschleunigte Decodierung mithilfe der DirectX-Videobeschleunigung (DXVA) zu ermöglichen.

In diesem Thema werden die Schritte beschrieben, die erforderlich sind, um die MFT-Direct3D zu unterstützen. Dieses Thema behandelt nicht die Mechanismen der DXVA-Decodierung. Weitere Informationen zu DXVA finden Sie unter [DirectX-Video Beschleunigung 2,0](directx-video-acceleration-2-0.md).

> [!IMPORTANT]
> Ab Windows 8 kann [**imsdxgidevicemanager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) anstelle von [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)verwendet werden. Für Windows Store-Apps müssen Sie **IMF dxgidevicemanager** und Microsoft Direct3D 11 verwenden. Weitere Informationen finden Sie in den [Video-APIs Direct3D 11](direct3d-11-video-apis.md).

 

1.  Implementieren Sie die [**IMF Transform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) -Methode. Diese Methode gibt einen Zeiger auf einen Attribut Speicher zurück.
2.  Der MFT muss den Wert des [**\_ \_ D3D \_**](mf-sa-d3d-aware-attribute.md) -Attributs der MF-Eigenschaft auf " **true** " in seinem eigenen Attribut Speicher festlegen. Bei Verwendung von Direct3D 11 wird ab Windows 8 die Verwendung von [MF \_ sa \_ D3D11 \_ ](mf-sa-d3d11-aware.md)unterstützt.
3.  Wenn beim Formatieren von Formaten das Attribut [**MF \_ sa \_ D3D \_ Aware**](mf-sa-d3d-aware-attribute.md) (oder [MF \_ sa \_ D3D11 \_ Aware](mf-sa-d3d11-aware.md) If using Direct3D 11) den Wert **true** hat, sendet der Client möglicherweise die [**MFT- \_ Nachrichten \_ Satz \_ D3D \_ Manager**](mft-message-set-d3d-manager.md) -Nachricht an die MFT. Der *ulparam* -Ereignis Parameter ist ein Zeiger auf die [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) -Schnittstelle. Ab Windows 8 können Sie [**IMF dxgidevicemanager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) anstelle von **IDirect3DDeviceManager9** verwenden. Der Client muss diese Nachricht nicht senden.
4.  Der MFT ruft [**IDirect3DDeviceManager9:: getvideoservice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) auf, um den benötigten DXVA-Dienst abzufragen. Ab Windows 8, wenn [**imfdxgidevicemanager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) verwendet wurde, ruft der MFT [**imfdxgidevicemanager:: getvideoservice**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-getvideoservice)auf. In der Regel würde ein Decoder [**idirectxvideodecoderservice**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice)Abfragen, und ein Videoprozessor würde [**idirectxvideoprocess orservice**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice)Abfragen.
5.  Wenn der vorherige Schritt erfolgreich ausgeführt wurde, müssen die Methoden [**imftransform:: getinputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) und [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) DXVA-kompatible Formate zurückgeben.
6.  Der Client konfiguriert die Medientypen auf dem MFT. Wenn ein Medientyp nicht mit DXVA kompatibel ist, muss der MFT den Fehlercode **MF \_ E \_ nicht unterstützten \_ D3D- \_ Typ** zurückgeben.
7.  Zu diesem Zeitpunkt gibt es zwei Optionen, abhängig davon, ob der Client ein geeignetes DXVA-Format findet.
    -   Wenn der Client ein DXVA-Format erfolgreich konfiguriert hat, kann er mit der Verarbeitung beginnen. An diesem Punkt kann die MFT DXVA zur Verarbeitung verwenden oder auf die Software Verarbeitung zurückgreifen.
    -   Wenn der Client jedoch kein akzeptables DXVA-Format findet, sendet der Client möglicherweise eine weitere [**MFT \_ Message \_ Set \_ D3D \_ Manager**](mft-message-set-d3d-manager.md) -Nachricht, bei der *ulparam* auf **null** festgelegt wird. Der MFT muss den [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) -Zeiger ( [**imfdxgidevicemanager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) -Zeiger, wenn **imfdxgidevicemanager** verwendet wurde) und alle anderen DXVA-Schnittstellen freigeben und die Software Verarbeitung wiederherstellen. An diesem Punkt darf die MFT die DXVA-Verarbeitung nicht verwenden.

Ein Direct3D-MFT muss darauf vorbereitet sein, Beispiele zu verarbeiten, die eine Direct3D-Oberfläche enthalten. Das Beispiel enthält genau einen Medien Puffer. Um die Direct3D-Oberfläche aus dem Puffer abzurufen, müssen Sie die [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) -Funktion aufrufen und den Dienst " **Mr- \_ Puffer \_ Dienst** " angeben. Weitere Informationen finden Sie unter [DirectX-Oberflächen Puffer](directx-surface-buffer.md).

Ein MFT, der DXVA verwendet, muss seine eigenen Ausgabe Beispiele wie folgt zuordnen:

1.  Legen Sie in der [**imftransform:: getoutputstreaminfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) -Methode fest, dass der **MFT- \_ Ausgabestream ein \_ \_ \_ Samples** -Flag enthält.
2.  Erstellen Sie einen Pool mit DXVA-Oberflächen, wie in der DXVA-Spezifikation beschrieben.
3.  Erstellen Sie Medien Beispiele, indem Sie [**mfcreatevideosamplefromsurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface)aufrufen.

Die MFT sollte die Software Verarbeitung immer als Fallback unterstützen, da die DXVA-Verarbeitung möglicherweise aus verschiedenen Gründen nicht verfügbar ist:

-   DXVA wird von der GPU möglicherweise nicht unterstützt.
-   Der Client verwendet möglicherweise nicht Direct3D.
-   DXVA-Profile sind nicht für jedes Videoformat definiert.

Ein Direct3D-MFT muss über einen einzelnen Ausgabestream verfügen. Es können nicht mehrere Ausgaben vorhanden sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben eines benutzerdefinierten MFT](writing-a-custom-mft.md)
</dt> </dl>

 

 



