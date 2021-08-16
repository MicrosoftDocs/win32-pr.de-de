---
title: Abrufen von Metadatenattributen
description: Abrufen von Metadatenattributen
ms.assetid: d1d2c8e0-7445-4ee1-94d9-4c1ed74f8fe2
keywords:
- Windows Medienformat-SDK, Abrufen von Metadatenattributen
- Advanced Systems Format (ASF), Abrufen von Metadatenattributen
- ASF (Advanced Systems Format), Abrufen von Metadatenattributen
- Metadaten, Abrufen von Attributen
- Streams,Abrufen von Metadatenattributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02dc24f06779c12d40a109c1a8ef0fee9811370d3459f3811c0c870ee535d749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807880"
---
# <a name="retrieving-metadata-attributes"></a>Abrufen von Metadatenattributen

Um ein Attribut aus einem Dateiheader abzurufen, müssen Sie die Streamnummer und den Index des Attributs kennen. Sie können die [**IWMHeaderInfo3::GetAttributeIndices-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) verwenden, um die Indizes für alle Attribute mit dem gleichen Namen oder alle Indizes in derselben Sprache abzurufen. Wie die anderen Methoden von [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)verarbeitet **GetAttributeIndices** einen einzelnen Stream oder alle Attribute auf Dateiebene mithilfe von Stream 0. Sie können 0xFFFF für die Streamnummer verwenden, um globale Indizes abzurufen, die Ihren Kriterien in der gesamten Datei entsprechen, unabhängig von der Streamnummer.

Wenn Sie den Index des abzurufenden Attributs kennen, rufen Sie [**IWMHeaderInfo3::GetAttributeByIndexEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) auf, um das Attribut abzurufen. Sie müssen für jedes abgerufene Attribut zwei **GetAttributeByIndexEx-Aufrufe** vornehmen. Übergeben Sie beim ersten Aufruf **NULL** für den Namen und die Datenpufferzeiger, um die erforderliche Größe abzurufen. Ordnen Sie dann Puffer der angegebenen Größe zu, und rufen Sie den Zweiten auf, um den Namen und die Daten abzurufen.

Beispielcode zum Abrufen von Metadatenattributen finden Sie unter [So rufen Sie alle Metadaten in einer Datei ab.](to-retrieve-all-metadata-in-a-file.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Arbeiten mit Metadaten**](working-with-metadata.md)
</dt> </dl>

 

 




