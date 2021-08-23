---
title: Bearbeiten von Metadatenattributen
description: Bearbeiten von Metadatenattributen
ms.assetid: 96c979e2-c616-45e3-9c60-a24f03e29dc4
keywords:
- Windows Medienformat-SDK, Bearbeiten von Metadatenattributen
- Advanced Systems Format (ASF), Bearbeiten von Metadatenattributen
- ASF (Advanced Systems Format), Bearbeiten von Metadatenattributen
- Metadaten, Bearbeiten von Attributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b973b787b37bbf9333a0adb218ab5db0e6f677521f1bfc9a0cdc1d5c37200e83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586060"
---
# <a name="editing-metadata-attributes"></a>Bearbeiten von Metadatenattributen

Das Bearbeiten von Metadatenattributen ähnelt dem Festlegen neuer Attribute. Anstatt [**IWMHeaderInfo3::AddAttribute zu**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute)verwenden, verwenden Sie [**IWMHeaderInfo3::ModifyAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-modifyattribute). **ModifyAttribute** ist mit **AddAttribute** identisch, aber Sie geben keinen Attributnamen an, und die Indexnummer ist ein Eingabeparameter anstelle einer Ausgabe.

Sie können die Streamnummer 0xFFFF verwenden, um ein Attribut anzugeben, das mit dem globalen Index geändert werden soll.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Arbeiten mit Metadaten**](working-with-metadata.md)
</dt> </dl>

 

 




