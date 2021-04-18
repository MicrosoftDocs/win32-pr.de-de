---
description: In diesem Abschnitt werden die Strukturen beschrieben, die mit der escapefunktion von mxdc \_ und dem Microsoft XPS Document Converter (mxdc) verwendet werden.
ms.assetid: 102dc056-7f65-47d4-8bcd-3b11608bdb9c
title: Mxdc-escapecodestrukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b35c393d00dab227a91cbbb55eeca62039b41ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352557"
---
# <a name="mxdc-escape-code-structures"></a>Mxdc-escapecodestrukturen

In diesem Abschnitt werden die Strukturen beschrieben, die mit der escapefunktion von [**mxdc \_**](mxdc-escape.md) und dem Microsoft XPS Document Converter (mxdc) verwendet werden.

## <a name="in-this-section"></a>In diesem Abschnitt



| Struktur                                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**mxdc- \_ Escape- \_ Header \_ T**](mxdcescapeheader.md)<br/>                         | Die [**mxdc- \_ Escape- \_ Header- \_ T**](/windows/desktop/printdocs/mxdcescapeheader) -Struktur enthält den Vorgangs Code für einen [**extescape-extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) mit [**mxdc \_**](mxdc-escape.md) -Escapezeichen als *Nescape* -Parameter. Außerdem werden die Größen der Eingabe-und Ausgabepuffer bereitstellt.<br/>  |
| [**mxdc \_ get \_ filename \_ Data \_ T**](mxdcgetfilenamedata.md)<br/>                 | Die [**mxdc \_ get \_ filename \_ Data \_ T**](/windows/desktop/printdocs/mxdcgetfilenamedata) -Struktur enthält den vollständigen Pfad und den Dateinamen einer Microsoft XPS Document Converter (mxdc)-Ausgabedatei.<br/>                                                                                                     |
| [**mxdc \_ PrintTicket \_ Escape \_ T**](mxdcprintticketescape.md)<br/>               | Die [**mxdc \_ PrintTicket \_ Escape \_ t**](mxdcprintticketescape.md) -Struktur ist eine [**mxdc- \_ Escape-Header- \_ \_ t**](mxdcescapeheader.md) -Struktur, die mit einer [**mxdc \_ PrintTicket \_ Data \_ T**](mxdcprintticketpassthrough.md) -Struktur verkettet ist.<br/>                            |
| [**mxdc- \_ PrintTicket- \_ Daten \_ T**](mxdcprintticketpassthrough.md)<br/>            | Die [**mxdc \_ PrintTicket \_ Data \_ T**](/windows/desktop/printdocs/mxdcprintticketpassthrough) -Struktur enthält ein XPS-Dokument-Druck Ticket, das Drucker-und Druckauftrags Einstellungen enthält, die an die Microsoft XPS Document Converter (mxdc)-Ausgabedatei ohne Verarbeitung übergeben werden.<br/>              |
| [**Mxdc \_ S0PAGE \_ Data \_ T**](mxdcs0pagedata.md)<br/>                             | Die [**mxdc \_ S0PAGE \_ Data \_ T**](/windows/desktop/printdocs/mxdcs0pagedata) -Struktur enthält eine XPS-Dokument Seite, die ohne Verarbeitung an die Microsoft XPS Document Converter-Ausgabedatei (mxdc) übermittelt werden soll.<br/>                                                                                  |
| [**Mxdc \_ S0PAGE \_ Passthrough \_ -Escapezeichen \_**](mxdcs0pagepassthroughescape.md)<br/> | Die [**mxdc \_ S0PAGE \_ Passthrough \_ \_**](/windows/desktop/printdocs/mxdcs0pagepassthroughescape) -escapestruktur ist eine [**mxdc- \_ Escape-Header- \_ \_ t**](mxdcescapeheader.md) -Struktur, die mit einer [**mxdc \_ S0PAGE \_ Data \_ T**](mxdcs0pagedata.md) -Struktur verkettet ist.<br/>                             |
| [**Mxdc \_ S0PAGE \_ Resource \_ Escape \_ T**](mxdcs0pageresourceescape.md)<br/>       | Die [**mxdc \_ S0PAGE \_ Resource \_ Escape \_ t**](/windows/desktop/printdocs/mxdcs0pageresourceescape) -Struktur ist eine [**mxdc- \_ Escape-Header- \_ \_ t**](mxdcescapeheader.md) -Struktur, die mit einer [**mxdc \_ XPS \_ S0PAGE \_ Resource \_ T**](mxdcxpss0pageresource.md) -Struktur verkettet ist.<br/>                   |
| [**Mxdc \_ XPS \_ S0PAGE \_ Ressource \_ T**](mxdcxpss0pageresource.md)<br/>             | Die [**mxdc \_ XPS \_ S0PAGE \_ Resource \_ T**](/windows/desktop/printdocs/mxdcxpss0pageresource) -Struktur enthält Informationen über eine Ressource, z. b. ein Bild oder eine Schriftart, die einer XPS-Dokument Seite zugeordnet ist und an die Microsoft XPS Document Converter (mxdc)-Ausgabedatei übermittelt werden soll.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**mxdc-Escapezeichen \_**](mxdc-escape.md)
</dt> </dl>

 

