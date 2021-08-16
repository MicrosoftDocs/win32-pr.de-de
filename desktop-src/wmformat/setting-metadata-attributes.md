---
title: Festlegen von Metadatenattributen
description: Festlegen von Metadatenattributen
ms.assetid: a5d99361-9919-4548-a24d-900ac65cc634
keywords:
- Windows Medienformat-SDK, Festlegen von Metadatenattributen
- Advanced Systems Format (ASF), Festlegen von Metadatenattributen
- ASF (Advanced Systems Format), Festlegen von Metadatenattributen
- Metadaten,Festlegen von Attributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa352a83e758b97bde6088377f8461a62b2d5071314d45f4978035bec219a5cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197510"
---
# <a name="setting-metadata-attributes"></a>Festlegen von Metadatenattributen

Metadatenattribute werden mithilfe der [**IWMHeaderInfo3::AddAttribute-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) festgelegt.

Allen Attributen wird eine Sprache aus der Sprachliste für die Datei zugewiesen. Sie können auf die Sprachliste zugreifen, indem Sie [**die IWMLanguageList-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) verwenden. Um einen Zeiger auf eine **IWMLanguageList-Schnittstelle** zu erhalten, rufen Sie **QueryInterface** für jede Schnittstelle des Objekts auf, von dem [**Sie IWMHeaderInfo3 erhalten haben.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)

Sie können Attribute mit einem beliebigen Namen hinzufügen. Die Verwendung von Attributnamen, bei denen es sich nicht um Standardnamen handelt, die vom Windows Media Format SDK unterstützt werden, kann die Suche nach Ihren Metadaten für Benutzer erschweren. Die meisten Medienanwendungen überprüfen auf Standardwerte. Weitere Informationen finden Sie unter [Benutzerdefinierte Metadaten.](custom-metadata.md)

Sie können die Streamnummer nicht 0xFFFF, um ein Attribut global hinzuzufügen. Sie müssen jedes Attribut einer bestimmten Streamnummer oder Stream 0 für Attribute auf Dateiebene zuweisen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Arbeiten mit Metadaten**](working-with-metadata.md)
</dt> </dl>

 

 




