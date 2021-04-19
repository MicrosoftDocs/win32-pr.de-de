---
title: Verwalten von Eigenschafts Sätzen
description: Ein persistenter Eigenschaften Satz enthält verwandte Daten als Eigenschaften.
ms.assetid: 19ff2751-87f3-43d8-9307-ce2dd399f694
keywords:
- Verwalten von Eigenschafts Sätzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af3f9862d3074a5221bf1d5d975754486a562f87
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341726"
---
# <a name="managing-property-sets"></a>Verwalten von Eigenschafts Sätzen

Ein persistenter Eigenschaften Satz enthält verwandte Daten als Eigenschaften. Jeder Eigenschaften Satz wird mit einer fmtid identifiziert, und eine Globally Unique Identifier (GUID), die es Anwendungen ermöglicht, auf den Eigenschaften Satz zuzugreifen, um den Eigenschaften Satz zu identifizieren. Durch diese Identifikation interpretiert die Anwendung die Eigenschaften, die in der Gruppe enthalten sind.

Beispielsweise sind die Zeichen Formatierungs Eigenschaften in einem Textverarbeitungsprogramm oder die renderingattribute eines Elements in einem Zeichnungsprogramm Eigenschafts Sätze.

COM definiert die [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Schnittstelle, um die Verwaltung von Eigenschafts Sätzen zu vereinfachen. Mithilfe der Methoden dieser Schnittstelle können Sie einen neuen Eigenschaften Satz erstellen oder einen vorhandenen Eigenschaften Satz öffnen oder löschen. Außerdem stellt Sie eine Methode bereit, die einen Enumerator erstellt und einen Zeiger auf die zugehörige [**ienumstatus propsetstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) -Schnittstelle bereitstellt. Sie können die Methoden dieser Schnittstelle aufrufen, um die [**Status**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) Wert-Strukturen für das Objekt aufzulisten, das Informationen zu allen Eigenschafts Sätzen für das Objekt bereitstellt.

Wenn Sie eine Instanz von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)erstellen oder öffnen, ähnelt Sie dem Öffnen eines Objekts, das [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) oder [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)unterstützt, da Sie den Speicher Modus angeben müssen, in dem Sie die Schnittstelle öffnen. Für **IStorage** umfassen diese den Transaktionsmodus, den Lese-/Schreibmodus und den Freigabe Modus.

Wenn Sie einen Eigenschaften Satz mit einem [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)-Befehl erstellen, geben Sie an, ob der Eigenschaften Satz einfach oder nicht einfach sein soll. Ein einfacher Eigenschaften Satz enthält Typen, die vollständig in den Eigenschaftenset-Stream geschrieben werden können. dieser ist für eine begrenzte Größe vorgesehen und darf nicht größer als 256 KB in Windows NT 4,0 und früher oder 1 MB in Windows 2000, Windows XP und Windows Server 2003 sein. Wenn Sie jedoch eine größere Menge an Informationen im Eigenschaften Satz speichern müssen, können Sie angeben, dass der Eigenschaften Satz nicht einfach ist. Dies ermöglicht es Ihnen, einen oder mehrere der Typen zu verwenden, die nur einen Zeiger auf ein Speicher-oder Streamobjekt angeben. Diese Typen sind VT \_ Stream, VT \_ -Streaming-Objekt, VT \_ -Speicher und \_ gespeichertes VT- \_ Objekt.

Die in diesen Eigenschaften gespeicherten Daten werden in Windows NT 4,0 oder früher nicht mit der Größenbeschränkung von 256 KB-Eigenschaften Satz in Windows NT oder früher gezählt, oder das Limit von 1 MB in Windows 2000, Windows XP und Windows Server 2003. Allerdings gelten die Daten über die Eigenschaft, z. b. den Namen,. Wenn Sie ein transaktives Update benötigen, muss der Eigenschaften Satz außerdem nicht einfach sein. Es gibt natürlich eine bestimmte Leistungs Einbuße zum Öffnen dieser Typen, da es erforderlich ist, den Stream oder das Speicher Objekt zu öffnen, für das Sie über den Zeiger verfügen.

Wenn Ihre Anwendung Verbund Dateien verwendet, können Sie die von com bereitgestellte Implementierung dieser Schnittstellen verwenden, die auf dem com-Verbund Dateispeicher Objekt implementiert werden.

Jeder Eigenschaften Satz besteht hauptsächlich aus einer logisch verbundenen Gruppe von Eigenschaften, wie unter [Verwalten von Eigenschaften](managing-properties.md)beschrieben.

Weitere Informationen zu Eigenschafts Sätzen in com finden Sie unter:

-   [Eigenschaften Satz Implementierungen in com](property-set-implementations-in-com.md)
-   [Überlegungen zu Eigenschaften Gruppen](property-set-considerations.md)
-   [Überlegungen zur IPropertySetStorage-Implementierung](ipropertysetstorage-implementation-considerations.md)
-   [Speichern von Eigenschafts Sätzen](storing-property-sets.md)
-   [Leistungsmerkmale](performance-characteristics.md)
-   [Implementieren des Eigenschaften Satzes für Zusammenfassungs Informationen](implementing-the-summary-information-property-set.md)

 

 