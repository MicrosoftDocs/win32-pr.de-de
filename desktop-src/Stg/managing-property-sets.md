---
title: Verwalten von Eigenschaftensätzen
description: Ein persistenter Eigenschaftensatz enthält verknüpfte Daten als Eigenschaften.
ms.assetid: 19ff2751-87f3-43d8-9307-ce2dd399f694
keywords:
- Verwalten von Eigenschaftensätzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b6b81c466232d4fd325d53a3cfe67ebb1cbc60c757a6dfe135a021ab7892a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117960884"
---
# <a name="managing-property-sets"></a>Verwalten von Eigenschaftensätzen

Ein persistenter Eigenschaftensatz enthält verknüpfte Daten als Eigenschaften. Jeder Eigenschaftensatz wird mit einer FMTID und einer GUID (Globally Unique Identifier) identifiziert, mit der Anwendungen auf den Eigenschaftensatz zugreifen können, um den Eigenschaftensatz zu identifizieren. Durch diese Identifizierung interpretiert die Anwendung die Eigenschaften, die der Satz enthält.

Beispielsweise sind die Zeichenformatierungseigenschaften in einem Textprozessor oder die Renderingattribute eines Elements in einem Zeichenprogramm Eigenschaftensätze.

COM definiert die [**IPropertySetStorage-Schnittstelle,**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) um die Verwaltung von Eigenschaftensätzen zu vereinfachen. Mithilfe der Methoden dieser Schnittstelle können Sie einen neuen Eigenschaftensatz erstellen oder einen vorhandenen Eigenschaftensatz öffnen oder löschen. Darüber hinaus stellt sie eine Methode bereit, die einen Enumerator erstellt und einen Zeiger auf seine [**IEnumSTATPROPSETSTG-Schnittstelle**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) bereitstellt. Sie können die Methoden dieser Schnittstelle aufrufen, um [**STATPROPSETSTG-Strukturen**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) für Ihr Objekt aufzuzählen, die Informationen zu allen Eigenschaftensätzen für das Objekt bereitstellen.

Wenn Sie eine Instanz von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)erstellen oder öffnen, ähnelt dies dem Öffnen eines Objekts, das [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) oder [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)unterstützt, da Sie den Speichermodus angeben müssen, in dem Sie die Schnittstelle öffnen. Für **IStorage** sind dies der Transaktionsmodus, der Lese-/Schreibmodus und der Freigabemodus.

Wenn Sie einen Eigenschaftensatz mit einem Aufruf von [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)erstellen, geben Sie an, ob der Eigenschaftensatz einfach oder nicht einfach sein soll. Ein einfacher Eigenschaftensatz enthält Typen, die vollständig innerhalb des Eigenschaftensatzdatenstroms geschrieben werden können, der begrenzt werden soll und in Windows NT 4.0 und früher nicht größer als 256 KB sein darf, oder 1 MB in Windows 2000, Windows XP und Windows Server 2003. Wenn Sie jedoch eine größere Menge an Informationen im Eigenschaftensatz speichern müssen, können Sie angeben, dass der Eigenschaftensatz nicht einfach ist. Dadurch können Sie einen oder mehrere typen verwenden, die nur einen Zeiger auf ein Speicher- oder Streamobjekt angeben. Diese Typen sind VT \_ STREAM, VT \_ STREAMED OBJECT, VT \_ STORAGE und VT \_ STORED \_ OBJECT.

In diesen Eigenschaften gespeicherte Daten werden nicht mit dem Größenlimit von 256 KB in Windows NT 4.0 oder früher oder dem Grenzwert von 1 MB in Windows 2000, Windows XP und Windows Server 2003 gezählt. Es gelten jedoch Daten über die Eigenschaft, z. B. deren Name. Wenn Sie eine transaktionierte Aktualisierung benötigen, muss der Eigenschaftensatz nicht einfach sein. Es gibt natürlich eine bestimmte Leistungseinbuße beim Öffnen dieser Typen, da das Öffnen des Streams oder Speicherobjekts erforderlich ist, auf das Sie den Zeiger haben.

Wenn Ihre Anwendung Verbunddateien verwendet, können Sie die von COM bereitgestellte Implementierung dieser Schnittstellen verwenden, die für das COM-Verbunddateispeicherobjekt implementiert werden.

Jeder Eigenschaftensatz besteht in erster Linie aus einer logisch verbundenen Gruppe von Eigenschaften, wie unter [Verwalten von Eigenschaften](managing-properties.md)beschrieben.

Weitere Informationen zu Eigenschaftensätzen in COM finden Sie unter:

-   [Implementierungen von Eigenschaftensatz in COM](property-set-implementations-in-com.md)
-   [Überlegungen zum Eigenschaftensatz](property-set-considerations.md)
-   [Überlegungen zur IPropertySetStorage-Implementierung](ipropertysetstorage-implementation-considerations.md)
-   [Speichern von Eigenschaftensätzen](storing-property-sets.md)
-   [Leistungsmerkmale](performance-characteristics.md)
-   [Implementieren des Eigenschaftensatzes für Zusammenfassungsinformationen](implementing-the-summary-information-property-set.md)

 

 