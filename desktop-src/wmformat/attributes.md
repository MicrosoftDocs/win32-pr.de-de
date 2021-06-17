---
title: Attribute (Windows Media Format 11 SDK)
description: Erfahren Sie mehr über Attribute im Windows Media Format 11 SDK. Ein Attribut ist ein einzelnes Element von Metadaten.
ms.assetid: 1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4
keywords:
- Windows Media Format SDK, Attribute
- Advanced Systems Format (ASF), Attribute
- ASF (Advanced Systems Format), Attribute
- Attribute,About
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23738e20df2c6360b20b7c3da005cde6b3942d44
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262192"
---
# <a name="attributes-windows-media-format-11-sdk"></a>Attribute (Windows Media Format 11 SDK)

Ein Attribut ist ein einzelnes Element von Metadaten. Die meisten Attribute können von Ihrer Anwendung festgelegt werden und werden in den Header einer ASF-Datei geschrieben.

Einige der vordefinierten Attribute sind codierte Attribute. Diese Attribute werden nicht im Header einer ASF-Datei gespeichert, sondern von den Objekten des Windows Media Format SDK berechnet, wenn die Datei geladen wird. Da codierte Attribute immer berechnet werden, sind sie grundsätzlich schreibgeschützt.

Dieses SDK enthält viele Attributdefinitionen, die Sie verwenden können. Sie können auch eigene Attribute erstellen, um Inhalte zu beschreiben.

In den folgenden Abschnitten werden die vordefinierten Attribute beschrieben.



| `Section`                                                                | BESCHREIBUNG                                                                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Attributliste](attribute-list.md)                                   | Stellt eine alphabetische Liste aller vordefinierten Attribute zur Nach der Liste wird jedes Attribut einzeln beschrieben.                                                                          |
| [Attribute mit mehreren Werten](attributes-with-multiple-values.md) | Listet die Attribute auf, die einer Datei mehr als einmal hinzugefügt werden können.                                                                                                                                      |
| [Attribute nach Typ](attributes-by-type.md)                           | Enthält Listen von Attributen, die nach Typ sortiert sind. Dazu gehören Listen von Speziellen Attributen (z. B. solche, die sich mit der Verwaltung digitaler Rechte beschäftigen) und Listen mit vorgeschlagenen Attributen nach Inhaltstyp. |
| [UNTERSTÜTZUNG FÜR ID3-Tags](id3-tag-support.md)                                 | Listet die Attribute auf, die mit ID3-Tags kompatibel sind.                                                                                                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMHeaderInfo::GetAttributeByIndex**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyindex)
</dt> <dt>

[**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)
</dt> <dt>

[**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute)
</dt> <dt>

[**Arbeiten mit Metadaten**](working-with-metadata.md)
</dt> </dl>

 

 




