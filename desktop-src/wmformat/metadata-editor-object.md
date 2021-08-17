---
title: Metadata Editor-Objekt
description: Metadata Editor-Objekt
ms.assetid: 224eea1c-1d0d-47ac-9d99-c13674284f6d
keywords:
- Windows Medienformat-SDK, Metadaten-Editor-Objekte
- Advanced Systems Format (ASF), Metadaten-Editor-Objekte
- ASF (Advanced Systems Format), Metadaten-Editorobjekte
- Objekte,Metadaten-Editor-Objekte
- Metadaten-Editor-Objekte,About
- Metadaten,Editor-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e8e78aaf6ada96a9cefa1a9ec6f4aa5708c7382539bc3b75493734c18d600b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027448"
---
# <a name="metadata-editor-object"></a>Metadata Editor-Objekt

Das Metadaten-Editor-Objekt wird verwendet, um Informationen zu bearbeiten, die im Headerabschnitt von ASF-Dateien gespeichert sind. Die am häufigsten von diesem Objekt bearbeiteten Dinge sind Metadatenattribute. Darüber hinaus befasst sich der Metadaten-Editor mit [*Markern*](wmformat-glossary.md) und Skriptbefehlen. Der Metadaten-Editor muss nur verwendet werden, wenn Sie den Header einer vorhandenen Datei bearbeiten möchten, ohne ihn wieder verwenden zu müssen.

Das Metadaten-Editor-Objekt wird von der [**Funktion WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor)erstellt, die einen Zeiger auf eine **IWMMetadataEditor-Schnittstelle** legt. Die anderen Schnittstellen des Metadaten-Editorobjekts können durch Aufrufen der **QueryInterface-Methode ermittelt** werden.

Die folgenden Schnittstellen werden vom Metadaten-Editor-Objekt unterstützt.



| Schnittstelle                                        | BESCHREIBUNG                                                                                                                                                                                            |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)             | Ermöglicht das Bearbeiten von Anwendungen, um die [*DRM-Eigenschaften*](wmformat-glossary.md) einer ASF-Datei zu untersuchen, ohne über Rechte zum Wiederspielen des geschützten Inhalts zu besitzen. |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | Bearbeitet Attribute, Marker und Skriptbefehle im Header.                                                                                                                                    |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)         | Ruft Codecinformationen ab. Erbt alle Methoden von **IWMHeaderInfo.**                                                                                                                         |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)         | Bietet erweiterte Unterstützung für Attribute, einschließlich großer Attribute, mehrerer Sprachen und doppelter Attributnamen. Erbt alle Methoden von **IWMHeaderInfo** und **IWMHeaderInfo2.**      |
| [**IWMMetadataEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor)   | Öffnet, schließt und speichert Änderungen am Header einer ASF-Datei.                                                                                                                                         |
| [**IWMMetadataEditor2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor2) | Öffnet eine ASF-Datei für die Headerbearbeitung mit mehreren Dateizugriffs- und Freigabeoptionen. Erbt alle Methoden von **IWMMetadataEditor**.                                                              |



 

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

 

 




