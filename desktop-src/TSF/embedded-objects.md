---
title: Eingebettete Objekte (Text Dienst-Framework)
description: Mit dem Text Services-Framework kann ein Text Dienst Objekte in einen anwendungstextstream einbetten.
ms.assetid: 44cb22b5-707b-4f21-b986-5258ed273543
keywords:
- Text Dienst Framework (TSF), eingebettete Objekte
- TSF (Text Services Framework), eingebettete Objekte
- TSF-aktivierte Anwendungen, eingebettete Objekte
- Eingebettete Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e4f819e6f42cc4e8d2ed81e47c79efe5ff7407
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104563354"
---
# <a name="embedded-objects-text-services-framework"></a>Eingebettete Objekte (Text Dienst-Framework)

Mit dem Text Services-Framework kann ein Text Dienst Objekte in einen anwendungstextstream einbetten. Eingebettete Objekte werden mithilfe des Werts [TS \_ Char \_ Embedded](ts-char--constants.md)in den Textstream eingefügt. Dieser Wert wird mit hexadezimal Schreibweise in das Ersatz Zeichen "U + fffc" von Unicode-Objekten aufgelöst. Die folgende Abbildung zeigt z. b. das Rendering eines eingebetteten *Objekts, das* das japanische Ideogramm-Zeichen darstellt, in Kombination mit der Sequenz von Unicode-Zeichen, die die englische Übersetzung von "Sun" darstellen.

![Zeichencodierung eines eingebetteten Objekts](images/emb-obj.gif)

Die obere Zeile der Abbildung enthält den übersetzten Text, der aus dem Wort "Sun" gefolgt von dem japanischen Zeichen für Sun, *Hi* besteht. Die Mitte der Zeile der Abbildung zeigt das Unicode-Zeichen. Im Fall von U + fffc ist dies das Objekt Ersetzungs Zeichen. Die untere Zeile der Abbildung zeigt den Hexadezimalwert der einzelnen Zeichen.

## <a name="supporting-embedded-objects-in-an-application"></a>Unterstützen von eingebetteten Objekten in einer Anwendung

Der TSF-Manager fügt ein eingebettetes Objekt in den Textstream ein, indem es [ITextStoreACP:: insertemembedded](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-insertembedded) für eine ACP-basierte Anwendung oder [itextstoreanchor:: insertemembedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded) für eine Anker basierte Anwendung anfordert. Wenn ein eingebettetes Objekt eingefügt wird, sollte die Anwendung den " **TS \_ Char \_ Embedded** "-Wert an der Zeichenposition (oder Ankerposition) platzieren, an der das Objekt eingebettet ist, und das dem eingebetteten Objekt zugeordnete IDataObject-Objekt speichern. Wenn [ITextStoreACP:: gettext](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-gettext) oder [itextstoreanchor:: gettext](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) aufgerufen wird und ein eingebettetes Objekt im erhaltenen Text enthalten ist, gibt der **TS \_ Char \_ Embedded** -Wert das vorhanden sein und den Speicherort des eingebetteten Objekts an. Rufen Sie zum Abrufen des eingebetteten Objekts [ITextStoreACP:: getemembedded](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getembedded) mit der Zeichenposition des eingebetteten Objekts oder [itextstoreanchor:: getemembedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) mit der Ankerposition des eingebetteten Objekts auf.

Die Anwendung erkennt den eingebetteten Objekt Inhalt normalerweise nicht. Die Anwendung kann versuchen, Anzeigeinformationen aus dem Objekt selbst abzurufen. Wenn das eingebettete Objektdaten in einem Format bereitstellen kann, das von der Anwendung erkannt wird, z. b. CF \_ UnicodeText oder CF \_ Bitmap, kann die Anwendung Grafik Informationen anzeigen, die vom-Objekt bereitgestellt werden.

## <a name="inserting-embedded-objects"></a>Einfügen von eingebetteten Objekten

Ein Text Dienst fügt ein eingebettetes Objekt in einen Kontext ein, indem [itfrange:: insertemembedded](/windows/desktop/api/msctf/nf-msctf-itfrange-insertembedded) oder [itfinsertatselection:: insertembeddedatselection](/windows/desktop/api/msctf/nf-msctf-itfinsertatselection-insertembeddedatselection)aufgerufen wird. Der Text Dienst muss das eingebettete IDataObject-Objekt bereitstellen.

 

 
