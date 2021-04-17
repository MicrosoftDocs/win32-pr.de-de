---
title: Attribute (Windows Media-Format 11 SDK)
description: Attribute
ms.assetid: 1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4
keywords:
- Windows Media-Format-SDK, Attribute
- Advanced Systems Format (ASF), Attribute
- ASF (Advanced Systems Format), Attribute
- Attribute, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c209558ed4803fee96e9b482302af1864cbf988b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391426"
---
# <a name="attributes-windows-media-format-11-sdk"></a>Attribute (Windows Media-Format 11 SDK)

Bei einem Attribut handelt es sich um ein einzelnes Element von Metadaten. Die meisten Attribute können von der Anwendung festgelegt und in den Header einer ASF-Datei geschrieben werden.

Einige der vordefinierten Attribute sind codierte Attribute. Diese Attribute werden nicht im Header einer ASF-Datei gespeichert, sondern durch die Objekte des Windows Media Format SDK berechnet, wenn die Datei geladen wird. Da codierte Attribute immer berechnet werden, sind Sie grundsätzlich schreibgeschützt.

Dieses SDK enthält viele Attribut Definitionen, die Sie verwenden können. Sie können auch eigene Attribute erstellen, um Inhalte zu beschreiben.

In den folgenden Abschnitten werden die vordefinierten Attribute beschrieben.



| `Section`                                                                | BESCHREIBUNG                                                                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Attributliste](attribute-list.md)                                   | Stellt eine alphabetische Liste aller vordefinierten Attribute bereit. Nach der Liste wird jedes Attribut einzeln beschrieben.                                                                          |
| [Attribute mit mehreren Werten](attributes-with-multiple-values.md) | Listet die Attribute auf, die einer Datei mehrmals hinzugefügt werden können.                                                                                                                                      |
| [Attribute nach Typ](attributes-by-type.md)                           | Enthält Listen von Attributen, sortiert nach Typ. Hierzu zählen Listen mit speziellen Attributen (wie z. b. die, die mit Digital Rights Management arbeiten) und Listen der vorgeschlagenen Attribute nach Inhaltstyp. |
| [Unterstützung für Unterstützung](id3-tag-support.md)                                 | Listet die Attribute auf, die mit ID3-Tags kompatibel sind.                                                                                                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmheaderinfo:: getattributebyindex**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyindex)
</dt> <dt>

[**Iwmheaderinfo:: getattributebyname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)
</dt> <dt>

[**Iwmheaderinfo:: Event Tribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute)
</dt> <dt>

[**Arbeiten mit Metadaten**](working-with-metadata.md)
</dt> </dl>

 

 




