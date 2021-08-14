---
title: Abrufen von Streamkonfigurationsinformationen von Codecs
description: Abrufen von Streamkonfigurationsinformationen von Codecs
ms.assetid: 76c734a1-6fe4-4958-8773-a65f5ced80c6
keywords:
- Streams, Konfigurationen von Codecs
- Codecs, Abrufen von Streamkonfigurationen aus
- Streams, Codecformate
- Codecs, Formate
- streams,IWMCodecInfo-Schnittstelle
- IWMCodecInfo, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10cd131bfd263e0e9a0616b6fa9b59b3f3b03ace30a199b8b79f8b3c3f3f09f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433866"
---
# <a name="getting-stream-configuration-information-from-codecs"></a>Abrufen von Streamkonfigurationsinformationen von Codecs

Für Audio- und Videostreams, die die Windows Medienaudio- und Videocodecs verwenden, sollten Sie die Werte für die Streamkonfigurationsstrukturen aus dem Codec abrufen, den Sie verwenden möchten. Obwohl es möglich ist, diese Werte selbst festzulegen, stellt die Verwendung der Codecs sicher, dass die Werte korrekt sind. Sie sollten die Werte in diesen Strukturen nur ändern, wenn in der Dokumentation ausdrücklich eine bestimmte Änderung empfohlen wird.

Informationen aus den Codecs werden in Form von Codecformaten übermittelt. Jedes Codecformat ist ein einzelnes Streamformat, das vom Codec unterstützt wird. Weitere Informationen zu Streamformaten finden Sie unter [Formate.](formats.md)

Sie können Informationen von den Windows Media-Codecs anfordern, indem Sie die Schnittstellen [**IWMCodecInfo,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo) [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)und [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) des Profil-Manager-Objekts verwenden. Um die [**IWMProfileManager-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) eines Profil-Manager-Objekts abzurufen, rufen Sie die [**WMCreateProfileManager-Funktion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) auf. Rufen Sie **QueryInterface** auf **IWMProfileManager** auf, um **IWMCodecInfo3** abzurufen.

In den folgenden Abschnitten wird beschrieben, wie Sie die benötigten Informationen abrufen.



| `Section`                                                                                                | BESCHREIBUNG                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [So aufzählen Sie alle installierten Windows Mediencodecs](to-enumerate-all-installed-windows-media-codecs.md) | Beschreibt, wie die Methoden der **IWMCodecInfo-** und **IWMCodecInfo2-Schnittstellen** verwendet werden, um den Namen und Codecindex jedes installierten Windows Media-Codecs abzurufen. |
| [So aufzählen Sie Codecformate](to-enumerate-codec-formats.md)                                           | Beschreibt, wie Sie Datenstromkonfigurationsobjekte aus Codecs abrufen, um sie in Ihren Profilen zu verwenden.                                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konfigurieren von Streams**](configuring-streams.md)
</dt> </dl>

 

 




