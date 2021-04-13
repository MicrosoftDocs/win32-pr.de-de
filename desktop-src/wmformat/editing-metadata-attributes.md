---
title: Bearbeiten von Metadatenattributen
description: Bearbeiten von Metadatenattributen
ms.assetid: 96c979e2-c616-45e3-9c60-a24f03e29dc4
keywords:
- Windows Media-Format-SDK, Bearbeiten von Metadatenattributen
- Advanced Systems Format (ASF), Bearbeiten von Metadatenattributen
- ASF (Advanced Systems Format), Bearbeiten von Metadatenattributen
- Metadaten, Bearbeiten von Attributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52990e5366da178e9ed5021af93a9f6403b80c4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389921"
---
# <a name="editing-metadata-attributes"></a>Bearbeiten von Metadatenattributen

Das Bearbeiten von Metadatenattributen ähnelt dem Festlegen neuer Werte. Verwenden Sie anstelle von [**IWMHeaderInfo3:: AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute)das [**IWMHeaderInfo3:: modifyattribute-Attribut**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-modifyattribute). **Modifyattribute** ist mit **AddAttribute** identisch, mit dem Unterschied, dass Sie keinen Attributnamen angeben und die Indexnummer anstelle einer Ausgabe ein Eingabeparameter ist.

Mit der Stream-Nummer 0xFFFF können Sie ein Attribut angeben, das mit dem globalen Index geändert werden soll.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Arbeiten mit Metadaten**](working-with-metadata.md)
</dt> </dl>

 

 




