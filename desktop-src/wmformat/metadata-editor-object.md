---
title: Metadata Editor-Objekt
description: Metadata Editor-Objekt
ms.assetid: 224eea1c-1d0d-47ac-9d99-c13674284f6d
keywords:
- Windows Media-Format-SDK, Metadaten-Editor-Objekte
- Advanced Systems Format (ASF), Metadaten-Editor-Objekte
- ASF (Advanced Systems Format), Metadaten-Editor-Objekte
- Objekte, Metadaten-Editor-Objekte
- Metadaten-Editor-Objekte, Informationen zu
- Metadaten, Editor-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27a30f5bd22bef9533352927901ad2b8a9e44fe
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724099"
---
# <a name="metadata-editor-object"></a>Metadata Editor-Objekt

Das Metadateneditor-Objekt wird verwendet, um die im Header Abschnitt von ASF-Dateien gespeicherten Informationen zu bearbeiten. Die gebräuchlichsten Elemente, die von diesem Objekt bearbeitet werden, sind Metadatenattribute. Darüber hinaus behandelt der Metadaten-Editor [*Marker*](wmformat-glossary.md) und Skript Befehle. Sie müssen den Metadateneditor nur dann verwenden, wenn Sie den Header einer vorhandenen Datei bearbeiten möchten, ohne Sie zu spielen.

Das Metadateneditor-Objekt wird von der [**wmkreateeditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor)-Funktion erstellt, mit der ein Zeiger auf eine **IWMMetadataEditor** -Schnittstelle festgelegt wird. Die anderen Schnittstellen des Metadateneditor-Objekts können durch Aufrufen der **QueryInterface** -Methode abgerufen werden.

Die folgenden Schnittstellen werden vom Metadateneditor-Objekt unterstützt.



| Schnittstelle                                        | BESCHREIBUNG                                                                                                                                                                                            |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iwmdrmeditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)             | Ermöglicht das Bearbeiten von Anwendungen, um die [*DRM*](wmformat-glossary.md) -Eigenschaften einer ASF-Datei zu untersuchen, ohne über Rechte zum Wiedergeben geschützter Inhalte zu verfügen. |
| [**Iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | Bearbeitet Attribute, Marker und Skript Befehle in der Kopfzeile.                                                                                                                                    |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)         | Ruft die Codec-Informationen ab. Erbt alle Methoden von **iwmheaderinfo**.                                                                                                                         |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)         | Bietet erweiterte Unterstützung für Attribute, einschließlich großer Attribute, mehrerer Sprachen und doppelter Attributnamen. Erbt alle Methoden von **iwmheaderinfo** und **IWMHeaderInfo2**.      |
| [**IWMMetadataEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor)   | Öffnet, schließt und speichert Änderungen am Header einer ASF-Datei.                                                                                                                                         |
| [**IWMMetadataEditor2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor2) | Öffnet eine ASF-Datei für die Header Bearbeitung mit mehreren Optionen für Dateizugriff und Freigabe. Erbt alle Methoden von **IWMMetadataEditor**.                                                              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Marker**](markers.md)
</dt> <dt>

[**Metadaten**](metadata.md)
</dt> <dt>

[**Objekte**](objects.md)
</dt> <dt>

[**Skriptbefehle**](script-commands.md)
</dt> <dt>

[**Arbeiten mit Metadaten**](working-with-metadata.md)
</dt> </dl>

 

 




