---
description: In diesem Thema wird beschrieben, wie ein benutzerdefinierter shelleigenschaftenhandler für eine Microsoft Media Foundation Medienquelle geschrieben wird.
ms.assetid: f8cf70ff-8324-4308-8adf-a145aa351ca9
title: Benutzerdefinierte Metadatenanbieter für Mediendateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2ded77492d03f7b802f6b2f9c25e1009ef97f50
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106357153"
---
# <a name="custom-metadata-providers-for-media-files"></a>Benutzerdefinierte Metadatenanbieter für Mediendateien

In diesem Thema wird beschrieben, wie ein benutzerdefinierter shelleigenschaftenhandler für eine Microsoft Media Foundation Medienquelle geschrieben wird.

> [!Note]  
> Hintergrundinformationen zu metadatenanbietern in Media Foundation finden Sie unter [Medien Metadaten](media-metadata.md). In diesem Thema werden shelleigenschaftenhandler behandelt. die Metadatenschnittstelle der Version 1, [**IMF Metadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata), wird nicht beschrieben.

 

Metadaten sind eng an das Format der Datei gebunden. In Media Foundation werden Dateiformate durch Medienquellen dargestellt. Wenn Sie Metadaten für ein Format unterstützen möchten, das in Media Foundation nicht nativ unterstützt wird, müssen Sie eine benutzerdefinierte Medienquelle mit einem Eigenschaften Handler implementieren. Der Eigenschaften Handler ermöglicht dem shelleigenschaftensystem das effiziente lesen und Schreiben von Metadaten.

Ein Eigenschafts Handler ist ein COM-Objekt, das die folgenden Schnittstellen implementiert:

-   [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)
-   [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

Optional kann auch die folgende Schnittstelle verfügbar gemacht werden:

-   [**Ipropertystorecapabilitäten**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities)

Wenn das shelleigenschaftensystem Metadaten für eine Datei erhalten muss, ruft es [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um den Eigenschafts Handler zu erstellen, und ruft dann die entsprechenden Lese-und Schreib Methoden in der [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Schnittstelle auf.

Die Media Foundation Pipeline verwendet einen etwas anderen Mechanismus, da die Pipeline den Eigenschaften Handler direkt aus der Medienquelle abruft. Anstatt [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) zum Erstellen des Eigenschaften Handlers aufzurufen, ruft die Pipeline [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) auf der Medienquelle auf, wie im Thema [shellmetadatenanbieter](shell-metadata-providers.md)beschrieben.

Gehen Sie folgendermaßen vor, um einen benutzerdefinierten Eigenschaften Handler zu erstellen:

-   Implementieren Sie die [**imfgetservice**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) -Schnittstelle, um [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar zu machen. Die Dienst-GUID ist der **MF- \_ \_ eigenschaftenhandlerdienst \_**
-   Wenn die Medienquelle Remote verwendet wird, muss Sie zusätzlich zu [**imfgetservice**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)auch die [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Schnittstelle über die **QueryInterface** -Methode der Medienquelle verfügbar machen.
-   Um den Eigenschaften Handler für das Shell-Eigenschaften System verfügbar zu machen, registrieren Sie die DLL für den Eigenschafts Handler, wie unter [registrieren und Verteilen von Eigenschaften Handlern](../properties/prophand-reg-dist.md)beschrieben.
-   Die Medienquelle wird separat registriert, wie in [Schema Handler und Byte-Stream Handlern](scheme-handlers-and-byte-stream-handlers.md)beschrieben.

### <a name="implementation-tips"></a>Implementierungs Tipps

Eine Liste der Metadaten-Eigenschafts Schlüssel finden Sie unter [Metadateneigenschaften für Mediendateien](metadata-properties-for-media-files.md).

Eigenschaften Handler müssen schnell sein. Sie müssen einen effizienten Lese-und Schreibzugriff auf die Metadaten bereitstellen. (Beachten Sie, dass die Shell Metadaten aus Hunderten von Dateien abrufen kann.) Daher müssen Sie [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) nicht über Ihren Eigenschafts Handler abrufen. Die **MF Startup** -Funktion führt die Start Latenz ein, da Sie mehrere Arbeitswarteschlangen-Threads erstellt und globalen Speicher belegt.

In einer typischen-Implementierung teilen sich der Eigenschaften Handler und die Medienquelle einen Teil desselben Code Codes. Eine Medienquelle verwendet jedoch asynchrone [**IMF Bytestream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) -Aufrufe für e/a-Vorgänge, während der Eigenschafts Handler die [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) -Schnittstelle verwendet. Media Foundation stellt ein Hilfsobjekt bereit, das einen **IStream**-basierten Datenstrom umschließt und ihn als **imfbytestream** -Stream verfügbar macht. Rufen Sie zum Erstellen des Wrappers [**mfkreatemfbytestreamonstream**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemfbytestreamonstream)auf.

Beim Aktualisieren von Metadaten wird empfohlen, die Daten direkt in den ursprünglichen Stream zu schreiben. Diese Empfehlung unterscheidet sich vom Verhalten bei den meisten Eigenschaften Handlern, bei denen eine Kopie der Daten geändert wird, vom *Kopier-/Schreib-Verhalten* . Mediendateien können sehr groß sein, daher ist Copy-on-Write in der Regel zu langsam für eine effiziente Implementierung. Legen Sie zum Deaktivieren von Copy-on-Write die Registrierungs Einstellung **manualsafesave** fest, wie unter [registrieren und Verteilen von Eigenschaften Handlern](../properties/prophand-reg-dist.md)beschrieben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medien Metadaten](media-metadata.md)
</dt> <dt>

[Medienquellen](media-sources.md)
</dt> <dt>

[Schreiben einer benutzerdefinierten Medienquelle](writing-a-custom-media-source.md)
</dt> </dl>

 

 
