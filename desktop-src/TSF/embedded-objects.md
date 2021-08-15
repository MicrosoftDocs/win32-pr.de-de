---
title: Eingebettete Objekte (Textdienstframework)
description: Textdienstframework ermöglicht einem Textdienst das Einbetten von Objekten in einen Anwendungstextstream.
ms.assetid: 44cb22b5-707b-4f21-b986-5258ed273543
keywords:
- Textdienstframework (TSF), eingebettete Objekte
- TSF (Textdienstframework),eingebettete Objekte
- TSF-fähige Anwendungen,eingebettete Objekte
- Eingebettete Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c45c14138df39142f503882c8d735ff1638618e028870af6aa67c25bc1a98b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118879678"
---
# <a name="embedded-objects-text-services-framework"></a>Eingebettete Objekte (Textdienstframework)

Textdienstframework ermöglicht einem Textdienst das Einbetten von Objekten in einen Anwendungstextstream. Eingebettete Objekte werden mit dem Wert TS CHAR EMBEDDED in den Textstream [ \_ \_ eingefügt.](ts-char--constants.md) Dieser Wert wird mit hexadezimaler Notation in das Unicode-Objektersetzungszeichen U+fffc auflösen. Die folgende Abbildung zeigt z. B. das Rendern eines eingebetteten Objekts, das die japanische Ideogramm *hi* darstellt, in Kombination mit der Sequenz von Unicode-Zeichen, die die englische Übersetzung von "Sun" darstellen.

![Zeichencodierung eines eingebetteten Objekts](images/emb-obj.gif)

Die obere Zeile der Abbildung enthält den übersetzten Text, der aus dem Wort "Sun" gefolgt vom japanischen Zeichen für sun, *hi, besteht.* Die mitte Zeile der Abbildung zeigt das Unicode-Zeichen. Im Fall von U+fffc ist dies das Objektersetzungszeichen. Die untere Zeile der Abbildung zeigt den Hexadezimalwert jedes Zeichens.

## <a name="supporting-embedded-objects-in-an-application"></a>Unterstützen eingebetteter Objekte in einer Anwendung

Der TSF-Manager fügt ein eingebettetes Objekt in den Textstream ein, indem er [ITextStoreACP::InsertEmbedded](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-insertembedded) für eine ACP-basierte Anwendung oder [ITextStoreAnchor::InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded) für eine ankerbasierte Anwendung aufruft. Wenn ein eingebettetes Objekt eingefügt wird, sollte die Anwendung den **TS \_ CHAR \_ EMBEDDED-Wert** an der Zeichenposition (oder an der Ankerposition) platzieren, an der das Objekt eingebettet ist, und das IDataObject speichern, das dem eingebetteten Objekt zugeordnet ist. Wenn [ITextStoreACP::GetText](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-gettext) oder [ITextStoreAnchor::GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) aufgerufen wird und ein eingebettetes Objekt im erhaltenen Text enthalten ist, gibt der **TS CHAR \_ \_ EMBEDDED-Wert** das Vorhandensein und den Speicherort des eingebetteten Objekts an. Rufen Sie zum Abrufen des eingebetteten Objekts [ITextStoreACP::GetEmbedded](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getembedded) mit der Zeichenposition des eingebetteten Objekts oder [ITextStoreAnchor::GetEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) mit der Ankerposition des eingebetteten Objekts auf.

Die Anwendung erkennt normalerweise den eingebetteten Objektinhalt nicht. Die Anwendung kann versuchen, Anzeigeinformationen aus dem Objekt selbst zu erhalten. Wenn das eingebettete Objekt Daten in einem Format angeben kann, das von der Anwendung erkannt wird, z. B. CF UNICODETEXT oder CF BITMAP, kann die Anwendung grafische Informationen anzeigen, die vom \_ \_ -Objekt bereitgestellt werden.

## <a name="inserting-embedded-objects"></a>Einfügen eingebetteter Objekte

Ein Textdienst fügt ein eingebettetes Objekt in einen Kontext ein, indem [er ITfRange::InsertEmbedded](/windows/desktop/api/msctf/nf-msctf-itfrange-insertembedded) oder [ITfInsertAtSelection::InsertEmbeddedAtSelection aufruft.](/windows/desktop/api/msctf/nf-msctf-itfinsertatselection-insertembeddedatselection) Der Textdienst muss das eingebettete IDataObject-Objekt liefern.

 

 
