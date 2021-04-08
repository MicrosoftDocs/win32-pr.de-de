---
title: Abrufen von Metadatenattributen
description: Abrufen von Metadatenattributen
ms.assetid: d1d2c8e0-7445-4ee1-94d9-4c1ed74f8fe2
keywords:
- Windows Media-Format-SDK, Abrufen von Metadatenattributen
- Advanced Systems Format (ASF), Abrufen von Metadatenattributen
- ASF (Advanced Systems Format), Abrufen von Metadatenattributen
- Metadaten, Abrufen von Attributen
- Streams, Abrufen von Metadatenattributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c918cb47e77c3fd69c64de586b84b7f6244e4c9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038520"
---
# <a name="retrieving-metadata-attributes"></a>Abrufen von Metadatenattributen

Wenn Sie ein Attribut aus einem Dateiheader abrufen möchten, müssen Sie die streamnummer und den Index des Attributs kennen. Mit der [**IWMHeaderInfo3:: getattributeindices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) -Methode können Sie die Indizes für alle Attribute mit demselben Namen oder allen Indizes in derselben Sprache erhalten. Wie bei den anderen Methoden von [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)behandelt **getattributeindices** einen einzelnen Stream oder alle Attribute auf Dateiebene mit Stream 0. Sie können "0xFFFF" für die Datenstrom Nummer verwenden, um globale Indizes zu erhalten, die Ihren Kriterien innerhalb der gesamten Datei entsprechen, unabhängig von der Datenstrom Nummer.

Wenn Sie den Index des Attributs kennen, das Sie abrufen möchten, rufen Sie [**IWMHeaderInfo3:: getattributebyindexex**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) auf, um das Attribut abzurufen. Sie müssen für jedes abgerufene Attribut zwei Aufrufe an **getattributebyindexex** durchführen. Übergeben Sie beim ersten-Befehl **null** für den Namen und Datenpuffer Zeiger, um die benötigte Größe abzurufen. Weisen Sie dann Puffer der angegeben Größe zu, und führen Sie den zweiten Rückruf aus, um den Namen und die Daten abzurufen.

Beispielcode, der zeigt, wie Metadatenattribute abgerufen werden, finden [Sie unter So rufen Sie alle Metadaten in einer Datei](to-retrieve-all-metadata-in-a-file.md)ab.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Arbeiten mit Metadaten**](working-with-metadata.md)
</dt> </dl>

 

 




