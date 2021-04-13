---
title: Informationen zu streamkonfigurations Informationen von Codecs
description: Informationen zu streamkonfigurations Informationen von Codecs
ms.assetid: 76c734a1-6fe4-4958-8773-a65f5ced80c6
keywords:
- Streams, Konfigurationen von Codecs
- Codecs, von dem Datenstrom Konfigurationen abgeleitet werden
- Streams, Codec-Formate
- Codecs, Formate
- Streams, iwmcodecinfo-Schnittstelle
- Iwmcodecinfo, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8657e03af97f9e4f1cae953d541c0e4369da193
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "104390040"
---
# <a name="getting-stream-configuration-information-from-codecs"></a>Informationen zu streamkonfigurations Informationen von Codecs

Für Audiodaten und Videostreams, die die Windows Media Audio-und Video Codecs verwenden, sollten Sie die Werte für die Datenstrom-Konfigurations Strukturen aus dem Codec erhalten, den Sie verwenden möchten. Obwohl es möglich ist, diese Werte selbst festzulegen, stellt die Verwendung der Codecs sicher, dass die Werte genau sind. Sie sollten die Werte in diesen Strukturen nur dann ändern, wenn in der Dokumentation ausdrücklich eine bestimmte Änderung empfohlen wird.

Informationen aus den Codecs werden in Form von Codec-Formaten angezeigt. Jedes Codec-Format ist ein einzelnes Streamformat, das vom Codec unterstützt wird. Weitere Informationen zu streamformaten finden Sie unter [Formate](formats.md).

Sie können Informationen von den Windows Media-Codecs mithilfe der Schnittstellen [**iwmcodecinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo), [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)und [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) des Profil-Manager-Objekts anfordern. Um die [**iwmprofilemanager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) -Schnittstelle eines Profil-Manager-Objekts abzurufen, müssen Sie die [**wmkreateprofilemanager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) -Funktion aufrufen. Nennen Sie **QueryInterface** für **iwmprofilemanager** , um **IWMCodecInfo3** abzurufen.

In den folgenden Abschnitten wird beschrieben, wie Sie die benötigten Informationen erhalten.



| `Section`                                                                                                | BESCHREIBUNG                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [So zählen Sie alle installierten Windows Media-Codecs auf](to-enumerate-all-installed-windows-media-codecs.md) | Beschreibt, wie die-Methoden der **iwmcodecinfo** -Schnittstelle und der **IWMCodecInfo2** -Schnittstelle verwendet werden, um den Namen und den Codec-Index der einzelnen installierten Windows Media Codec abzurufen. |
| [So zählen Sie Codec-Formate auf](to-enumerate-codec-formats.md)                                           | Hier wird beschrieben, wie Sie Datenstrom-Konfigurationsobjekte aus Codecs für die Verwendung in ihren Profilen erhalten.                                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konfigurieren von Streams**](configuring-streams.md)
</dt> </dl>

 

 




