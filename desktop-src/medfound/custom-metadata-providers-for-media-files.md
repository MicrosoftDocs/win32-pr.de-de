---
description: In diesem Thema wird beschrieben, wie ein benutzerdefinierter Shell-Eigenschaftenhandler für eine Microsoft Media Foundation Medienquelle geschrieben wird.
ms.assetid: f8cf70ff-8324-4308-8adf-a145aa351ca9
title: Benutzerdefinierte Metadatenanbieter für Mediendateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1951fd90265299cb53369d521193740b7d4d05e0f1650583965eb670ab375cc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777600"
---
# <a name="custom-metadata-providers-for-media-files"></a>Benutzerdefinierte Metadatenanbieter für Mediendateien

In diesem Thema wird beschrieben, wie ein benutzerdefinierter Shell-Eigenschaftenhandler für eine Microsoft Media Foundation Medienquelle geschrieben wird.

> [!Note]  
> Hintergrundinformationen zu Metadatenanbietern in Media Foundation finden Sie unter [Medienmetadaten.](media-metadata.md) In diesem Thema werden Shelleigenschaftenhandler erläutert. es beschreibt nicht die Metadatenschnittstelle der Version [**1, OPCMetadata.**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)

 

Metadaten sind eng an das Format der Datei gebunden. In Media Foundation werden Dateiformate durch Medienquellen dargestellt. Wenn Sie Metadaten für ein Format unterstützen möchten, das in Media Foundation nicht nativ unterstützt wird, müssen Sie eine benutzerdefinierte Medienquelle mit einem Eigenschaftenhandler implementieren. Der Eigenschaftenhandler ermöglicht dem Shell-Eigenschaftensystem das effiziente Lesen und Schreiben von Metadaten.

Ein Eigenschaftenhandler ist ein COM-Objekt, das die folgenden Schnittstellen implementiert:

-   [**Iinitializewithstream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)
-   [**Ipropertystore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

Optional kann auch die folgende Schnittstelle verfügbar gemacht werden:

-   [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities)

Wenn das Shell-Eigenschaftensystem Metadaten für eine Datei abrufen muss, ruft es [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um den Eigenschaftenhandler zu erstellen, und ruft dann die entsprechenden Lese- und Schreibmethoden für die [**IPropertyStore-Schnittstelle**](/windows/win32/api/propsys/nn-propsys-ipropertystore) auf.

Die Media Foundation Pipeline verwendet einen etwas anderen Mechanismus, da die Pipeline den Eigenschaftenhandler direkt aus der Medienquelle erhält. Anstatt [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) zum Erstellen des Eigenschaftenhandlers aufzurufen, ruft die Pipeline [**ÜBERGETService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) für die Medienquelle auf, wie im Thema [Shell Metadata Providers](shell-metadata-providers.md)beschrieben.

Gehen Sie wie folgt vor, um einen benutzerdefinierten Eigenschaftenhandler zu erstellen:

-   Implementieren Sie die [**INTERFACESGetService-Schnittstelle,**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) um [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar zu machen. Die Dienst-GUID ist **MF \_ PROPERTY HANDLER \_ \_ SERVICE.**
-   Wenn die Medienquelle remote verwendet wird, muss sie zusätzlich zu [**DERENGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)auch die [**IPropertyStore-Schnittstelle**](/windows/win32/api/propsys/nn-propsys-ipropertystore) über die **QueryInterface-Methode** der Medienquelle verfügbar machen.
-   Um den Eigenschaftenhandler für das Shell-Eigenschaftensystem verfügbar zu machen, registrieren Sie die DLL für den Eigenschaftenhandler, wie unter [Registrieren und Verteilen von Eigenschaftenhandlern](../properties/prophand-reg-dist.md)beschrieben.
-   Die Medienquelle wird separat registriert, wie unter [Schemahandler und Byte-Stream Handler beschrieben.](scheme-handlers-and-byte-stream-handlers.md)

### <a name="implementation-tips"></a>Implementierung Tipps

Eine Liste der Metadateneigenschaftsschlüssel finden Sie unter [Metadateneigenschaften für Mediendateien.](metadata-properties-for-media-files.md)

Eigenschaftenhandler müssen schnell sein. sie müssen effizienten Lese- und Schreibzugriff auf die Metadaten bereitstellen. (Beachten Sie, dass die Shell Metadaten aus Hunderten von Dateien abrufen kann.) Rufen Sie daher [**mfstartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) nicht von Ihrem Eigenschaftenhandler auf. Die **MFStartup-Funktion** führt zu Startlatenz, da sie mehrere Arbeitswarteschlangenthreads erstellt und globalen Arbeitsspeicher zuweist.

In einer typischen Implementierung teilen sich der Eigenschaftenhandler und die Medienquelle einen Teil desselben Analysecodes. Eine Medienquelle verwendet jedoch asynchrone [**SUBSCRIBERByteStream-Aufrufe**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) für E/A, während der Eigenschaftenhandler die [**IStream-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-istream) verwendet. Media Foundation stellt ein Hilfsobjekt bereit, das einen **IStream-basierten** Datenstrom umschließt und als **EINEN GIGABYTEByteStream-Stream** verfügbar macht. Um den Wrapper zu erstellen, rufen [**Sie MFCreateMFByteStreamOnStream auf.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemfbytestreamonstream)

Beim Aktualisieren von Metadaten wird empfohlen, die Daten direkt in den ursprünglichen Stream zu schreiben. Diese Empfehlung unterscheidet sich vom Verhalten beim *Kopieren beim Schreiben* der meisten Eigenschaftenhandler, bei dem eine Kopie der Daten geändert wird. Mediendateien können sehr groß sein, sodass das Kopieren beim Schreiben für eine effiziente Implementierung in der Regel zu langsam ist. Um copy-on-write zu deaktivieren, legen Sie die Registrierungseinstellung **ManualSafeSave** fest, wie unter [Registrieren und Verteilen von Eigenschaftenhandlern](../properties/prophand-reg-dist.md)beschrieben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medienmetadaten](media-metadata.md)
</dt> <dt>

[Medienquellen](media-sources.md)
</dt> <dt>

[Schreiben einer benutzerdefinierten Medienquelle](writing-a-custom-media-source.md)
</dt> </dl>

 

 
