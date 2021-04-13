---
title: Festlegen von Metadatenattributen
description: Festlegen von Metadatenattributen
ms.assetid: a5d99361-9919-4548-a24d-900ac65cc634
keywords:
- Windows Media-Format-SDK, Festlegen von Metadatenattributen
- Advanced Systems Format (ASF), Festlegen von Metadatenattributen
- ASF (Advanced Systems Format), Festlegen von Metadatenattributen
- Metadaten, Festlegen von Attributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfde27d7bc965076d1a4b5f9674c6d198ce61da5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389912"
---
# <a name="setting-metadata-attributes"></a>Festlegen von Metadatenattributen

Metadatenattribute werden mithilfe der [**IWMHeaderInfo3:: AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) -Methode festgelegt.

Allen Attributen wird eine Sprache aus der Sprachliste für die Datei zugewiesen. Mithilfe der [**iwmlanguagelist**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) -Schnittstelle können Sie auf die Sprachliste zugreifen. Um einen Zeiger auf eine **iwmlanguagelist** -Schnittstelle zu erhalten, nennen Sie **QueryInterface** für jede beliebige Schnittstelle des Objekts, von dem Sie [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)abgerufen haben.

Sie können Attribute mit einem beliebigen Namen hinzufügen. Das Verwenden von Attributnamen, die keine von dem Windows Media Format SDK unterstützten Standardnamen sind, kann jedoch dazu führen, dass Ihre Metadaten schwer zu erkennen sind. Die meisten Medienspiel Anwendungen überprüfen Standardwerte. Weitere Informationen finden Sie unter [benutzerdefinierte Metadaten](custom-metadata.md).

Sie können die streamnummer 0xFFFF nicht zum globalen Hinzufügen eines Attributs verwenden. Jedes Attribut muss einer bestimmten streamnummer zugewiesen werden, oder es muss Stream 0 für Attribute auf Dateiebene zugewiesen werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Arbeiten mit Metadaten**](working-with-metadata.md)
</dt> </dl>

 

 




